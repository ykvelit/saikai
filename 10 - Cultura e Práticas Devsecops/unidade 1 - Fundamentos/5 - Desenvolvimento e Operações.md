# Desenvolvimento e Operações

- Desenvolvimento (Dev)
    - Aumentar o valor para o negócio
    - Agilidade para inovar
    - Requisitos funcionais

- Operações (Ops)
    - Proteger valor para o negócio
    - Estabilidade do ambiente
    - Requisitos não funcionais

- Extreme Programming, SCRUM e KANBAN, preenchem a lacuna entre cliente e desenvolvimento

- DevOps preenche a lacuna entre Desenvolvimento e Operações

- Fatores de sucesso do DevOps
    - Comunicação e colaboração 
        - Desenvolvimento e Operações colaboram entre si com feedback contínuo
    - Redução de falhas
        - Ambientes mais homogêneos (desenvolvimento, teste e produção)
    - Provisionamento
        - Provisionamento da infraestrutura é tempestiva por meio de Infraestrutura como Código (IaC)
    - Automatização
        - Tarefas e testes são automatizados, reduzindo o tempo na entrega do software
    - 5x menos chance de falhas
    - 440x mais rápido entre commit e deploy
    - 46x deploys mais frequentes
    - 44% mais tempo com novas features

- Building blocks
    - Pessoas
        - Todas as equipes devem colaborar e trabalharem juntas
    - Processos
        - Eficiência de processos ajuda a organização a melhorar a produtividade
    - Produtos/Tecnologia
        - Minimizar débito técnico e aumentar a agilidade

## Continuous integration

- Continuous integration
- Integração Contínua (CI) (XP Programming) testa e mescla automaticamente as alterações para ajudar a manter a integridade da base de código
- Auxilia na detecção e correção de bugs nos estágios iniciais, executando testes automatizados
- Fornece feedback imediato sobre os problemas à medida que eles ocorrem 
- Reduz riscos ao tornar o processo de implantação fácil e previsível

## Continuous delivery

- Entrega Contínua (CD) é uma extensão do CI
- Usa ferramentas avançadas para testar e validar completamente uma compilação e a passa para a implantação  em ambiente de homologação
- Elimina a complexidade de implantação de software
- Permite lançamentos (releases) com mais frequência e acelera o ciclo de feedback com os clientes
- Reduz a pressão para tomar decisões sobre pequenas mudanças, incentivando iterações mais rápidas

## Continuous deployment

- Atua na implantação contínua de alterações de configuração, novos recursos e correções erros para o ambiente de produção
- Automatiza as tarefas repetitivas para o processo de implantação de software
- Garante implantação sem comprometer a segurança e minimiza erros
- Permite que as organizações integrem processos e equipes em um único pipeline unificado

## Fases típicas do método DevOps

- Plan
    - Requisitos  das partes interessadas  e clientes,  e feedback,  sprints
- Code
    - Escrita  de código, kit de desenvolvimento,  plugins, linguagens
- Build
    - Commit, pull request,  aprovação,  merge, artefatos  de software
- Test
    - UAT, teste  de segurança, teste  de carga, integração
- Release
    - Processo  de build é planejado,  agendado e controlado  em diferentes  ambientes
- Deploy
    - Todo o produto  de software  e arquivos  correlatos  são implantados  no ambiente de produção  (máquinas virtuais,  contêineres)
- Operate
    - O produto  de software  é entregue  para o cliente  em pleno funcionamento  pela equipe de Operações
- Monitor
    - Monitoramento  contínuo  do software,  métricas,  desempenho


## Práticas gerais no método DevOps

- Infrastructure as a Code (IaC)
- Continuos Integration
- Testes Automatizados
- Continuos Deployment
- Gerenciamento de Release
- Monitoramento de Desempenho de Aplicações
- Escalonamento Vertical, Horizontal e Diagonal
- Monitoramento da Disponibilidade
- Gerenciamento de Configuração
- Feature Toggle Flags
- Provisionamento e Desprovisionamento Automatizado
- Self-Service Environment
- Rollback automatizado
- Suporte ao Desenvolvimento Baseado em Hipótese

## DevOps em ambiente de nuvem

|   | Azure | Amazon |
|---|-------|--------|
| Source Code Management (SCM) | Azure Repos | AWS CodeBuild |
| Package Management | Azure Artifacts | AWS CodeArtifact |
| CI/CD Pipeline | Azure Pipelines | AWS CodePipeline |
| Unit and Integration Testing | Azure TestPlans | AWS CodePipeline |
| Project Management | Azure Boards | AWS CodeStar |
| Deployment | Azure Automation | AWS CodeDeploy |
| Infrastructure Automation | Automation, Resource Manager Templates | AWS CloudFormation |
