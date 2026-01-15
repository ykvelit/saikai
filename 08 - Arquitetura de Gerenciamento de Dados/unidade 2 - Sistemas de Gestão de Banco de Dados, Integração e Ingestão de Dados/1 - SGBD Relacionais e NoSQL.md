# SGBD Relacionais e NoSQL

## O que é um Sistema de Gestão de Banco de Dados ?

- Software  responsável pelo gerenciamento de bancos de dados
- Tem como principal objetivo liberar os sistemas aplicacionais das atividades de gerenciamento de acesso, manipulação, persistência e organização dos dados

## Bancos de dados relacionais

- Dados são representados em tabelas
- Cada linha da tabela representa um registro
- Cada registro tem uma chave exclusiva que o identifica
- Cada coluna da tabela representa um atributo do registro
- Tabelas podem ser relacionadas entre si através de uma chave estrangeira

- Exemplos
    - Oracle
    - SQL Server
    - PostgreSQL
    - MySQL

## Banco de dados não relacionais ou NoSQL

- Podem processar grandes volumes de dados não estruturados e em constante mudança de maneiras diferentes de um banco de dados relacional (SQL) com linhas e tabelas

- Documentos
    - Estrutura completamente flexível. 
    - Pode ser agrupada em coleções
    - mongoDB
    - Azure Cosmos DB
    - Amazon DocumentDB

- Chave-Valor
    - Estrutura livre mas sempre referenciada por uma chave
    - Redis
    - Amazon DynamoDB

- Grafos
    - Estrutura representada por nós, arestas e propriedades
    - neo4j
    - Amazon Neptune

- Colunar
    - Estrutura organizada pelas colunas. Muito usado em Big Data
    - Google Big Query
    - Amazon Redshift
    