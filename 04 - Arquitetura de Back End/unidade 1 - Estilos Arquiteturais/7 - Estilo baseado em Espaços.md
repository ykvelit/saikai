# Estilo baseado em Espaços

- O estilo arquitetural baseado em espaços (Space-Based Architecture – SBA) é uma abordagem projetada para eliminar gargalos de banco de dados e permitir escalabilidade linear em sistemas distribuídos de alta performance. A ideia central é tratar os dados e os componentes de aplicação como objetos armazenados e acessados em um “espaço” compartilhado de memória distribuída.

## Principais Características
- Grid de Dados em Memória
    - Os dados são mantidos em caches distribuídos (data grid), reduzindo latência de acesso e aliviando o banco de dados tradicional.

- Unidades de Processamento
    - Cada instância da aplicação (processing unit) contém lógica de negócio e mantém seu próprio cache local, lendo e escrevendo no espaço de dados.

- Desacoplamento pelo Espaço
    - Produtores e consumidores de dados interagem indiretamente via operações no espaço (e.g., write, read, take), sem conexão ponto-a-ponto.

- Escalonamento Dinâmico
    - É fácil aumentar ou diminuir o número de nós de processamento conforme a carga, sem impacto significativo na consistência eventual.

- Grid de Mensagens (Opcional)
    - Para comunicações de pub/sub ou eventos, pode-se integrar um broker leve ou usar mecanismos internos do espaço.

## Vantagens

- Escalabilidade Linear
    - Adicionar novas instâncias escala throughput quase que diretamente proporcional ao número de nós.

- Alta Disponibilidade e Resiliência
    - Replicação de dados e fail-over automático de unidades de processamento evitam pontos únicos de falha.

- Baixa Latência
    - Acesso a dados em memória torna operações de leitura/escrita extremamente rápidas.

- Simplicidade de Desdobramento
    - Deploy de novas instâncias é trivial, já que não há dependências centralizadas além do espaço de dados.

## Exemplos de Aplicação

- E-commerce com picos de acesso (Black Friday, lançamentos)
- Plataformas de trading em tempo real
- Sistemas de publicidade RTB (Real-Time Bidding)
- Jogos multiplayer com estado compartilhado

## Tecnologias Comuns

- GigaSpaces XAP
- Hazelcast IMDG
- Oracle Coherence
- Redisson (Redis como data grid)
- Apache Ignite