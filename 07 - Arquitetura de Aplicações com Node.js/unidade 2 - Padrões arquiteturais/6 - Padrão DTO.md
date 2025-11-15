# Padrão DTO

- Data Transfer Object

- Uma vez que temos as entidades prontas para serem mapeadas para o banco de dados, podemos criar um DTO, que serve para mapear os dados da entidade para o cliente

- Teoricamente, poderíamos expor essas entidades diretamente para os serviços, entretanto nem sempre é uma boa ideia transferir toda a entidade para o cliente, visto que:
    - Eventualmente, precisamos ocultar propriedades específicas
    - O cliente pode enviar dados diferentes dos que são armazenados no banco de dados para executar alguma regra de negócio específica

- Evita vulnerabilidades de excesso de postagem quando enviamos dados não desejados do banco para o cliente

- Maior desacoplamento entre a camada de serviço e a camada de banco de dados

- Podemos implementar técnicas de validações que nos garantem uma API mais segura e confiável no tratamento de dados

- Input e Output de dados podem ser customizados globalmente através de validadores e definição dos tipos via DTO

- As validações de Input garantem que os dados que chegam via controladores estão de acordo com o que definimos previamente

- As validações de Output garantem que estamos expondo apenas os dados necessários como resposta a uma requisição