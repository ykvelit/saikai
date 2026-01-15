# Padrão Repositório

- Visa separar a lógica de persistência da camada do domínio de negócio

- É uma camada que fica entre o Serviço e o banco de dados

- A implementação de queries e toda a logica direta de acesso a dados fica na camada repositor

- A grande vantagem é que qualquer alteração na camada de dados não afeta a implementação da regra de negócio