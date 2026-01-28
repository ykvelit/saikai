# DW, Datalake, ETL e ELT

## Data Warehouse

- Data Lake é uma metodologia de armazenamento, processamento e disponibilização de dados tendo como principais objetivos
    - Atender a consultas complexas de  Analytics e BI
    - Dados estruturados em bancos relacionais
    - Estruturado por métricas e dimensões
    - Ingestão de dados por ETL

- Fonte de dados
    - Sistemas transacionais ou operacionais
    - Arquivos estruturados de dados
    - Logs estruturados

- Staging
    - Área onde os dados são armazenados para entrada no DW
    - Ingeridos por ETL
    - Ainda não estruturados dimensionalmente
    - Guardados em tabelas não relacionadas

- Warehouse
    - Dados armazenados em modelo dimensional, em estrela ou Snowflake
    - Guardados no seu nível de granularidade mais baixo

- Data Marts
    - Dados também modelados de forma dimensional
    - Agregados ou consolidados em granularidade mais alta (semana, mês, total loja, etc)
    - Métricas já calculadas para representar indicadores de negócio

- Consumo 
    - Dados são consultados no DW para compor relatórios ou dashboards
    - Dados são por vezes integrados com outros sistemas de gestão estratégica
    - Dados podem ser usados em apresentações, indights e abordagens de story telling

## Data Lake

- O data lake é um repositório centralizado projetado para armazenar, processar e proteger grandes quantidades de dados estruturados, semiestruturados e não estruturados:
    - Estruturado por camadas
    - Pode ter diferentes tipos de modelagem
    - Muito usado como fonte de ciência de dados e ML
    - Dados inseridos por processos de ELT

## Data Lake House

- Os Data Lake Houses permitem que estruturas e esquemas como os usados ​​em um Data Warehouse sejam aplicados aos dados não estruturados do tipo que normalmente seria armazenado em um Data Lake

- Dados estruturados, semi-estruturados e não estruturados

- Guardados por camadas com ingestão ELT

- Organizados e apresentados de forma dimensional sem precisar reprocessamento dos dados. Com representação de metamodelos de dados


## ETL e ELT

### ETL

- Extract, Transform and Load
- Os dados são extraídos da fonte
- É filtrado e transformado na ingestão
- Depois é carregado e armazenado no repositório

### ELT

- Extract, Load and Transform

- Os dados são extraídos da fonte
- É carregado e armazenado no repositório
- Depois é filtrado e transformado na ingestão

