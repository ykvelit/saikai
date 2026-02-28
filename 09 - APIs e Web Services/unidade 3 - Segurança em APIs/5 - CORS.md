# CORS

- Cross Origin Resource Sharing

- CORS é um mecanismo de segurança sobre HTTP que permite páginas de um site A acessarem recursos de um site B

- A política de mesma origem (same-origin) restringe sites de acessarem recursos apenas no servidor em que está hospedado, evitando que códigos maliciosos usem chamadas AJAX para repasse de informações em uma sessão aberta

- O CORS define dois tipos de requisições
    - Requisição Simples
        - Métodos
            - GET
            - HEAD 
            - POST
        - Cabeçalhos permitidos
            - Accept
            - Accept-Language
            - Content-Language
            - Content-Type 
                - Apenas para valores como application/x-form-urlencoded, multipart/form-data, text/plain
            - Connection
            - User-Agent
        - Requisições permitidas

    - Requisição Preflighted 
        - Métodos
            - GET
            - HEAD
            - POST
            - PUT
            - DELETE
        - Cabeçalhos permitidos
            - Demais cabeçalhos
        - Requer verificação de acesso via método OPTIONS

- É possível desabilitar o controle de same-origin feito pelo browser enquanto estiver fazendo testes de desenvolvimento