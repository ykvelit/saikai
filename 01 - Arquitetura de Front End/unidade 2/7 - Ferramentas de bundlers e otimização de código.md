# Ferramentas de bundlers e otimização de código

* Pipeline de desenvolvimento de código pode ser custoso
* Em um cenário com uso de uma stack simples pode ser necessárias várias ferramentas para build do código.
* Imagine a stack HTML, JS e SASS
    * Escrever HTML
        * Escrever o HTML semântico
        * Incluir manualmente todo novo arquivo JS criado
        * Incluir manualmente todo novo arquivo CSS criado
        * Mudar da abordagem de arquivos para abordagem em blco é totalmente inviável
    * Escrever JS em vários arquivos
        * Preocupação com compatibilidade entre browsers
            * Nem todos os recursos modernos estão disponíveis em versões mais antigas
        * Incluir manualmente no HTML todo novo arquivo JS criado
        * Concatenar e minificar o conteúdo de todos os arquivos manualmente
    * Escrever SASS em vários arquivos 
        * Compilar o SASS em arquivos CSS
        * Incluir manualmente no HTML todo novo arquivo CSS criado
        * Concatenar e minificar o conteúdo de todos os arquivos manualmente
* Os principais frameworks de front-end já tem essa funcionalidade embarcadas

## Bundlers

* Os bundlers foram criados para resolver justamente esse tipo de problema
* Um arquivo de configuração necessário para automatizar todas essas tarefas
* Possibilidade de customizar, a qualquer momento, as tarefas já automatizadas
* Frameworks mais novos vêm com algum bundler embutido, mas conhecendo o seu funcionamento podemos customizar e adaptar à nossa arquitetura
* Exemplos
    * Webpack
    * Rollup
    * Parcel

### Webpack

* Webpack é o bundler mais utilizado pela comunidade
* Utilizado por Angular, Vue e React
* Fera automaticamente um grafo de dependências entre os arquivos escritos
* Utiliza o conceito *"convention over configuration"*
    * Convenção ao invés de configuração
    * Exemplo
        * Sempre ter uma pasta `src` e o output será na pasta `dist`
* Por convenção, seguinido a estrutura a seguir, basta rodar o comando `webpack` na linha de comando e um arquivo `dist/bundle.js` será gerado
* Utiliza o conceito de *"loaders"*
    * Onde é possível adicionar plugins ao pipeline de build do webpack
    * Exemplos
        * sass-loader
            * Loader responsável por compilar arquivos sass em css
        * Code splitting
            * Lazy loading