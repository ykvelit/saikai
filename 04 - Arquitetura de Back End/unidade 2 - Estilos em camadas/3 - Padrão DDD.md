# Padrão DDD

- Domain Driven Design
- Grande utilização de orientação a objetos
- Manutenabilidade
- Testabilidade
- Acoplamento de regras de negócio, persistências e detalhes técnicos tornaram o código ruim
- Separação entre analista de negócio e desenvolvimento
    - Comunicação truncada
- Ferramenta de comunicação manifestada em código para todos
- Organizar o código de forma clara para ser mantido, entendido e evoluido
- Abordagem para o desenvolvimento de software que enfatiza a importância do domínio central e da lógica de domínio
- Envolve a criação de abstrações de software chamadas de modelos de domínio que encapsulam lógica de negócios complexas e vinculam as condições reais do aplicativo de um produto ao código
- O DDD também defende a modelagem baseada na realidade dos negócios como relevante para os casos de uso e descreve áreas problemáticas independentes como contextos limitados, cada um dos quais se correlaciona com um microsserviço
- Organizar grandes domínios em pequenos domínios autonomos
- O objetivo do DDD é criar sistemas ideais de objetos por meio de uma colaboração criativa entre especialistas técnicos e de domínio para refinar iterativamente um modelo conceitual
- A linguagem ubíqua no DDD é uma linguagem comum e compartilhada entre todas as pessoas envolvidas no desenvolvimento do software, incluindo desenvolvedores, especialistas de negócio e outros stakeholders
    - Essa linguagem é composta de termos e conceitos específicos que representam os conceitos do domínio da aplicação
- Além de ser um padrão arquitetural, é também uma forma de manter a comunicação clara entre os envolvidos no projeto

## Camadas

### Dominio

- Negócio
- Ela é responsável por representar conceitos, informações e situações referentes aos negócios
- O estado que reflete a situação de negócio é controlado e usado aqui, embora os detalhes técnicos sobre como armazená-lo sejam delegados a infraestrutura
- Essa camada é a essência de negócio do software sendo construído

### Infraestrutura

- Persistência
- Integração com outros sistemas
- Auditoria
- Mantém a lógica técnica do produto, tais como persistência, segurança da informação, interoperabilidade e outros temas técnicos
- Organiza os repositórios com a lógica específica de persistência de dados

### Serviço

- Coordenação e mediação utilizando o domínio e a infraestrutura
- Fornece uma visão dos serviços da aplicação
- Aqui são implementadas fluxos de trabalho e regras globais ao sistema
- Essa camada também usa o domínio para persistir informações contra os bancos de dados

### Aplicação

- Coordenação e apresentação das camadas
- Ponto de entrada 
- Responsável pelo projeto principal
- Aqui serão implementados os controladores e a exposição de APIs
- Tem a função de receber todas as requisições e direcioná-las a algum serviço para executar uma determinada ação
