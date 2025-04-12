# Arquitetura Modular

* Projetos estão sempre em evolução e crescimento
* Encontrar uma arquitetura ideal logo de cara nem sempre é possível
* Arquitetura evolutiva
    * Projeto deve ser escalável e flexível o suficiente para poder sofrer alterações no futuro
    * *last responsible moment*
* Objetivo
    * Encontrar uma arquitetura que seja agnóstica a framework
    * Que possa ser aplicada em qualquer stack
* Arquiteturas podem e devem ser adaptadas para pequenos e grandes projetos
* Divisão de uma aplicação em módulos
    * Divisão em pastas
    * UI Components
        * Componentes que contém a lógica visual e de interação com o usuário
        * Exemplos
            * Botões 
            * Menus
            * Listas
            * Cabeçalhos
            * Datepicker
    * Page Components
        * Componentes que representam uma tela e estão associados a uma rota
        * Possíveis nomes
            * Views
            * Containers
        * Exemplos
            * Página principal 
            * Página de contato
            * Listagem de produtos
            * Página de configurações
            * Página de perfil de usuário
    * Application Routes
        * Arquivo `routes.js`
        * Arquivo que contém todas as rotas daquele módulo
        * Toda nova rota deve estar associada a um componente
    * API Client
        * Necessidade de desacoplar a lógica de chamada de APIs da lógica dos componentes
        * Ponto único de contato entre a aplicação e API externa
        * Um service
    * State management
        * Compartilhamento de estados comuns entre os componentes
            * Dados do usuário logado
                * Token
                * Sessão
                * Dados de perfil
            * Tema visual e sistemas de cores
                * Dark mode
            * Filtro de elementos visuais
                * Ordenação
        * SSOT
            * Single Source of Truth
            * Lugar único onde será acessado os dados compartilhados
        * Utilização da **arquitetura flux** para gerenciamento de estados como exemplo