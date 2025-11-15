# Plataforma Node.js

- Código fonte baseado em C++, exposto em 2009;
- Arquitetura single thread:
    - Menor uso de memória e recursos
    - Menor complexidade
    - Fim dos deadlocks

- Possibilidade de execução de fluxos assíncronos mesmo em uma arquitetura Single thread, através de uma arquitetura baseada em eventos 
    - Promises
    - setTimeouts
    - setIntervals