# Pré-processadores de CSS

* Como o próprio nome diz: um pré-processador, com a capacidade de adicionar novos recursos na escrita de estilos
* Três principais ferramentas com o mesmo propósito
    * SASS
    * LESS
    * Stylus
* Permite gerar CSS baseado na linguagem do pré-processador
* Em tempo de desenvolvimento
    * Browser recebe um css
* Possibilidade de utilizar variáveis
* Permite ter uma boa escalabilidade na criação de recursos compartilhados
* Flexibilidade na criação de mixins
    * **@mixin**
    * Como se fosse uma função
    * Reutilar código
* Complexidade
    * Necessita de alguma ferramenta de build para interpretar os pré-processadores

```html
<ul class="main-nav">
    <li class="nav-item">Link 1</li>
    <li class="nav-item">Link 2</li>
    <li class="nav-item">Link 3</li>
</ul>
```
```scss
/* SASS */
$primary-bg: 'green';
$primary-color: 'white';

.main-nav {
    background: $primary-bg;

    .nav-item {
        color: $primary-color;
    }
}

@mixin tranform($property){
    -webkit-transform: $property;
    -ms-transform: $property;
    transform: $property;
}

.box { 
    @include transform(rotate(30deg));
}
```