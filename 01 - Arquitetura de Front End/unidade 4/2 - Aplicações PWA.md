# Aplicações PWA

- Progressive Web Applications
- São aplicações baseadas na web que oferecem ao usuário funcionalidades como a possibilidade de utilização sem conexão (offline), notificações push e acesso a recursos nativos dos dispositivos móveis
- Código javascript que executa em background
- É associado a um domínio (scope)
- Gerencia as diversas páginas do escopo
- Vive mesmo após o fechamento de uma página
- Requer HTTPS para comunicação 
    - Exceção para **localhost**
- Responde à eventos
- **Manifest**
    - Metadados da aplicação

## APIs

- Service Worker API
    - Atua como proxy entre a aplicação e o servidor
- Cache API
    - Armazena os arquivos estáticos da aplicação
- Fetch
    - Requisições HTTP ao servidor/Service Worker
- Push Notifications
    - Permite interagir com o usuário
    - AppLike
- Indexed DB
    - Estrutura de dados no browser

## Padrão Arquitetural

- Application Shell
    - App Shell
- Parte comum entre páginas e área de conteúdo