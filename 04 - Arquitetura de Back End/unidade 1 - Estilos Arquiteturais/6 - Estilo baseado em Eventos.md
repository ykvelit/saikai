# Estilo baseado em Eventos

- O estilo arquitetural baseado em eventos (Event-Driven Architecture – EDA) é um modelo de design onde os componentes de um sistema se comunicam e reagem a eventos. Um evento é qualquer ocorrência significativa no sistema, como “pedido criado”, “pagamento aprovado” ou “usuário cadastrado”.

## Principais Características

- Desacoplamento temporal e espacial
    - Os emissores de eventos não conhecem os receptores, permitindo maior flexibilidade e independência entre os componentes.

- Assíncrono
    - A maioria das comunicações acontece de forma assíncrona, melhorando a escalabilidade e o desempenho.

- Reatividade
    - Os componentes reagem a eventos em tempo real, o que permite fluxos dinâmicos e adaptáveis.

- Mensageria
    - Utilização de mecanismos como filas, tópicos e brokers (ex: Kafka, RabbitMQ) para transporte dos eventos.

## Vantagens

- Alta escalabilidade e resiliência, pois os serviços não precisam esperar uns pelos outros.
- Permite fácil extensão do sistema, apenas adicionando novos ouvintes (consumidores) de eventos.
- Favorece a auditoria e observabilidade por meio de rastreamento de eventos.
- Ideal para sistemas distribuídos e microserviços.

## Exemplos de Aplicação

- Processamento de pedidos em e-commerces
- Sistemas financeiros com notificações e reconciliação
- Aplicações com atualização em tempo real (ex: dashboards, chats)

## Tecnologias Comuns:

- Brokers de mensagens
    - Apache Kafka, RabbitMQ, Amazon SNS/SQS

- Padrões
    - Event Sourcing, CQRS

- Protocolos
    - AMQP, MQTT, WebSocket