# Arquitetura de Micro Front-ends

* Maior independência entre os módulos
* Arquitetura mais agnóstica a frameworks
* Lógica pulverizada em vários projetos
* Pipeline de build, test e deploys mais rápidas
* Assim como a arquitetura de micro serviços, adiciona uma complexidade a mais no projeto

## Definições

* Baixo ou nenhum acoplamento
* Alta coesão
* Não deve assumir a responsabilidade de outro micro front-end
* Não deve interferir ou ser interferido por outro micro front-end
* Base de código independente
* Pipeline de build, test e deploy separados e independentes

## Benefícios

* Modernização da aplicação sem a necessidade de jogar tudo fora
* Aplicação agnóstica de novas tecnologias
* Possibilidade de migração gradativa do código legado
* Pipeline de build, test e deploy mais rápida e independente

## Formas de implementação

* Implementação em tempo de build
    * Através de projetos npm 
* Integração por meio de funções javascript
* Integração através de web components
    * Via de projetos npm 
    * Via javascript
* Integração via 

### Comunicação entre micro front-ends

* [Window post message proxy](https://github.com/microsoft/window-post-message-proxy)
* [Iframe Message Proxy](https://github.com/takenet/iframe-message-proxy)

## Material de apoio

* https://github.com/micro-frontends-demo
* https://martinfowler.com/articles/micro-frontends.html