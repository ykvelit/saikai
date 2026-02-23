# Json e Json Schema

## JSON

- Permite estruturar dados diversos

- Simples de ser criado e lido

- Compatível com diversas plataformas

- Oferece bom desempenho na leitura

- Tipos de Dados
    - Dados numéricos: inteiro, real
    - Dados textuais: caracteres, strings
    - Dados booleanos: true e false
    - Dados Compostos
        - Datas
        - Arrays
        - Objetos

## JSON Schema

- JSON Schema é um vocabulário que permite descrever, referenciar e validar documentos JSON

- Benefícios
    - Descreve formatos de dados 
    - Provê uma documentação legível para seres humanos
    - Permite validação de dados 

- Aplicações
    - Automação de testes
    - Garantir qualidade de dados submetidas por clientes

| Palavra Reservada | Significado |
| ----------------- | ----------- |
| $schema | Indica o dialeto (Versão) utilizado para descrever o esquema Possui uma URI com o endereço do dialeto |
| $id | Indica o base URI para esta definição de esquema na Internet Possui uma URI sem fragmentos com o endereço da definição do esquema |
| $ref | Indica um esquema definido em outro local |
| $defs | Indica um local para definição de esquemas e sub-esquemas JSON reutilizáveis em um esquema mais gera |