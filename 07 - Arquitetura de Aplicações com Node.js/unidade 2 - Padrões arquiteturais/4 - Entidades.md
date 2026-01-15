# Entidades

- Entidades fazem o papel de implementar os objetos que serão mapeados para o banco de dados

- Podemos colocar as propriedades, seus tipos e as validações necessárias para que elas sejam convertidas em tabelas no SQL

- Domain Driven Design

```js
import { Column, Entity, PrimaryGeneratedColumn } from "typeorm"

@Entity()
export class Project {
    @PrimaryGeneratedColumn()
    id: number

    @Column({ name: "name", nullable: false })
    name: string

    @Column({ name: "description", nullable: false })
    description: string
}
```
