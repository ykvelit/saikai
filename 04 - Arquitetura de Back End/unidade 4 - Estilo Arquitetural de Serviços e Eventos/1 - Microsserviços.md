# Microsserviços

- Uma forma particular de projetar aplicações de software como suítes de serviços implantáveis de forma independente

- O conceito nasce da indústria com o exemplo de modernização de legados em empresas como Netflix, Uber, Amazon, entre outras, a partir de 2009

- O conceito de populariza com a escrita do artigo de Microsserviços de James Lewis e Martin Fowler em 2015
    - https://martinfowler.com/articles/microservices.html

## Características

- Embora não exista uma definição única deste estilo arquitetural, existem certas características comuns tais como:
    - a organização em torno da capacidade de negócios
    - implantação automatizada
    - inteligência nos endpoints
    - controle descentralizado de linguagens e de bases de dados

- Arquitetura distribuída

- Os serviços são implantados e escalam de forma independente

- Cada serviço também provê uma fronteira bem definida entre os módulos, permitindo até mesmo que diferentes serviços sejam escritos em diferentes linguagens de programação. Eles podem inclusive serem administrados por times diferentes

- Serviços como componentes

- Organização em torno da capacidade de negócios

- Interfaces publicadas (APIs)

- Implantação automatizada

- Inteligência nos endpoints

- Controle descentralizado de linguagens e de bases de dados

## Razões para uso

- Aplicações com topologia monolíticas comalto custo para alterar e implantar em produção
- Servidores Web e de aplicação pesados
- Longos ciclos de mudança
- Dificuldades de implantação
- Custo de evolução do legado
- Barramentos de serviços que falharam em suas promessas

## Implantação como componentes

- Se você tem uma aplicação que consiste em diversas bibliotecas em um único processo, uma mudança em qualquer componente resulta em ter que republicar toda sua aplicação

- Uma das principais razões para usar serviços como componentes (ao invés de bibliotecas) é que serviços são publicados de maneira independente

- Mas se esta aplicação é divida em múltiplos serviços, você pode esperar que diversas mudanças em um único serviço exijam uma republicação somente no serviço alterado

- Isso não é algo absoluto, pois algumas mudanças criam alterações nas interfaces entre os serviços, mas o dever de uma boa arquitetura em microsserviços é minimizar este impacto, criando interfaces coesas e mecanismos para evolução entre os serviços

- Uma das principais razões para usar serviços como componentes (ao invés de bibliotecas) é que serviços são publicados de maneira independente

- Um componente é uma unidade de software que é substituída ou atualizada de maneira 
independente
- Na prática, tecnologias como o Docker e o Kubernetes permitem esse nível de componentização

## Interfaces publicadas

- A consequência em usar serviços como componentes é ter uma interface mais explícita. A maioria das linguagens não tem uma boa forma de definir explicitamente uma interface do tipo Published Interface
- Serviços ajudam a evitar esse problema usando mecanismos de chamadas remotas através de APIs baseadas em REST, RPC, GraphQL ou outros protocolos
- Mas usar serviços desta forma tem alguns efeitos colaterais
- Chamadas remotas são mais custosas que chamadas dentro do mesmo processo e APIs remotas precisam ser granulares, o que torna ainda mais complicado para usar
- E Se você precisa mudar as responsabilidades entre os componentes, tais mudanças de comportamento são mais difíceis de fazer do que quando você consegue ultrapassar as fronteiras entre os processos

## Governança de microsserviços

### Governança técnica tradicional

- Uma das consequências de governanças centralizadas é a tendência de padronizar tudo em uma única plataforma tecnológica

- Exemplos
    - Um único banco de dados 
    - Uma única linguagem de programação

- Limites da centralização de tecnologias
    - A experiência mostra que esta abordagem é limitada – nem todo problema é um prego, nem toda solução é um martelo
    - Por exemplo, problemas de ciência de dados tendem ser melhor resolvidos por linguagens funcionais
    - E aplicações de telemetria tendem ser melhor resolvidas por banco de dados NoSQL

### Governança técnica de microsserviços

- Times construindo microsserviços também preferem uma abordagem descentralizada

- Ao invés de usar um conjunto definido de padrões escritos em algum papel, eles preferem a ideia de escolher suas próprias linguagens e produzir ferramentas úteis que outros desenvolvedores possam usar para resolver problemas similares aos que eles têm enfrentado

- Estas ferramentas são extraídas geralmente das próprias implementações e compartilhadas com um grupo maior, algumas vezes usando modelos open sourcespúblicos

- A governança técnica descentralizada traz desafios de comunicação entre os times para que os aspectos técnicos compartilhados entre os serviços sejam equacionados

- Descentralização tecnológica em microsserviços
    - Provedores de identidade
    - API Gateway
    - Formatos de mensagens (REST/HTTP, AMQP, MQTT, STOMP) 
    - Bancos de dados e mecanismos de tratamento de dados
    - Geração de conteúdo estáticos (CDN)
    - Descoberta de serviços
    - Health Check
    - Monitoração, Loge Tracing

- A adoção de uma arquitetura de microsserviços precisa fornecer autonomia técnica para os times

- Governança técnica descentralizada é abordagem recomendada para equipes operando com microsserviços