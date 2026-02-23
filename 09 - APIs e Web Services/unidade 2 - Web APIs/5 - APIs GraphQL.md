# APIs GraphQL

- GraphQL é uma linguagem de consultas para dados em grafos e um ambiente que executa operações nos dados voltada para a criação de APIs

- Endpoint único ao invés de diversas entradas como no padrão REST
- Independente de linguagem, protocolo ou framework
- Maior controle do cliente via linguagem de consulta (Graph Query Language)
- Acabar com o Overfetching e o Underfetching
- Redução do trafego de dados e o número de requisições
- Reduz a necessidade de manutenções de uma API

## Conceitos importantes

### Schema

- Especificação de uma API GraphQL, escrita em uma linguagem denominada Schema Definition Language (SDL)
- Estabelece os tipos de dados possíveis de serem em uma API baseada em GraphQL 
- Define as operações de consulta (Queries) e alteração  (Mutations)disponíveis no serviço que oferece a API GraphQL

### Tipos

- Tipo Objeto
    - Type define um objeto, o elemento mais básico do Schema GraphQL

- Tipos escalares
    - String 
        - Para propriedades baseadas em texto (UTF-8)
    - Integer
        - Para propriedades numéricas
    - Float
        - Para propriedades numéricas com uma parte decimal
    - Boolean
        - Para propriedades binárias de um objeto (true ou false)
    - ID
        - Unique identifiers 
        - Para descrever um identificar único para um objeto São serializadas com strings, porém possuem tratamento diferenciado

- Tipos enumerados
    - Tipo especial restrito a um conjunto particular de valores

- Listas
    - Definidas por meio do modificador de colchetes [ e ]

- Tipo Query
    - Operações disponíveis em uma API GraphQL que permitem obter dados do servidor

- Mutation
    - Operações disponíveis em uma API GraphQL que permitem modificar os dados no servidor e recuperar os dados modificados

- Resolvers
    - Funções que implementam a lógica por traz das queries e mutations definidas no Schema de um serviço
    - Cada campo no Schema, deve ter um resolver correspondente que implementa o que é necessário para buscar os dados ou executar ações relacionadas
