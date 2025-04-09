# BEM: Block, Element e Modifier

* Block
    * header
    * container
    * menu
    * checkbox
    * input
* Element
    * ítem de menu
    * ítem de lista
    * título de cabeçalho
* Modifier
    * disabled
    * active
    * fixed
    * background cinza

```html
<nav class="main-menu">
    <ul class="main-nav">
        <li class="main-nav__item main-nav__item--is-active">Home</li>
        <li class="main-nav__item">Sobre</li>
        <li class="main-nav__item">Contato</li>
    </ul>
</nav>
``` 
```css
/* block */
.main-nav {
    margin-bottom: 10px;
}

/* element */
.main-nav__item {
    padding: 20px;
    color: black;
}

/* modifier */
.main-nav__item--is-active {
    border: 1px solid black;
}
```

* Convenção já definida para nomenclatura de classes
* Visão clara de estilos para elementos filhos
* Visão clara de estados
* Nomes de classes muito grandes
* http://getbem.com/naming