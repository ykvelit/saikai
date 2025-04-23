# Arquitetura em Monorepos

* Conceito arquitetural que propõe um repositório para múltiplos pacotes
* Cada pacote representa um projeto (seja um micro front-end ou um módulo)
* Isolamento de código com possibilidade de dependência entre pacotes
* Controle de versão tanto do repositório quanto dos pacotes
* Refatoração fácil de configurações globais e compartilhadas entre os os pacotes

## Ferramentas

* [Lerna](https://lerna.js.org)
    * `lerna init`
        * Cria um novo repositório com as configurações iniciais
    * `lerna publish`
        * Cria uma release dos pacotes atualizados tanto no git quanto no npm
    * `lerna run [script]`
        * Roda o script especificado em todos os pacotes que contém esse script configurado
        * `lerna run start`
* [Yarn Workspaces](https://classic.yarnpkg.com/en/docs/workspaces)

## Exemplos

* [React](https://github.com/facebook/react)