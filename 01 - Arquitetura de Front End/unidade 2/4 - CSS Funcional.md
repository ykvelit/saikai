# CSS Funcional

* Ideia de ter micro classes de CSS para compor um elemento
* Cada classe altera uma única propriedade do CSS
* Classe sempre tratam responsividade desde a concepção
* Responsividade
    * Todas as classes possuem tratamento responsivo
* Reutilizável e modular
    * Inúmeras classes prontas para serem usadas em qualquer tela
* Legibilidade
    * Ao olhar o HTML, você sabe exatamente qual será o seu estilo
* Produtividade
    * Escrever HTML é mais rápido, pois diminui a necessidade de criar classes para modificar propriedades simples
* Exemplos
    * Tachyons
    * Tailwind CSS
    * BassCSS

```css
.tl {
    text-align: left;
}

.tr {
    text-align: right;
}

.tc {
    text-align: center;
}

.tj {
    text-align: justify;
}

.w-10 {
    width: 10%;
}

.w-20 {
    width: 20%;
}

.w-25 {
    width: 25%;
}

.w-30 {
    width: 30%;
}
```

```html
<div class="w-10 tl pa1">
    Conteúdo do elemento aqui
</div>
```

