# Estilo baseado em Serviços

- O estilo arquitetural baseado em serviços (Service-Oriented Architecture – SOA) é uma abordagem de design de sistemas onde funcionalidades são organizadas como serviços independentes e reutilizáveis, que se comunicam por meio de interfaces bem definidas, geralmente por protocolos de rede, como HTTP ou mensageria.

## Principais Características

- Desacoplamento
    - Cada serviço é autônomo e possui responsabilidades bem definidas.

- Reusabilidade
    - Serviços podem ser reutilizados em diferentes contextos e aplicações.

- Interoperabilidade
    - Comunicação entre serviços heterogêneos (escritos em diferentes linguagens ou hospedados em plataformas distintas).

- Contratos bem definidos
    - Interfaces de serviço são descritas por contratos, como WSDL (em Web Services) ou Swagger/OpenAPI (em APIs REST).

- Composição
    - Serviços menores podem ser combinados para criar serviços mais complexos.

## Vantagens

- Facilita a manutenção e a evolução de sistemas grandes.
- Promove a escalabilidade, permitindo escalar serviços individualmente.
- Favorece o reuso de funcionalidades e a integração entre sistemas legados.

## Exemplos de Aplicação

- Sistemas distribuídos corporativos
- Plataformas de microserviços (evolução do SOA com maior granularidade e automação)
- Integrações entre sistemas via APIs

## Tecnologias Comuns

- REST, SOAP, gRPC
- Message brokers (RabbitMQ, Kafka)
- Service discovery, API gateways, contratos de interface