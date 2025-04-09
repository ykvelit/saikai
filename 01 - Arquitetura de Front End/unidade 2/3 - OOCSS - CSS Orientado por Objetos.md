# OOCSS: CSS Orientado por Objetos

* Separação entre CSS de estrutura e skin
* Structure properties
    * width
    * height
    * padding
    * margin
    * overflow
* Skin
    * color
    * background
    * font
    * shadow

## Antes
```css
.button-1 {
    width: 150px;
    height: 50px;
    background: #fff;
    border-radius: 5px;
}

.button-2 {
    width: 150px;
    height: 50px;
    background: #000;
    border-radius: 5px;
}
```

```html
<button class="button-1">Botão</button>
```

## Depois
```css
.button {
    width: 150px;
    height: 50px;
    border-radius: 5px;
}

.skin-1 {
    background: white;
}

.skin-2 {
    background: black;
}
```

```html
<button class="button skin-1">Botão</button>
```