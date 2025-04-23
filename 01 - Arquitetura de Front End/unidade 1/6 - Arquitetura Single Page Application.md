# Arquitetura Single Page Application

* Aplicações de uma única página
* Ao invés de recarregar toda a página, apenas a parte do conteúdo é reescrito na navegação entre telas
* Definição de uma parte comum na aplicação. Demais conteúdos (templates) são escritos como componentes e renderizados ao entrar na página
* Fluidez na navegação, uma vez que apenas parte do conteúdo é trocado nas mudanças de páginas
* Muito presente no mercado de trabalho
* Traditional Web Application / Multi-page app
    * Recarrega toda a página a cada requisição
    * Nível de servidor
    * Renderiza todo o html do lado do servidor e entrega
* SPA
    * Não recarrega a cada requisição
    * Otimização
    * Tem um único index.html e quem decide o que é carregado/montado é da aplicação
* Exemplos
    * Emails
        * Só altera a parte do email
        * Não altera o menu, cabeçalho e rodapé
    * Aplicações de áreas logadas
    * Streaming
* Carga maior em cima do browser
    * Uma vez que a máquina do usuário é a responsável por renderizar a aplicação
* Problemas com SEO
    * a aplicação é renderizada dinamicamente, após interpretação dos scripts. Isso faz com que os mecanismos de busca não consigam identificar o conteúdo da página para fazer a indexação de acordo com a busca do usuário
*  Tempo inicial de renderização um pouco maior
    * a página é aberta, uma requisição ao servidor é feita para buscar os scripts, os scripts são interpretados e só após o conteúdo é renderizado na página
* Mapeamento de componente + página. 
    * Cada página (rota) é representada por um componente que deve ser implementado
* React Router
    * Biblioteca para React com o objetivo de possibilitar a implementação de múltiplas rotas em uma aplicação
    * Recebe parâmetros via URL
    * Component-driven
        * Todas as rotas nos levam a um componente
## Integrações com API Externas

* Aplicações client-side(front-end) tratam apenas de interações com usuário
* Grande parte das aplicações corporativas irão ser construídas com base em uma arquitetura cliente-servidor 