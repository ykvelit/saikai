# SDLC: Code

- Esta fase tem como foco a codificação do produto pelas equipes competentes
- A introdução de análise estática de código é fundamental  nesta fase 
- A análise estática  de código deve ser parte do Pipeline DevOps e ocorrer de forma automatizada
- A análise estática  de código deve ser considerada desde a IDE de Desenvolvimento  dos colaboradores

## Quebra do pipeline

- O que fazer em caso de detecção de vulnerabilidade? 
    - Quebrar o Pipeline em função da gravidade da vulnerabilidade 
        - Requer Maturidade
    - Adotar mecanismo de aprovação com responsabilização  sem quebrar o Pipeline 
        - Requer Supervisão, Treinamento e Conscientização Eficaz

## Source Code Management

- Repositório  onde o código-fonte  é centralizado e devidamente integrado ao Pipeline
- Código-fonte  majoritariamente  é classificado  como informação confidencial e segredo industrial
- Requer rígido controle  de acesso e proteção  contra  exfiltração  de dados (DLP, Controle  de Acesso, Revisão de Acesso)
- Requer configurações  de proteção de Branch, estratégia  de versionamento  e Branch Workflow,  revisores obrigatórios  e número de revisores,  alertas de divulgação não autorizada, identificação  de informações sigilosas,  processo de aprovação, auditoria,  entre  outros 
- Cada organização pode definir  o workflow do gerenciamento  de Branches (ao lado Gitflow Workflow)
- Idealmente a análise estática  de código deve ocorrer em todas as Branches anteriores  à Branch Main 

- Ferramentas
    - GitHub
    - GitLab
    - Azure DevOps
    - Bitbucket
    - AWS CodeCommit

- GitHub Advanced Security (GAS)
    - Code Scanning 
        - Encontra possíveis vulnerabilidades de segurança e erros de codificação usando o CodeQL ou ferramenta de terceiros
    - CodeQL CLI
        - Processa localmente projetos de software ou gera resultados de scanning de código para upload para o GitHub
    - Secrets Scanning
        - Detecta segredos (chaves e tokens) verificados em repositórios privados
        - Se a proteção push estiver ativada, também detecta segredos quando eles são enviados para o repositório
    - Custom Auto-Triage Rules
        - Gerenciamento de alertas Dependabot. Com regras de triagem automática personalizadas permitindo controle sobre os alertas que deseja ignorar ou acionar uma atualização de segurança
    - Dependency Review
        - Apresenta o impacto total das mudanças nas dependências e detalhes de quaisquer versões vulneráveis antes de mesclar o Pull Request

- Commit e Pull Request
    - O SCM deve ser integrado com soluções de análise estática de código
    - Forma de notificar  a equipe sobre as alterações  feitas por um usuário em uma branch específica  do repositório
    - Um pull request é uma etapa realizada  antes de mesclar as alterações  com a branch principal  e adicionar  commits de acompanhamento  para discutir  as alterações  com as partes envolvidas
    - A análise estática de código deve ocorrer  no Pull Request como uma tarefa obrigatória
    