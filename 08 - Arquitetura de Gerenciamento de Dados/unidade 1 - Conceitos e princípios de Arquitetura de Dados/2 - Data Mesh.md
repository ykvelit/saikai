# Data Mesh

## O que é Data Mesh ?

- Introduzido por Zhamak Dehghani
    - Defende que os times que trabalham os dados de forma analítica devem estar próximos das áreas do produto e do desenvolvimento
    - De um lado vamos ter o sistema operacional e muito próximo o time de analytics
    - Times descentralizados
    - Governança federada

- Arquitetura e responsáveis orientado a domínio decentralizado de dados
    - Deve ter uma arquitetura que ela seja descentralizada, com os times orientados ao domínio e que eles sejam os próprios responsáveis e tenham a responsabilidade sobre os dados daquele domínio
    - Garante escalabilidade

- Dados como um produto
    - Olhar o dado com um produto ou um serviço

- Infraestrutura de dados autônomo como uma plataforma

- Governança computacional federada

## O que são domínios de dados ?

- São áreas de informação que no seu contexto estão auto contidas
- Conseguimos trabalhar e interagir com os dados através de um grupo em que as pessoas tem um grau de especialização e dominio e trabalhar de uma forma isolada para dar continuidade e sequência e acrescentar valor aquele conjunto de dados

- Níveis de maturidade
    - Nível 0
        - Criando um time de analytics
        - Criando um repositório
    - Nível 1
        - Consultas ao Banco de Dados Operacional
    - Nível 2
        - Analisa os próprios dados
    - Nível 3
        - Analisa dados de domínios cruzando as informações
    - Nível 4
        - Publicação e venda dos dados

## Produtos de dados

- Uma entidade lógica que contem todos os componentes e processos de todos os atributos que permitem disponibilizar esse dado para que ele possa ser consumido por alguém

- É considerado como uma unidade mínima dentro de uma arquitetura

- Tipos de produtos de dados

    - Orientado a fonte
        - São aqueles que são disponibilizados com sua estrutura e modelagem mais próxima possível da modelagem da organização que o dado tem na modelagem operacional ou transacional
        - Destinado a cientistas de dados ou para análise

    - Agregador
        - Combinação de dados 
        - Dados enriquecidos
        - Machine Learning
        - CRM

    - Orientado ao consumo
        - Já estão no seu estado final para serem disponibilizados para o negócio
        - BI
        - Datasets com todos os indicadores

- Contratos de dados
    - As métricas que temos associadas a qualidade e operação 
    - Transforma elas em indicadores com metas e determina um SLA para o produto de dados
    - Determina se estamos cumprindo com o acordo de disponibilização do produto de dados

## Plataforma de dados

- Pode ser analitica ou operacional
- Considerar os diferentes niveis de abstração dentro da plataforma
- Pode ser implementado em cima de uma plataforma toda agnóstica ou numa plataforma já previamente estruturada 

## Governança Federada

- Olhar para o que são politicas, diretrizes e normas não como algo que vamos controlar de perto, mas como algo que podemos orientar e determinar para ser o mais automatizado
- A organização começa ser compostas por pessoas que representam cada um dos times de desenvolvimento e de produtos de dados
