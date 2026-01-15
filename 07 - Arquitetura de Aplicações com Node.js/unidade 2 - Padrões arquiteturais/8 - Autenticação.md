# Autenticação

- Aplicações que requerem uma área logada precisam de um sistema sólido de autenticação

- A aplicação deve reagir conforme o usuário logado 
    - Operações de leitura e escrita

- A autenticação pode ser feita de inúmeras formas
    - Tokens
    - Sessões

# JWT

- JSON Web Token
    - RFC 7519

- JWT é um padrão aberto que define uma maneira compacta e segura de transmitir informações entre partes como um objeto JSON

- É comumente usado para autenticação e autorização em aplicativos web e APIs

- Permite que os usuários se identifiquem de forma segura e confiável sem a necessidade de armazenar informações de sessão no servidor

- O usuário envia credenciais de login para o servidor

- O servidor autentica o usuário e gera um JWT contendo informações de identificação e envia para o cliente

- O cliente armazena o JWT (em local storage ou cookies) e o envia no cabeçalho de todas as solicitações subsequentes ao servidor

- Bearer authentication (ou token authentication) é um esquema de autenticação HTTP que é gerada de forma encriptada pelo servidor e enviada ao cliente

- O cliente precisa de ter um cabeçalho chamado Authorization com a seguinte estrutura:
    - Authorization: Bearer <token> 
    - O Nestjs fornece dois recursos para gerenciamento de autenticações:   
        - AuthGuards 
        - JwtService