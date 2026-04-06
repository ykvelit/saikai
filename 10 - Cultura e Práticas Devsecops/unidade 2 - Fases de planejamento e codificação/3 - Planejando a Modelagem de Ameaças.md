# Planejando a modelagem de ameaças do produto

## Scrum: Artefatos e eventos

- História do Usuário
    - Requisitos dos usuários
    - São documentos que descrevem os requisitos do sistema, contudo, histórias são documentos resumidos, com apenas duas ou três sentenças, que define o que se deseja que o sistema faça

- Backlog do Produto
    - Compreende uma lista de histórias, ordenada por prioridades, pelo Dono do Produto e constituem uma descrição resumida das funcionalidades que devem ser implementadas no produto

- Sprint
    - Em Scrum trata-se de uma iteração. Scrum é um método iterativo, no qual o desenvolvimento é dividido em sprints, de até um mês 
    
- Planejamento do Sprint
    - Reunião na qual todo o time se reúne para decidir as histórias que serão implementadas no sprint que será iniciado
    - Marca o início de um sprint
    - O Dono do Produto propõe as histórias (a partir de um Épico) e os desenvolvedores validam a velocidade para implementá-las
    - Os desenvolvedores desmembram as histórias em Tarefas estimando a duração

- Backlog do Sprint
    - Artefato gerado ao final do Planejamento do Sprint
    - É uma lista com as tarefas do sprint e a duração destas
    - Apesar de determinadas tarefas poderem ser alteradas e a duração, o objetivo do sprint (sprint goal) - lista de histórias selecionadas para o sprint – não deve ser alterada

## Scrum: Papéis e responsabilidades

- Product Manager (PM)
    - Analisar o mercado
    - Definir as estratégias do produto
    - Avaliar a concorrência
    - Gerenciar a visão do produto
    - Traduz a visão estratégica do produto do Senior Management (CEO) para as áreas
    - Atua frente ao âmbito estratégico da organização
    - Dissemina o método ágil Scrum na organização

- Product Owner (PO)
    - Representa o cliente dentro da organização
    - Criar a visão do produto
    - Tomar decisões no produto
    - Adota metologias ágeis
    - Desenvolve e monitora métricas
    - Responsável pelo Backlog do Produto
    - Define o roadmap do produto
    - Refina o Backlog 
    - Conduz a Daily Scrum
    - Conduz a reunião de revisão do sprint

- Desenvolvedores
    - Definem as tarefas a partir das histórias do usuário
    - Definem a velocidade possível de implementação
    - Participam da Daily Scrum 
        - Indicando o que foi feito
        - O que será feito no dia 
        - Problemas enfrentados
    - Participam da Revisão do Sprint 
        - Resultados da sprint
        - Apresenta o produto para o cliente
        - Aprovação das histórias ou reprovação, que volta para o backlog do produto e requer novas sprints

## Metodologias de Threat Modeling

- STRIDE 
    - Spoofing, Tampering, Repudiation, Information Disclosure, Denial of Service (DoS), and Elevation of Privilege

- PASTA 
    - Process for Attack Simulation and Threat Analysis

- TRIKE

- VAST 
    - Visual
    - Agile
    - Simple Threat

- OCTAVE 
    - Operationally Critical Threat, Asset, and Vulnerability Evaluation

## Processo de modelagem de ameaças

1. Identificar ativos
2. Decompor a aplicação
3. Identificar ameaças
4. Classificar ameaças
5. Determinar impactos/gravidade
6. Aplicar controles

## Metodologia STRIDE

- STRIDE é uma metodologia para identificar ameaças à segurança computacional desenvolvido por Praerit Garg e Loren Kohnfelder na Microsoft

|   | Tipo de ameaça | Violação | Meios de violação |
|---|----------------|----------|-------------------|
| S | Spoofing | Autenticação | Acessar e usar as credenciais de outro usuário, como nome de usuário e senha  |
| T | Tampering | Integridade | Modificar sem autorização os dados em trânsito, repouso ou em uso |
| R | Repudiation | Não Repúdio/Autenticidade | Afirmar que não é responsável pela ação |
| I | Information Disclosure | Confidencialidade | Provê informação para quem não está autorizado |
| D | Denial of Services | Disponibilidade | Negar ou impedir acesso a recursos |
| E | Elevation of Privilege | Autorização | Obter acesso privilegiado a recursos para obter acesso não autorizado a informações ou comprometer um sistema |

- Quais são as funções de negócios do sistema?
- Quais são os papéis dos atores que interagem com o sistema?
- Que tipo de dados o sistema processa e armazena?
- Existem requisitos comerciais ou legais que afetam a segurança?
- Com quantos usuários o sistema deve lidar?
- Quais são as consequências se o sistema não fornecer confidencialidade, integridade ou disponibilidade dos dados e serviços que o sistema lida?
