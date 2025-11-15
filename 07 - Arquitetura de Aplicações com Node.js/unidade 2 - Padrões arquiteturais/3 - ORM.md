# ORM

- Object Relational Mapping

- Técnica de meta-programação que tem como objetivo transformar classes/objetos em tabelas/colunas de banco de dados

- A representação do banco é espelhada em Classes e propriedades, facilitando a manutenção do esquema de dados e a sua utilização no código-fonte

- Abstrai a implementação da integração entre linguagem e banco de dados        
    - Permite a quem está desenvolvendo a utilizar métodos abstratos que representam as instruções SQL
    
- Portabilidade
    - Possível portar entre diferentes tipos de bancos de dados sem a necessidade de refatorar toda a aplicação

## TypeORM

- O TypeORM é uma biblioteca escrita em TypeScript que implementa o conceito de ORM para aplicações baseadas em Nodejs

- Pode ser utilizada com qualquer framework e tem integração facilitada com o NestJs

- Possui um conjunto de validadores e uma série métodos para acessar o conteúdo do banco de dados

```js
import { Module } from "@nestjs/common"
import { TypeOrmModule } from "@nestjs/typeorm"

@Module({
    imports: [
        TypeOrmModule.forRoot({
            type: "sqlite",
            database: "db/sql.sqlite",
            synchronize: true,
            autoLoadEntities: true,
        }),
    ],
})
export class TypeOrmConfig {}
```