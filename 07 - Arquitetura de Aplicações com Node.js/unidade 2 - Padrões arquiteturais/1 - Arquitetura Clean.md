# Arquitetura Clean

- Arquitetura limpa

- Arquitetura Clean é uma tentativa de criar um modelo que ofereça separação de responsabilidades através de camadas

- Combinação com uma série de melhorias de arquiteturas criadas anteriormente, como a Hexagonal (ou Ports and Adapters)

- Dentre os pilares desses modelos arquiteturais, podemos citar:
    - Independência de frameworks
        - Arquitetura pode ser aplicada em qualquer framework de qualquer linguagem
    - Testabilidade
        - Regras de negócio devem poder ser testadas sem depender da camada de UI
    - Independência da UI
        - A interface deve poder ser desacoplada e independente da regra de negócio da aplicação e dos casos de uso
    - Independência de terceiros
        - Regras de negócio específicas da aplicação não devem conhecer sobre interfaces do mundo externo

- A regra primordial para o funcionamento dessa arquitetura é a regra da dependência
    - Os elementos de um círculo interno não devem saber nada sobre os elementos de um círculo externo

- Resumidamente, algo declarado em um círculo externo não deve ser mencionado diretamente pelo código em um círculo interno