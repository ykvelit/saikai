# Requisitos Arquiteturais

## Requisitos de negócio

- Coração do problema
- Visão do projeto
- Restrições de projeto
- Objetivo de negócio
- Escopo do projeto
- Análise do processo de negócio
- Pessoas envolvidas
- Serviços/Departamentos de TI

- Tipos de requisitos
    - Requisitos funcionais
    - Requisitos não funcionais
        - Disponibilidade
        - Continuidade de negócio
        - Compliance
        - Interoperabilidade
        - Mantenabilidade
        - Performance
        - Usabilidade

## Dimensionalidade dos dados

- A dimensionalidade de dados refere-se ao número de atributos ou características (também chamados de features) que cada ponto de dados possui

- Dados com alta dimensionalidade trazer vários desafios, entre eles
    - Complexidade computacional
        - Mais dimensões significam mais cálculos, o que pode aumentar o tempo de processamento
    
    - Maldição da dimensionalidade
        - À medida que o número de dimensões aumenta, o volume do espaço de dados cresce exponencialmente, tornando mais difícil encontrar padrões significativos

    - Maldição da dimensionalidade
        - Modelos treinados de machine learning com muitos atributos podem se ajustar muito bem aos dados de treinamento, mas falhar em generalizar para novos dados

- Considerar apenas os atributos necessários para satisfazer os requisitos de negócio

- Equilíbrio na criação de entidades, seus atributos e relacionamentos

## Ingestão e integração de dados

- Serviço produtor
    - Arquivos não estruturados
        - Áudio
        - Vídeo
    - Arquivos estruturados/semiestruturados
    - Bases de dados relacionais
    - Bases de dados No SQL
    - Envio de dados por demanda
        - API
        - GraphQL
    - Envio de dados por eventos
        - Pub/Sub
        - Fila
    - Processos de ingestão de dados para Data Lake/Data Warehouse

- Plataforma de dados
    - Ingestão
    - Producer
        - Repositório por camadas
        - Processamento
    - Consumer
        - Envio de dados por evento
        - Envio de dados por demanda
    
- Serviço consumidor
    - Arquivos não estruturados
        - Áudio
        - Vídeo
    - Arquivos estruturados/semiestruturados
    - Bases de dados relacionais
    - Bases de dados No SQL
    - Recebe dados por demanda
    - Recebe dados por eventos
    - Recebe dados de plataforma de dados

## Processamento e armazenamento de dados

- Sistema Transacional / App / Serviço
    - Tipo de dados gerados ?
        - Formulário
        - Texto 
        - Chat
        - Imagem
        - Vídeo
        - Audio
        
    - Destinatário dos dados e forma de interação ?
        - Unilateral
        - Bilateral
        - B2C
        - B2B
    
    - Volume dos dados, frequência de consulta e disponibilização ?

    - Arquivos não estruturados
        - Áudio
        - Vídeo
    - Arquivos estruturados/semiestruturados
    - Bases de dados relacionais
    - Bases de dados No SQL

- Ingestão
    - Dados são disponibilizados em tópicos ou filas ?
    - Existem apenas em banco de dados relacionais ou NoSQL ?
    - Estão disponíveis apenas em arquivo ?

    - API
    - GraphQL
    - ELT
    - PUB/SUB
    - CDC

- Armazenamento
    - Dados são apenas incrementais?
    - Preciso processar retroativos ou atualizar dados dimensionais?
    - Preciso consultar muitos dados no detalhe ou dados consolidados?

    - Orientado ao evento
        - PARQUET 
        - ORC
    
    - Orientado ao registro
        - Open Table Iceberg
        - Delta Table
    
    - Orientado ao negócio
        - Banco de dados colunar

- Processamento
    - Quando o dado consolidado deve estar disponível?
    - Que informações preciso para consolidar o dado e onde estão disponíveis?
    - Quem vai consultar o dado consolidado e com qual frequência?

    - Processamento por batch (Jobs Spark por exemplo)
    - Processamento NRT (Streaming)

## Governança, acessos e segurança de dados

- Processos
- Políticas e diretrizes
- Papéis e responsabilidades
- Acessos
- Autenticação e compartilhamento
- Perfis e roles
- Segurança
- Aderência às leis e regulamentos (LGPD, HIPAA, SBIS, DORA)
- Dados sensíveis, encriptação e expurgo de dados
- Aplicação das políticas e diretrizes em pipeline
- Monitoramento e alertas
- Auditoria interna e externa
