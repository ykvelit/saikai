# GraphQL

- É uma linguagem de consulta para APIs que ganhou tração significativa recentemente
- Ela foi criada internamente pelo Facebook em 2012 e publicamente em 2015 e foi adotada desde então por provedores de API como GitHub, Yelp e Pinterest, entre outros
- O GraphQL permite que os clientes definam a estrutura dos dados necessários, e o servidor retorna exatamente essa estrutura
- Referência primária: https://graphql.org

## Vantagens

- AS APIs REST e RPC muitas vezes acabam respondendo com dados que clientes podem nunca usar
- Com o GraphQL, como os clientes podem especificar exatamente o que precisam os tamanhos dos pacotes podem ser menores
- As consultas da GraphQL retornam resultados previsíveis, dando aos clientes controle sobre os dados que são devolvidos
- O servidor define um esquema de dados com tipos aninhados
- O servidor cria um código que interpreta as requisições que enviam pacotes de dados baseados no esquema de dados, e retorna ou altera as coleções de dados necessárias
- O GraphQL permite que os clientes aninhem consultas e busquem dados de recursos em uma única solicitação. Sem o GraphQL, isso pode exigir várias chamadas HTTP para o servidor
- Isso significa que aplicativos móveis usando GraphQL podem ser rápidos, mesmo em conexões de trabalho de rede lenta
- Você pode adicionar novos campos e tipos a uma API GraphQL sem afetar as consultas existentes. Da mesma forma, depreciar os campos existentes é mais fácil
- Ao fazer análise de log, um provedor de API pode descobrir quais clientes estão usando um campo. Você pode esconder campos preteridos de ferramentas e removê-los quando nenhum cliente os estiver usando
- Com as APIs REST e RPC, é mais difícil descobrir quais clientes estão usando um campo preterido, dificultando a remoção

## Desvantagens

- Projeto do servidor GraphQL pode ser complexo para esquemas de dados muitos complexos
- Custo do processamento de operações complexas de atualizações (Mutations) pode ser um problema na escalabilidade do servidor
