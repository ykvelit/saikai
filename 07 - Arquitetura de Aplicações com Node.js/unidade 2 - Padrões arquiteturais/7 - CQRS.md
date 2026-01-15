# CQRS

- Command and Query Responsibility Segregation

- O fluxo de operações de aplicações CRUD (Create, Read, Updated e Delete) pode ser descrito nos seguintes passos
    - A camada de controller gerencia as requisições HTTP e delega tarefas para a camada de serviços
    - A camada de serviços é onde a maior parte da regra de negócio é implementada
    - Serviços usam repositórios para acessar/alterar dados persistidos
    - Entidades performam como containers para valores e get/set

- Esse fluxo normalmente é mais do que necessário para aplicações pequenas/médias, mas pode não ser a melhor abordagem para aplicações em larga escala

- Para grandes aplicações, o problema do fluxo anterior começa a aparecer quando precisamos de, eventualmente, customizar de formas diferentes as operações de escrita e leitura

- Operações de escrita e leitura podem precisar de estruturas de dados diferentes para otimização de performance e diferentes dimensionamentos

- Além disso, as representações de leitura e gravação de dados geralmente são diferentes 
    - Campos necessários durante atualizações podem ser desnecessários durante as leituras

- O CQRS tenta sanar problemas de
    - Separação de responsabilidades
        - Separa operações de leitura e escrita em modelos separados

    - Escalabilidade
        - Operações de leitura e escrita são escaladas de forma independente, se necessário

    - Flexibilidade
        - Utilização de tipos diferentes de armazenamentos para leitura e escrita
