# Padrão MVC

- MVC é um padrão antigo
    - 1978
    - Organização de código para frontend e backend

- Usuário > Requisição para o Controller > Requisição para o Model > Resposta para o Controller > Envio de dados para View > Resposta para o usuário

- Ordem de chamadas no MVC
    - O usuário invoca algum controlador
    - O controlador valida a requisição e seleciona o modelo a ser chamada
    - O modelo executa regras de negócio, prepara e retorna dados para o controlador
    - Controlador entrega dados para visão através de uma projeção do modelo
    - Visão desenha os dados para os clientes da aplicação

- MVC na Web
    - Controlador e modelo são do backend 
    - Visão é no frontend

- MVVM e MVP são derivações do MVC