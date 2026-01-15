# Conceitos e princípios de arquitetura de dados

## O que é uma arquitetura de dados ?

- Conjunto de modelos, desenhos, regras e artefactos que definem padrões para todos dados, sua estrutura, governança e operação

- Clico de vida do dado
    - Captura e ingestão do dado
    - Integração e movimentação
    - Limpeza, consistência e armazenamento
    - Processamento
    - Gestão da qualidade dos dados e metadados
    - Gestão de acessos e dados sensíveis
    - Disponibilização, apresentação e consumo

- Estutura organizacional
    - Papéis e competências
    - Metodologias de trabalho
    - Papéis e responsabilidades

- Evolução e operação
    - Gerenciamento
    - Governança
    - Operação e evolução
        - DataOps
        - MLOps
    - Monitoramento e alarmística
    - Plano de escalada e atuação

## Que tipos de arquitetura de dados existem ?

- Gerenciamento
- Governança
- Segurança

### Integração e comunicação de sistemas transacionais

- Consideram os sistemas que representam os processos e operação do dia a dia
- Sistemas monolito
- Sistemas orientados a microsserviços
- IoT
- On-premise
- Cloud: single ou multi cloud

### Plataforma de dados

- Local de armazenamento de dados
- Data Warehouse
    - Forma de armazenar os dados quando eles são muito relacionais
    - Banco de dados
    - ETL
- Data Lake
    - Forma de armazenar dados não estruturados e relaciona-las
    - Dividido em camadas
- Data Lake House
    - Combina a estratégia de Data Lake com uma entrega mais orientada ao analítico com estruturas de indicadores e que podem ser consumidas por dashboards

### Apresentação | Story Telling | Suporte à tomada de decisão

- Como disponibilizar os dados e o contexto que serão apresentadas
- Dashboarding
- Self Service BI
- Disponibilização para outros sistemas

### Inteligência Artificial | Ciência de dados | Machine Learning

- Consumo de grande volume de dados
- Exploração de dados e construção de modelos
- Feature Store
- Treinamento e otimização
- Modelo de scoring/inferência
- MLOps - Operação e evolução dos modelos

### Estrutura organizacional dos times e suas metodologias

- Organização centralizada
- Data Mesh
- Data Fabric

## Quem são os profissionais envolvidos no gerenciamento de dados ?

- CDO
    - Chief Data Offer
    - Executivo responsável pela estratégia de dados
    - Lidera os times todos os times de desenvolvimento e operações da companhia

- Líder de dados
    - Responsáveis pela execução tática de desenvolvimento e/ou operações de dados
    - Líderes de cada um dos times de dados da companhia
    - Podem ser líderes de desenvolvimento de operações ou de engenharia, BI, ciência de dados, etc.

- Engenheiro de dados
    - Responsáveis pelo desenvolvimento e operação das pipelines de ingestão, processamento e limpeza de dados
    - Devem conhecer bastante de Data Lake, DW e Data Lakehouse
    - Dominam técnicas e ferramentas de big data

- Analista de dados
    - Especialistas nas suas áreas de negócio mas conhecem também as técnicas e ferramentas de ingestão e processamentos de dados
    - Responsáveis por definir indicadores junto do negócio e desenvolver dashboards
    - Devem conhecer técnicas de Storytelling

- Cientista de dados
    - Especialistas em exploração de dados
    - Dominam estatística e modelagem de machine learning e inteligência artificial
    - Responsáveis por trazer insights e tendências para a companhia com base nos dados
    - Desenvolvem modelos preditivos e prescritivos

- Engenheiro ML/AI
    - Responsáveis pela produtização dos modelos de machine learning e/ou inteligência artificial desenvolvidos pelos cientistas de dados
    - Colocam esses modelos em ambiente produtivo na plataforma de dados e são responsáveis pelo sua operação e monitoramento

- Curador de dados
    - Responsáveis pela governança dos dados
    - Constroem e operação os catálogos de dados da companhia
    - Verificam e atuam junto com os restantes profissionais para garantir que dados sensíveis estão acessíveis apenas pelos pelas pessoas certas e apoiam no acesso correto de todos os dados

- Arquiteto  de dados
    - Responsáveis por determinar o modelo transversal de atuação dos times e ferramentas
    - Manter a consistência das componentes, sistemas e ferramentas que compõem as soluções de dados da companhia
    - Identificar novas tendências e ferramentas para uma melhoria de toda a plataforma
