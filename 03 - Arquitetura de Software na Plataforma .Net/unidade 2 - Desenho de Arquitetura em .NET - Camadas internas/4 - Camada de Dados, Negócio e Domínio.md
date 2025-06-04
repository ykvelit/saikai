# Camada de Dados, Negócio e Domínio

## Como desenhar a parte de Domínio, Negócio e Dados

- Muitos softwares tem necessidade de armazenamento de dados

- Separar armazenamento de dados das regras de negócio é importante

- Encapsula complexidades para as outras camadas

- Baixo acoplamento

- Como se inicia o desenho de um software ?
    - Após entendimento com cliente
    - Após construção de artefatos
    - Após prototipagem

- Modelos
    - Guiado por dados
    - Guiado por domínio/negócio

- Programação orientada a objetos (POO)
- Diagrama de Entidade e Relacionamento

## Desenvolvimento guiado a dados

- Inicia o desenho do sistema pelo DER (diagrama de entidades e relacionamentos), pelo banco de dados

- Os próximos passos acabam seguindo o modelo de banco: domínio, serviços, etc

### Vantagens

- Velocidade de produção
- Facilidade de persistência dos dados
- Recuperação de dados simplificada (linq)

### Desvantagens

- Ancorado nos recursos do banco
- Fugindo de recursos valiosos de Orientação a Objetos
- Tendência de aumento de Acoplamento (dependência do banco)
- Controle especial das versões do banco e da aplicação

### Quando optar

- Foco em registros
- Regras de negócio mais simples

### Transaction Scripts

- DbCommand
    - SqlCommand, OracleCommand, etc
- Uso de queries para construção do DataSet
- Tipos de dados definidos no momento da consulta
- Não possui validações em tempo de compilação

- Vantagens
    - Fácil entendimento para quem conhece a linguagem SQL
    - Execução rápida, sem custo de mapeamento entre objeto e banco
    - Independência de bancos de dados: SQL, Oracle, MySql, etc
- Desvantagens
    - Dificuldade de manutenção
    - Fuga de padrões de código Orientado a Objetos

### Table Module

- DataSet Não tipado
- Uso de queries para construção do DataSet
- Tipos de dados definidos no momento da consulta
- Não possui validações em tempo de compilação

- Vantagens
    - Fácil mapeamento inicial do banco
    - Fácil manutenção
    - Grande velocidade de produção
- Desvantagens
    - Baixa performance (alto custo de transformação do DataSet e do Banco)
    - Fuga de padrões de código Orientado a Objetos

### Active Record

- Entity Framework

- Vantagens
    - Fácil mapeamento inicial do banco
    - Fácil manutenção
    - Grande velocidade de produção
    - Possibilidade de desenho Orientado a Domínio e utilização de padrões OO
- Desvantagens
    - Baixa performance (alto custo de transformação)
    - Alto custo de manutenção de banco quando o modelo Entity não o espelha, gera algum retrabalho

## Desenvolvimento guiado a domínio/negócio

- Inicia-se o desenho do sistema construindo o diagrama de classes, usualmente um projeto do tipo Class Library, com foco no negócio e comportamento; não nos dados

- O restante do projeto acaba se adaptando a este diagrama

### Vantagens

- Flexibilidade de funcionamento
- Melhor representação do negócio
- Camada de negócios mais independente (menor acoplamento)
- Menos regras de negócio fora do código-fonte(no banco de dados)
- Melhor utilização de princípios de Orientação a Objetos

### Desvantagens

- Maior complexidade na persistência de dados
- Maior complexidade de recuperação de dados
- Pode haver maior custo de transformação
- Menor capacidade de leitura direto do banco

### Quando optar

- Foco no negócio
- Negócio e regras mais complexas

### Formas de armazenar dados

#### Modelos facilitados - DataSet, Command ou Entity Framework

- Pode-se usar facilitadores e transformar manualmente, com bancos relacionais
- Modelo relacional diferente do modelo de classes
- Transformação manual entre os modelos
    - Modelo de domínio diferente do modelo de dados
    - Uma tabela pode virar um campo serializado
    - Uma classe pode ser armazenada em mais de uma tabela
    - Um registro no banco pode gerar mais de um objeto

#### Nhibernate - Mapeador Objeto-Relacional

- Mapeador flexível
- Possibilita diferença do modelo de banco para o modelo de classes
- Cabe ao programador definir as transformações

#### NoSql

- Não relacionais
- Dados menos estruturados ou esquemas flexíveis
- Melhor desempenho em alguns cenários
- Colunas, Chave-valor, Grafos ou Documentos

#### Outras formas de armazenamento

- Arquivos XML
- Arquivos de Texto
- Caches em memória
