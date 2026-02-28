# Autenticação no protocolo HTTP

- Processo para verificar a identidade do usuário de uma aplicação Web

- Esquemas de Autenticação
    - Usuário Anônimo + Forms da aplicação (Login)
    - Autenticação Basic
    - Autenticação Digest
    - Autenticação Bearer (Token Authentication)

## Autenticação HTTP - Basic

- Tela de login exibida pelo próprio browser e envio de string codificada em Base64 com  informação de usuário e senha

- Recomenda-se utilizar apenas com conexões HTTPS

- WWW-Authenticate
    - Cabeçalho da resposta que exige o envio de dados de autenticação

- Realm
    - Definição do espaço protegido pela autenticação

- Authorization
    - Cabeçalho da requisição que leva os dados de autenticação do cliente

- Base64
    - Algoritmo de codificação de dados para a Internet

## Autenticação HTTP - Digest

- Cliente e servidor não trocam informações de senha, apenas o hash

## Autenticação HTTP - Bearer

- Cliente e servidor trocam um token previamente acordada

- Recomenda-se utilizar apenas com conexões HTTPS