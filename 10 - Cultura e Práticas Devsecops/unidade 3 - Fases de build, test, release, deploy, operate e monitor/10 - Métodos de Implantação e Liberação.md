# Métodos de Implantação e Liberação

- Deployment
    - Implantação
    - Refere-se ao processo de implantação por meios técnicos no ambiente

- Release
    - Liberação
    - Refere-se a disponibilizar o produto e seus recursos após a implantação para os clientes

- Baseado no aplicativo
    - Uso de configurações (mais simples) na aplicação que não requerem o processo de implantação, por exemplo, habilitar um recurso a partir de uma aquisição, plugins etc
    - Alternância de recursos (Feature Toggles, Bits de Recurso ou Flippers) e lançamento escuro (sem o usuário perceber)

- Baseado no ambiente
    - Há no mínimo dois ambientes, sendo que apenas um deles fica ativo para o cliente (requer configuração em balanceadores e outros recursos)
    - Blue-Green
        - Desafios na estratégia blue-green incluem a automatização dos apontamentos DNS, configuração dos balanceadores e gerenciamento dos sistemas de banco de dados
        - Mecanismos eficazes de rollback devem ser instituídos
        - Os recursos e controles de segurança devem existir e serem garantidos nos dois ambientes
    - Staging
        - Ambiente que acomoda a versão candidata à produção
        - Requer-se que seja um “espelho” do ambiente de Produção quanto à gestão da configuração, mas não necessariamente em escala
        - Diferente do ambiente de desenvolvimento, teste, homologação ou QA, pois trata-se de um ambiente com a versão testada e pronta para a produção (testes de software não ocorrem neste ambiente)
    - Canary
        - Ambiente de Pré-Release
        - Após a fase de Staging pode realizar o deploy em Canary em que entre 5% a 10% da carga de trabalho do ambiente de produção é utilizada
        - Em caso de sucesso no comportamento da aplicação, novas implantações são realizadas no restante da carga de trabalho

- Ambiente de Staging total
    - Sem comunicaçãp de dados entre o ambiente de Staging total e ambiente de Produção
    - Cópia-espelho do ambiente de Produção

- Ambiente de Staging parcial
    - Acesso Read Only às bases de dados de Produção

| Diferenças entre ambientes Staging                | Staging Total | Staging Parcial |
|---------------------------------------------------|---------------|-----------------|
| Cópia completa do ambiente de Produção            | Sim           | Não             |
| Portas de Staging de Backend e Frontend separadas | Sim           | Sim             |
| Acesso a serviços de Produção                     | Não           | Sim             |
| Acesso de leitura aos databases de Produção       | Não           | Sim             |
| Acesso de escrita aos databases de Produção       | Não           | Sim             |
| Requer rollback automatizado                      | Não           | Sim             |

- Fases
    - Fase 1: Staging
        - Versão candidata à Produção é implantada em ambiente de Staging
    - Fase 2: Canary
        - Versões que passam da fase de Staging são implantadas na fase de Canary
    - Fase 3: Produção
        - Versões que passam da fase de Canary são implantadas gradualmente em Produção