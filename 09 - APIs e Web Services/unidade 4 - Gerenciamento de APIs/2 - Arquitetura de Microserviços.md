# Arquitetura de Microserviços

- Monolítico > Orientado a Serviço > Microserviços

## Arquitetura Orientada a Serviços

- Estilo arquitetural de software baseado na estruturação das aplicações de negócios por meio de um conjunto de serviços
- Cada serviço provê uma funcionalidade específica do negócio e permite a criação de aplicações distribuídas utilizando diferentes tecnologias e plataformas

- Camadas
    - Interface de Usuário
    - Processos de Negócios
    - Serviços
    - Componentes de Serviços
    - Sistemas Operacionais

## Microserviços

- Microsserviços é uma abordagem arquitetural que define um conjunto de serviços independentes com escopo limitado

| Aspecto | Monolito | Microserviços | 
|---------|----------|---------------|
| Deployment | Deploy simples e rápido do sistema inteiro | Requer recursos distintos tornando a orquestração mais complexa | 
| Escalabilidade | Difícil de manter e aplicar mudanças | Cada elemento pode ser escalado independente sem downtime | 
| Agilidade | Dificuldade de adotar novas tecnologias | Adota novas tecnologias resolvendo problemas de negócios |
| Resiliência | Um erro pode afetar o sistema inteiro | Uma falha em um serviço não afeta os demais |
| Teste | Teste fim a fim | Componentes requerem testes individuais |
| Segurança | Comunicação dentro de uma unidade única  | Comunicação interprocessos requer API gateways e maior complexidade |
| Desenvolvimento | Dificuldade de distribuir os esforços dos times em função da estrutura | Os times podem trabalhar de forma independente em cada componente |

## API Gateway

- API Gateway é um Design Pattern que oferece um único ponto de entrada para APIs numa arquitetura de microsserviços, atuando como um proxy reverso que trata solicitações de clientes e encaminha ao serviço apropriado

- Funcionalidades de um API Gateway
    - Cache de Respostas
    - Balanceamento de carga
    - Roteamento de requisições
    - Gerenciamento da autenticação  e autorização
    - Monitoramento e análise de dados
    - Documentação de APIs