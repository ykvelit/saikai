# Sistema de Módulos

- Componentização
- Organização de código e responsabilidades
- Em Node, tudo pode virar um módulo
    - string, number, object, functions, classes etc

```js
module.export = function(x,y){
    return x + y;
}

const sum = require('./sum.js');
const result = sum(1,2);
```

```js
export default function(x,y){
    return x + y;
}

import sum from './sum.js';
const result = sum(1,2);
```