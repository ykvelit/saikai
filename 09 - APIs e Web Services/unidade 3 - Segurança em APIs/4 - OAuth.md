# OAuth

- Open Authorization

- Framework aberto definido pelo IETF (RFC 6749) com foco na autenticação e autorização de recursos na Web

- Evita exposição de senhas

- Baseado no uso de token e autenticação Bearer

- Facilita a interoperabilidade 
    - Web, Mobile e Server

- Controla a validade e o escopo do acesso concedido

## Papéis

- Dono do recurso
    - Entidade que possui recursos na rede e pode ser solicitado a autorizar o acesso a estes recursos protegidos
    - Ex: Usuário final

- Aplicação Cliente
    - Aplicações utilizadas para acessar recursos na rede. Podem ser confidenciais ou públicos
    - Ex: aplicações móveis e sites na Web

- Servidor de Autorização
    - Sistema que controla a geração de tokens de acesso para as aplicações cliente
    - Ex: Google Accounts

- Servidor de Recursos
    - Sistema que mantém recursos na Internet e pode fornece tais recursos por autorização do dono
    - Ex: Google Photos

## Access Token

- O Access Token é uma credencial para acesso a um recurso protegido

- Trata-se de uma string em formato específico de acordo com a aplicação em questão

- Uma Access Token é obtida de acordo com o tipo de autorização

- A Access Token substitui a necessidade de usuário e senha

## Tipos de Autorização

- Authorization Code
    - Código de Autorização 
    - Aplicação Cliente é uma aplicação Web ou nativa e mantém uma chave secreta
    - Ex: Site X acessa seus dados no facebook

- Implicit Grant
    - Autorização Implícita 
    - Aplicação Cliente é baseada no browser e não pode manter uma chave secreta.
    - Ex: Aplicações SPA (Single Page Web)

- Resource Owner Password Credentials
    - Credenciais do Usuário 
    - Aplicação Cliente é próxima do Servidor de Autorização e requer usuário e senha, normalmente, ambos feitos pela mesma empresa
    - Ex: Aplicativo "Gerenciador de Negócios" do facebook

- Client Credentials
    - Credenciais do Cliente 
    - Aplicação Cliente é a proprietária dos recursos e não o usuário final
    - Ex: Cloud Azure acessando dados em storage interno