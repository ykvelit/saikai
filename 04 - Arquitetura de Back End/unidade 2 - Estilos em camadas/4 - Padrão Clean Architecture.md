# Padrão Clean Architecture

- Arquitetura Limpa
- Separação de responsabilidades
- Livro Clean Architeture
- Separação de camadas
- Conjunto de conceitos e princípios que visam a construção de sistemas de alta coesão, baixo acoplamento e separação de responsabilidades
- A regra principa da Arquitetura Limpa é a Regra da Dependência
    - Que estabelece que as dependências de um código fonte devem sempre apontar para dentro, ou seja, as camadas mais internas não devem depender das camadas mais externas
    - Onion Architecture
- Proposições
    - Separação das preocupações
    - Isolamento das regras de negócio
    - Independência de frameworks
    - Testabilidade
    - Independência de UI
    - Independênca de banco de dados
    - Independênca de qualquer coisa externa

- Outra regra importante é o Princípio do Reuso Comum
    - Que diz que não devemos entregar para o usuário mais do que ele realmente precisa e devemos manter juntas somente as classes que o usuário irá utilizar
    - Ser econômica

- O papel do arquiteto é enxergar os pontos de mudança e criar limites/divisões para separar as partes do sistema de forma coesa
    
## Arquitetura Limpa X DDD

- Abordagens que se complementam
- Arquitetura Limpa
    - Foca na organização do código para criar sistemas escaláveis, mantendo a separação de preocupações e facilitando a manutenção e evolução do software
    - Baseia-se em princípios de design de software, como SOLID e inversão de dependências. O código é dividido em camadas, sendo a camada mais interna responsável pela lógica de negócio e as camadas mais externas responsáveis pela comunicação com o mundo externo (UI, DB, etc)
    - O foco é na organização e separação od código em diferentes camadas e componentes. A arquitetura limpa tem um padrão de camadas concêntricas
        - Entidades
            - Regra de negócio
        - Casos de uso
            - Interação com a lógica de negócio
        - Adaptadores
            - Conversão de formatos
        - Estruturas
            - Integração com o mundo externo

- DDD
    - Foca na modelagem do domínio do problema, alinhando o design do software com o conhecimento do negócio e a linguagem utilizada pelos especialistas no domínio
    - Baseia-se em princípios específicos para a modelagem de domínios, como entidades, agregados, repositórios, serviços de domínio e objetos de valor. O DDD também promove o uso de uma linguagem ubíqua, compartilhada por desenvolvedores e especialistas no domínio para garantir uma compreensão comum do problema
    - O foco é na modelagem do domínio, criando um modelo rico e expressivo que reflita o conhecimento do negócio. O DDD também se preocupa com a divisão do sistema em contextos limitados, que são partes do domínio com limites bem definidos, facilitando o desenvolvimento e manutenção do sistema

