# Versionamento de APIs

- A lógica de negócio de uma aplicação ou os recursos disponíveis podem sofrer alterações com o tempo

- Isso acaba refletindo na API desta aplicação

- Para garantir que os clientes tratem estas mudanças adequadamente, é fundamental controlar o número da versão da API e refletir isso na forma de acesso garantindo o uso correto das funcionalidades disponíveis

- Diante disso, existem duas questões que precisamos entender
    1. Como numerar novas versões?
    2. Como refletir os novos números na forma de acesso?

- Para especificar a versão de uma API é comum utilizar a URL de acesso ou, ainda, cabeçalhos HTTP

    - Via URL
        - Domínio do site 
        - Caminho do recurso 
        - Parâmetro na query string

    - Via cabeçalho HTTP
        - Cabeçalho Accept
        - Cabeçalho Customizado

- Versionamento Semântico
    - {Versão Maior}.{Versão Menor}.{Patch}
    - Versão Maior
        - Possível quebra de compatibilidade
    - Versão Menor
        - Compatibilidade retroativa
        - Funcionalidade depreciada, mas funcional
        - Refatoração interna
    - Patch
        - Correção de bugs
