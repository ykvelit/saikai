# Implementação de APIs

- Application Programming Interface (API)
- No contexto de API, aplicação refere-se a qualquer software
- Interface
    - Contrato definido entre duas aplicações
    - Esse contrato define a forma como as aplicações se comunicam

- No caso de uma API REST, a comunicação se dá através de chamadas HTTP
    - O cliente envia uma solicitação ao servidor, através de um verbo HTTP
    - O servidor processa essa solicitação e devolve uma resposta ao cliente

- O Node.js oferece um conjunto de métodos para implementação de APIs em HTTP de forma nativa, ou através de bibliotecas prontas, como:
    - Express
        - Biblioteca que configura um servidor HTTP juntamente com a possibilidade de expor uma API REST
    - Nestjs
        - Framework que abstrai o Express criando dando a possibilidade de implementarmos arquiteturas robustas e escaláveis, como microserviços, modularização e etc