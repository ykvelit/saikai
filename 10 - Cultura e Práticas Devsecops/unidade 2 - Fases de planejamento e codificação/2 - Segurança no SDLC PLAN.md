# Segurança no SDLC: PLAN

## Gestão de mudança no mundo Ágil

- Gestão de mudança tradicional
    - Mudança do Software
        - A equipe recebe instruções para realizar uma mudança no software, sendo o risco, compreendido como Alto
    - GMUD
        - O CAB (Change Advisory Board) irá analisar a mudança e os riscos de segurança associados
        - O responsável pela mudança é um indivíduo ou dono da mudança
    - Redução de risco
        - O CAB, enquanto órgão consultivo, apresenta os argumentos que requerem ser trabalhados para reduzir o risco ou convencimento para não realizar a mudança

- Gestão de Mudanças DevOps
    - Mudança do Software
        - A equipe recebe instruções para realizar uma mudança no software, sendo o risco, compreendido como Alto
    - CI/CD e Testes Automatizados
        - O CAB (Change Advisory Board) irá analisar a mudança e os riscos de segurança associados
        - O responsável pela mudança é a equipe
    - Redução de risco
        - O CAB, enquanto órgão consultivo, apresenta os argumentos que requerem ser trabalhados para reduzir o risco ou convencimento para não realizar a mudança

- Para mudanças de baixo risco deve-se considerar a automação do processo de aprovação para tornar o processo de mudanças alinhando com as entregas

- As equipes de desenvolvimento e os devidos líderes responsáveis devem analisar o risco para decidir qual fluxo a mudança deve seguir (Padrão, Normal, Urgente)

- A maturidade nos testes de Segurança e do software são fundamentais para reduzir os riscos antes de decidir o fluxo da mudança

- Gestão de Mudanças Ágil
    - Automação de Processos
        - Buscar automatizar os processos, garantindo que os requisitos de conformidade e regulamentação sejam atendidos, minimizando intervenções e erro humanoAutomação de Processos
    
    - Adotar CAB
        - Use um Change Advisory Board (CAB) que forneça suporte ao gerenciamento de mudanças aprovando solicitações, avaliando e priorizando mudanças, analisando os devidos riscos

    - Integração com Ferramentas
        - Integrar o gerenciamento de mudanças com ferramentas e processos existentes, por exemplo, Jira/ServiceNow/Confluence/Outros para enviar e-mails para aprovações quando uma alteração for enviada ao código pelo desenvolvedor
        - Requer trilhas de auditoria e lastro de aprovação

    - Integração Contínua
        - Alcançar a Integração Contínua (IC) usando monitoramento e mitigando problemas internos e aqueles relatados por clientes
        - A estratégia de gerenciamento de mudanças deve ser flexível, robusta em sua abordagem, mas sem complexidades de implementação

    - Monitoramento e Investigação
        - Tente investigar o fluxo de trabalho sempre que um novo código ou uma atualização for introduzida
        - Deve-se Implementar métricas de desempenho adequadas para calcular os riscos e vulnerabilidades envolvidos nas mudanças

## Melhores práticas para um planejamento de sucesso

- Patrocínio do Senior Management
- Quebrar silos e focar na colaboração 
    - Inclui papéis e responsabilidades
- Foco no cliente 
    - Qualidade do produto
- Sempre adotar metas realistas, tangíveis e exequíveis
- Adotar avaliações de desempenho de equipes e indivíduos 
- Gerenciamento de mudanças sem impactar a produtividade
- Segurança não pode ser um gargalo para a entrega do produto 
    - Automação
- Monitoramento contínuo do ambiente de produção e feedback
- Colaboração ativa entre as partes interessadas
- Automatizar testes de software e segurança
- Automatize e adote a Integração Contínua (CI)
- Automatize e adote a Entrega/Implantação Contínua (CD)
- Adote Infraestrutura como Código (IaC) e Segurança como Código (SaC)

## Tecnologias e processos

- SCM (Source Code Management)
- Análise Estática de Código
- Análise Dinâmica de Código e Pentest
- Análise de Composição de Software
- Análise de Qualidade de Software
- Automatização de Testes
- Monitoramento da Infraestrutura
- Monitoramento da Aplicação (Produto)
- Centralização de Artefatos de Software
- Vault (Chave de Criptografia e Segredos)
- Centralização do Registro de Contêineres
- Controle de Acesso ao Código Fonte
- Proteção de Branches e Verificação de Pré-Commit
- Política de Revisão de Código (e de Segurança)
- Processo de Controle e Gestão de Mudanças
- Modelagem de Ameaças

## Estratégia efetiva de cultura DevSecOps

- DevSecOps é Mudança Cultural 
- Educar a Equipe
- Aprendizado Contínuo dos Desenvolvedores
- Auditorias e Avaliações de Segurança
- Habilitar Segurança 
- Baseado em Código
- Automação

## Débito

- Débito é a distância entre os sistemas atuais e esperados
- O sistema esperado é o melhor sistema para atender às necessidades presentes e futuras
- O débito leva a uma qualidade de código insatisfatória e representa o trabalho de desenvolvimento extra necessário para remediar a qualidade de código insatisfatória

- Débito Técnico
    - Devido ao deadline do projeto, equipes de desenvolvimento buscam atalhos para entregar o aplicativo, resultando em código de baixa qualidade
    - Resulta em débito técnico, que é o trabalho extra para resolver os problemas de qualidade
    - Muitas tarefas correção de código no backlog

- Débito Técnico de Segurança
    - Vulnerabilidades  e falhas no aplicativo que não foram resolvidas e que podem conduzir uma violação de segurança
    - É um subconjunto do Débito Técnico, e pode ser endereçado por meio da adoção da cultura DevSecOps
    - Muitas tarefas de remediação de vulnerabilidades  no backlog

- Tratando o débito técnico de segurança
    - Identificar Pontos de Acesso
        - Identificar o uso de anti-padrão na linguagem de programação ou framework adotado
        - Avaliar o conjunto de testes existentes
        - Garantir que dependências de software estejam atualizadas
        - Garantir que funções críticas da aplicação seja avaliada
    - Débito Técnico de Segurança
        - Realizar scan de vulnerabilidade contínuo de forma automatizada, identificando e mitigando as vulnerabilidades no Pipeline
        - Remedias as vulnerabilidades tão logo sejam detectadas no início do desenvolvimento por meio de scan contínuo do Pipeline

    - O Product Owner (PO) e equipe de desenvolvimento devem ser conscientizados e apresentar-lhes suas responsabilidades para evitar débito técnico de segurança
    - Ter em mente o princípio neste contexto que também é aplicável: “responder a mudanças mais que seguir um plano”
    - Vulnerabilidades devem ser consideradas como bugs e falhas que devem ser tratados antes de se tornarem débito técnico de segurança
    - Hooks de Pré-Commit devem ser configurado nas estações de trabalho de todos os desenvolvedores e ambiente de desenvolvimento
    - Usuários válidos, e-mails autorizados e configurações de segurança são definidos para o SCM (Source Code Management) nas estações de trabalho dos desenvolvedores e ambientes de desenvolvimento 
    - Hooks de Pré-Commit garantem a integridade dos dados do usuário, push de informações sensíveis acidentais, entre outros

## Treinamento e conscientização
- Práticas de Codificação Segura
- OWASP TOP 10
- Princípios de Segurança da Informação
- Exploração de Vulnerabilidades
- Modelagem de Ameaças
- Avaliação da Eficácia do Treinamento
