# Introdução ao Nest.js

- NestJS é um framework para construção de aplicativos Node.js escaláveis e eficientes, baseado no TypeScript

- Ele utiliza os princípios da arquitetura modular muito inspirada no Angular e orientada a objetos para fornecer uma estrutura robusta para o desenvolvimento de APIs e aplicativos web

- O NestJs atua como um framework que encapsula os recursos de servidor providos pelo Express (ou o fastify) para fazer com que seja possível estruturar a aplicação de uma forma muito mais robusta e escalável

## Services

- São classes responsáveis por conter a lógica de negócio da aplicação, como a interface com o banco, integrações com APIs externas e quaisquer outras regras 
pertinentes

- Podem ser injetados em controladores, módulos ou outros provedores de serviço

```js
import { Injectable } from'@nestjs/common'

@Injectable()
export class ProductsService {
    findAll(): string {
        return 'Lista de produtos';
    }
}
```

- O conceito de injeção de dependências no Nest (ou dependency injection como na documentação) facilita muito o reuso de código e a visualização de dependências entre partes da aplicação

- Uma classe que atua como um Provider pode ser injetada em qualquer construtor, desde que esteja dentro de um mesmo módulo

- Uma classe injetável (Injectable) possui uma instância única na aplicação, atuando como um singleton

## Controllers

- São responsáveis por lidar com as requisições HTTP e retornar as respostas adequadas

- Decorados com metadados que definem os endpoints da API e os métodos HTTP que cada endpoint suporta

```js
import { Controller, Get } from '@nestjs/common'
import { ProductsService } from './products.service'

@Controller('products')
export class ProductsController {

    constructor(private readonly productsService: ProductsService) {}

    @Get()
    findAll(): string {
        return this.productsService.findAll();
    }
}
```

## Módulos

- Segundo o NestJs, muitos frameworks e bibliotecas têm o propósito de resolver problemas isolados, mas a grande maioria falhou em resolver um problema arquitetural

- Arquitetura 100% modular
    - Utiliza módulos para organizar e estruturar a aplicação de forma modular e escalável