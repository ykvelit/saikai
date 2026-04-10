# Infraestrutura como Código em DevSecOps

## IaC

- Processo de automatização do gerenciamento, provisionamento e desprovisionamento da infraestrutura e seus elementos, como serviços, redes, máquinas virtuais, contêineres, balanceadores de carga usando código em vez de processos manuais

- Permite a criação e versionamento da infraestrutura, assim como a devida gestão de configuração do ambiente

- Fast Feedback
- Colaboração
- Iteração
- Visibilidade
- Automação da Infraestrutura
- Controle de Versão e Peer Review
- CI/CD
- Automação de Teste
- Automação de Deploy

- Papéis
    - Dev
        - Escreve o Template, Políticas e código de infraestrutura
    - Aprovador 
        - O código da infraestrutura é armazenado no SCM e aprovado por partes competentes
    - Orquestrador
        - Executa o código para provisionar, desprovisionar e configurar recursos

- Infraestrutura Mutável
    - Modificações no ambiente de produção são realizadas sem interromper as operações ou serviços executados na aplicação
    - Este modelo implica em mudanças e atualizações contínuas para atender às demandas de negócios

- Infraestrutura Imutável
    - Não pode ser alterada uma vez provisionada
    - Para fazer alterações requer-se provisionar novamente toda a infraestrutura e destruir a antiga

- Paradigma Imperativo
    - A configuração desejada é definida por meio de uma sequência de etapas
    - Descreve a ordem de execução
    - Requer-se definir os objetivos e as etapas para atingir o estado desejado da infraestrutura (Chef, é um exemplo)
    - Não indicado para ambientes complexos

- Paradigma Declarativo
    - O estado desejado da infraestrutura é definido diretamente sem descrever as etapas para chegar a esse estado
    - Requer-se apenas mencionar informações adicionais, como quantas máquinas serão implantadas, as cargas de trabalho serão virtualizadas ou em contêineres, quais aplicativos serão implantados, como serão configurados (Terraform, Puppet, Ansible são exemplos)

- CIS Benchmark
    - O CIS Benchmark pode ser implantado como gestão de configuração por meio de infraestrutura como código (IaC)
    - Imagens e instâncias/máquinas virtuais Linux/Windows de marketplace Azure, AWS e Google estão disponíveis já com o CIS Benchmark configurado
    - A adoção do CIS Benchmark ajuda em manter conformidade com a ISO/IEC 27001, PCI-DSS, FISMA, entre outros
    - A adoção do CIS Benchmark é usado para Security Hardening
