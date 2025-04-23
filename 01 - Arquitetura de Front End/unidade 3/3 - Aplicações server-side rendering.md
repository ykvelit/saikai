# Aplicações Server-Side Rendering

- Até antes de 2010, todas as aplicações web dinâmicas eram server-side rendered
    - PHP
    - ASP.NET MVC
    - Java Server Pages
- Grande mudança causada pelo AngularJS
- Em cada uma das requisições, o servidor é o responsável por devolver a página completa ao usuário, pois elajá foi pré-processada
- Regras de negócio na mesma base de código da camada de apresentação
- Roteamento de URLs direto no servidor

## Vantagens

- Search Engine Optimization (SEO)
    - Páginas já que possuem o HTML semântico nos resultados de busca
- Performance e Time to Interactive (TTI)

## Pontos de atenção
- Algumas arquiteturas de server-side rendering estão em desuso
- Separação das responsabilidades pode ser mais difícil
- Dificuldade de componentização e reaproveitamento de códigos de interface

## Bibliotecas

- Nextjs
- nest
- Nuxtjs
- Gatsby

## SSR + React

- Next.js
- Aplicação é pré-renderizada no servidor, somente pela primeira vez
- Navegação subsequentes utilizam o "efeito SPA"
- Melhor desempenho em mecanismos de buscas
    - Requisições feitas nas URLs retornam a página HTML com conteúdo completo pré-renderizado
- Possibilidade de usar todos os conceitos de componentização presentes no React
- Sistemas de rotas baseado na estrutura de pastas
- Possibilidade de criar funções serverless
    - Estilo AWS Lambda ou Azure Functions
- Possibilidade de executar funções de servidor
    - Envio de e-mails
    - Requisição em APIs com chaves privadas
- [Demo](https://codesandbox.io/s/cold-water-9tb3k)

## Gatsby

- JAMStack
    - Javascript, Api e Markup
- Utilização de SSR para criação de Static Site Generator (SSG)
- Utilização de React para criação das páginas e componentes
- Principais linhas de utilização
    - Criação de landing pages
    - Criação de blogs pessoais
- Comunidade
    - Bem madura, com boa utilização principalmente em projetos pessoais de baixo custo
- Flexibilidade
    - Personalização total dos recursos disponíveis
    - Grande showcase de starter projects para iniciar a sua aplicação
- Hospedagem simplificada
    - No caso de blogs pessoais, as postagem são armazenadas juntamente com o código, evitando a contratação de um espaco em banco
- GraphQL
    - Utilização da linguagem de query para listagem dos posts em arquivos
- [Demo](https://codesandbox.io/s/gatsby-example-meu18)
- [Starters](https://www.gatsbyjs.com/starters/)