# JWT

- JSON Web Token

- Padrão que define uma forma compacta e segura de transferência de informações baseada em tokens no formato JSON (RFC-7519), utilizado em mecanismos de autenticação e autorização

- Estrutura básica da token JWT
    - header
    - payload
    - signature
    - [header].[payload].[signature]

- Campos reservados (claims)
    - Iss (Issuer) 
        - Emissor da token JWT
    - Sub (Subject) 
        - Assunto da token
    - Aud (Audience) 
        - Identifica o público para o qual a token foi emitida
    - Exp (Expiration Time) 
        - Horário de expiração da token, a partir do qual não é mais aceita
    - Iat (Issued At) 
        - Horário em que a token foi emitida