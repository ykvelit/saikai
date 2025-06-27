# Estilo baseado em Microsserviços

- O estilo arquitetural baseado em microsserviços é uma abordagem para desenvolvimento de sistemas onde a aplicação é dividida em múltiplos serviços pequenos, autônomos e independentes, cada um responsável por uma funcionalidade específica de negócio. Esses serviços se comunicam entre si, geralmente por meio de APIs leves (como REST ou mensagens assíncronas).

## Principais Características

- Serviços pequenos e focados
    - Cada microsserviço tem uma responsabilidade única e bem definida (princípio Single Responsibility).

- Desenvolvimento e deploy independentes
    - Equipes podem desenvolver, testar e implantar microsserviços de forma isolada, reduzindo o acoplamento.

- Escalabilidade específica
    - Cada serviço pode ser escalado separadamente, conforme sua demanda.

- Comunicação por rede
    - Os serviços interagem por protocolos como HTTP/REST, gRPC ou mensageria (RabbitMQ, Kafka).

- Resiliência e tolerância a falhas
    - Arquitetura preparada para falhas localizadas sem comprometer o sistema inteiro.

## Vantagens

- Agilidade no desenvolvimento
    - Equipes menores podem evoluir serviços rapidamente e com mais autonomia.

- Manutenção facilitada
    - Mudanças em um serviço não impactam diretamente outros, desde que as interfaces sejam mantidas.

- Adoção de tecnologias diversas
    - Cada microsserviço pode ser desenvolvido com a linguagem, banco de dados ou tecnologia mais adequada.

- Escalabilidade e alta disponibilidade
    - Serviços críticos podem ter mais instâncias ou políticas específicas de tolerância a falhas.

## Desafios

- Complexidade de comunicação
    - Gerenciar a comunicação entre múltiplos serviços requer infraestrutura robusta.

- Gerenciamento distribuído
    - Necessita de soluções para log centralizado, rastreamento de chamadas (traceability) e monitoramento.

- Consistência de dados
    - Muitas vezes usa-se consistência eventual, com padrões como Eventual Consistency e Sagas.

## Exemplos de Aplicação

- Sistemas com múltiplos domínios de negócio (ex: e-commerce, plataformas bancárias)
- Aplicações que precisam escalar partes específicas
- Ambientes com DevOps e entrega contínua (CI/CD)

## Tecnologias Comuns

- API Gateways
    - Kong, Ocelot, NGINX
- Mensageria/Eventos
    - Kafka, RabbitMQ
- Descoberta de Serviços
    - Consul, Eureka
- Containers e Orquestração
    - Docker, Kubernetes
- Observabilidade 
    - Prometheus, Grafana, Jaeger