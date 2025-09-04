# Gestão de dados descentralizada

- Normalmente temos um banco de dados monolítico com centenas de tabelas

- A alteração nos esquema de dados é mediado por um AD (administrador de dados)

- O suporte em produção é mediado por um DBA (administrador do banco de dados)

- Microsserviços preferem permitir que cada serviço gerencie sua própria base de dados, quer através de diferentes instâncias usando a mesma tecnologia de banco de dados, ou até mesmo usando diferentes sistemas de banco de dados – uma abordagem 
chamada Polyglot Persistence

- Uma base de dados proprietária para cada microsserviço não implica que cada microsserviço use um servidor de banco de dados dedicado

- Saber diferenciar a visão lógica da visão física é importante na arquitetura de microsserviços para evitar complexidade acidental na infraestrutura de dados

- Em microsserviços a gestão de dados se torna descentralizada

- Isso envolve modelos mentais diferentes para o arquiteto e o time

- Complexidades acidentais devem ser resolvidas com padrões como o SAGA e o CQRS

## Benefícios

- Ajuda a garantir que os serviços sejam fracamente acoplados. As alterações no banco de dados de um serviço não afetam nenhum outro serviço

- Cada serviço pode usar o tipo de banco de dados mais adequado às suas necessidades

- Exemplo
    - Um serviço que faz pesquisas de texto pode usar o ElasticSearch
    - Um serviço que manipula um grafo social poderia usar o Neo4j

## Pontos de atenção

- A implementação de transações distribuídas que abrangem vários serviços não é simples. É melhor evitar transações distribuídas por causa do teorema de CAP e usar padrões como o SAGA

- A implementação de consultas que associam dados que agora estão em vários bancos de dados é um desafio

- Complexidade do gerenciamento de vários bancos de dados SQL e NoSQL

## Controle transacional

- A responsabilidade descentralizada para os dados através dos microsserviços tem implicações para a administração de atualizações

- A abordagem comum para lidar com atualizações tem sido usar transações para garantir a atualização de múltiplos recursos. Esta abordagem é usada frequentemente em estruturas monolíticas

- O uso de transações como estas ajuda com a consistência, mas impõem um acoplamento temporário significante, que é problemático quando existem múltiplos serviços

- Transações distribuídas são nitidamente difíceis para implementar e como consequência, arquiteturas em microsserviços enfatizam a coordenação sem transação entre serviços 

- Existe o reconhecimento explícito que consistência pode ser somente eventual e os problemas gerados por isto são lidados com operações que compensem esta questão

- Um padrão comum para lidar com isso é o SAGA

### SAGA

O **Padrão Saga** é um padrão arquitetural usado para gerenciar **transações distribuídas** em sistemas de microsserviços.  
Ele garante **consistência de dados** em operações que envolvem múltiplos serviços, sem a necessidade de um **2PC (Two-Phase Commit)**, que é custoso e pouco escalável.

#### Problema
Em microsserviços, uma operação de negócio (ex: criar um pedido) geralmente envolve várias etapas em serviços diferentes:
- Reservar estoque  
- Processar pagamento  
- Enviar confirmação  

Se uma das etapas falhar, é necessário **desfazer as operações anteriores** para manter a consistência.  
Como cada serviço tem seu próprio banco de dados, não existe uma transação distribuída única que cubra tudo.

#### Solução com Saga
O Saga divide a transação em uma **sequência de transações locais**.  
Cada transação local:
1. Executa no seu próprio serviço.
2. Publica um **evento** ao completar.
3. Caso ocorra falha, executa uma **transação compensatória** (rollback lógico).

#### Abordagens

##### 1. Orquestrada
- Existe um **orquestrador central** (um serviço que controla o fluxo).
- Ele chama os serviços participantes na ordem correta.
- Se algo falhar, ele aciona as compensações.

**Vantagem:** controle centralizado, mais simples de gerenciar.  
**Desvantagem:** pode se tornar um ponto único de falha.

**Exemplo de fluxo:**
```
Orquestrador → Serviço de Pedido → Serviço de Estoque → Serviço de Pagamento
```

##### 2. Coreografada
- Não há orquestrador central.
- Cada serviço **escuta eventos** e reage com sua própria lógica.
- Em caso de falha, publica eventos de compensação.

**Vantagem:** sistema descentralizado, mais resiliente.  
**Desvantagem:** fluxo mais difícil de rastrear e depurar.

**Exemplo de fluxo:**
```
PedidoCriado → [Estoque reserva] → Evento "EstoqueReservado"
              → [Pagamento processa] → Evento "PagamentoConfirmado"
              → [Pedido confirmado]
```

#### Exemplo prático

##### Criar pedido (Saga Orquestrada)
1. Orquestrador inicia Saga.
2. Serviço de **Pedido** cria o pedido.
3. Serviço de **Estoque** reserva itens.
4. Serviço de **Pagamento** processa o pagamento.
5. Orquestrador finaliza Saga.

Se o pagamento falhar:
- Orquestrador aciona o serviço de **Estoque** para liberar reserva.
- Orquestrador aciona o serviço de **Pedido** para cancelar.

#### Vantagens
- Maior **consistência eventual** entre serviços.
- Evita dependência de 2PC (não escalável).
- Flexível para cenários distribuídos.

#### Desvantagens
- Maior **complexidade de implementação**.
- Fluxos de compensação precisam ser cuidadosamente projetados.
- Depuração pode ser difícil, principalmente em coreografia.

#### Quando usar
- Em sistemas de **microsserviços** com operações de negócio que envolvem múltiplos contextos/bancos.  
- Quando **consistência eventual** é aceitável.  
- Em processos longos (ex: pedidos, pagamentos, reservas).

## Acesso a dados

- Muitas vezes, dados precisam ser recuperados a partir de diversos serviços e bancos de dados distribuídos em servidores distintos

- Como resultado, não é mais fácil implementar consultas que associam dados de vários serviços

- Múltiplas chamadas de rede podem tornar o desempenho de relatórios pesados inviáveis

- O padrão arquitetural CQRS pode ser usado para lidar com essa situação

### CQRS

O **CQRS** é um padrão arquitetural que separa a responsabilidade de **leitura** (Queries) e **escrita** (Commands) em modelos distintos.  
Ele é muito usado em sistemas complexos, principalmente quando combinados com **DDD (Domain-Driven Design)** e **Event Sourcing**.

#### Problema
Na maioria das aplicações tradicionais (CRUD), o mesmo modelo de dados é usado para:
- **Ler informações** (ex: buscar detalhes de um pedido).
- **Modificar informações** (ex: criar, atualizar ou excluir um pedido).

Isso gera alguns problemas em sistemas complexos:
- O modelo de escrita (normalizado) pode não ser eficiente para leitura.
- Regras de negócio e consultas ficam misturadas, aumentando a complexidade.
- Dificuldade em escalar separadamente leitura e escrita.

#### Solução com CQRS
O CQRS propõe **separar os modelos**:
- **Command Model (Escrita):** usado para modificar o estado da aplicação.  
  - Aplica **regras de negócio**.
  - Não retorna dados, apenas confirmações (ex: sucesso/falha).
- **Query Model (Leitura):** usado para consultas.  
  - Otimizado para leitura (pode ser desnormalizado, cacheado, ou até em outro banco).
  - Nunca altera o estado.

#### Fluxo Simplificado

##### Escrita (Command)
1. O cliente envia um **Command** (ex: CriarPedido).
2. O **Command Handler** processa o comando, aplicando as regras de negócio.
3. O estado é atualizado no banco de escrita.
4. (Opcional) Um evento é publicado para sincronizar a base de leitura.

##### Leitura (Query)
1. O cliente envia uma **Query** (ex: ObterPedidosPorCliente).
2. O **Query Handler** consulta diretamente o modelo de leitura.
3. Retorna os dados de forma rápida e otimizada.

#### Exemplo
##### Sem CQRS (CRUD tradicional):
```sql
-- Um único modelo para leitura e escrita
SELECT * FROM Pedidos WHERE ClienteId = 123;

INSERT INTO Pedidos VALUES (...);
```

##### Com CQRS:
- **Command:** CriarPedido → validações → salva no banco de escrita.  
- **Query:** ObterPedidosPorCliente → busca em um modelo de leitura desnormalizado.  

#### Vantagens
- Separação clara entre **leitura e escrita**.
- Possibilidade de otimizar cada modelo para seu caso (ex: leitura desnormalizada).
- Escalabilidade independente (ex: múltiplas réplicas de leitura).
- Facilita a adoção de **Event Sourcing**.

#### Desvantagens
- Maior complexidade de implementação.
- Necessidade de sincronizar os modelos de leitura e escrita (eventual consistency).
- Não é necessário para sistemas simples (pode ser overengineering).

#### Quando usar
- Sistemas complexos com alta demanda de **leitura e escrita**.
- Quando é preciso escalar leituras e escritas de forma independente.
- Cenários que combinam com **DDD** e **Event Sourcing**.
- Casos onde o modelo de leitura é muito diferente do de escrita.