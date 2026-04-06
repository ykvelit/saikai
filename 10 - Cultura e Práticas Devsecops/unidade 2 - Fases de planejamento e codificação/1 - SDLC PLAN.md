# SDLC: Plan

- Software Development Life Cycle

- Esta fase caracteriza-se  pelas definições de alto nível de como o produto será implantado na organização  e devido planejamento 

- Define os requisitos  de segurança de forma abrangente,  como a segurança  é incorporada  ao SDLC, aspectos de cultura no contexto  de segurança, automatização  de SaC (Security as Code) no Pipeline

- Define ainda os controles técnicos  e organizacionais adotados, melhores práticas  e codificação segura

## Cultura

- A cultura é definida como a interação entre pessoas e grupos em uma organização

- Ajuda a estabelecer a comunicação e melhorar a compreensão mútua de metas, objetivos e responsabilidades entre as equipes

- Busca quebrar silos nas áreas de Desenvolvimento, Quality Assurance (QA), Operações e Segurança

- Governança
    - Criar métricas abrangentes para garantir que políticas e melhores práticas sejam seguidas
    - Medir o desempenho de pessoas, processos e tecnologias

- Processo
    - Processos de segurança devem ser integrados e devem possuir estreita associação com os processos de desenvolvimento e operações

- Tecnologia
    - Adotar automação, SaC, IaC, e gerenciamento de configuração
    - Tecnologias devem integrar o pipeline de CI/CD

- Pessoas
    - Equipes devem comunicar e colaborar entre si para garantir feedback oportuno

- Lacuna de profissionais de segurança da informação (SI)
    - Cenário típico (geralmente 100 desenvolvedores, 20 profissionais de Operações e 1 de segurança) nas empresas quanto à organização das pessoas e envolvidos no contexto de DevSecOps
    - Este cenário conduz a um ínfimo envolvimento da segurança com as áreas de desenvolvimento e operações

- Security Champion
    - Deve haver  pessoas dedicadas  de segurança  da informação  para suportar o processo  de segurança  no SDLC
    - Uma estratégia de um Programa  de Security  Champion pode ser adotada treinando defensores  de segurança  na equipe de desenvolvimento  para garantir que a segurança  seja o objetivo  principal  em todo o processo  de entrega de software
    - O Security  Champion  deve assumir  a responsabilidade  de gerenciar  (coordenar,  rastrear  e relatar)  as questões  de segurança  no projeto/produto  e fornecer  orientação  para tomar  as decisões  necessárias  para envolver  uma equipe  de segurança
    - Aplicar a segurança continuamente no SDLC
    - Trabalhar com a área de segurança da informação em estratégias de mitigação de riscos
    - Auxiliar as equipes de QA e Testes
    - Acompanhar e monitorar testes de software e de segurança
    - Auxiliar no desenvolvimento de um ambiente de Integração Contínua (CI)
    - Ter conhecimento dos principais ataques cibernéticos contra as aplicações
    - Ter conhecimento sobre o OWASP TOP 10, OWASP Testing Guide, Codificação Segura
    - Colaborar com as equipes de desenvolvimento e operações para monitorar e registrar problemas de segurança no SDLC

- Maturidade e cultura
    - Cultura e estratégia
    - Automação
    - Estrutura e processos
    - Colaboração e compartilhamento

## Maturidade Devops

- Estágio 1: Inicial
    - Ambiente sem DevSecOps e as equipes de Desenvolvimento, Segurança e Operações atuam em silos

- Estágio 2: Gerenciado
    - Foco na colaboração entre as equipes de Desenvolvimento, Segurança e Operação para estabelecer agilidade no processo de desenvolvimento e automatização nos processos operacionais

- Estágio 3: Definido
    - Um processo de negócio bem definido e um processo automatizado são adotados no ambiente organizacional

- Estágio 4: Mensurado
    - A organização concentra-se em entender o processo e os recursos de automação para habilitar processos de Integração Contínua e Entrega Contínua (CI/CD)

- Estágio 5: Otimizado
    - A organização concentra-se em melhorar o trabalho em equipe, otimizando os resultados do negócio, obtendo visibilidade dos resultados e valorizando os esforços da equipe

## Focos de maturidade

- Maturidade da Aplicação
    - Determina a segurança no processo de desenvolvimento de código desde a fase de desenvolvimento até a produção
    - A organização deve empregar automação para executar a construção, teste, varredura de segurança e monitoramento no pipeline de implantação para detectar o nível de maturidade nos aplicativos

- Maturidade de Dados
    - Verifica a capacidade das operações de dados em detectar e automatizar alterações de dados
    - Garante que todas as funcionalidades atendam ao nível de maturidade de DevOps por dados (DataOps)

- Maturidade de Infraestrutura
    - A capacidade de simplificar as habilidades de gerenciamento da infraestrutura pertencentes à automação
    - Adota funções de automação, simplificação, autoatendimento e monitoramento para alinhamento com o negócio e medir o nível de maturidade do DevOps por infraestrutura

## CAMS

- Culture
    - Interação entre pessoas e grupos em uma organização
    - Ajuda a estabelecer comunicação e melhorar a compreensão mútua de metas, objetivos e responsabilidades

- Automation
    - Foco na adoção de um pipeline que consiste em Infraestrutura como Código (IaC), Integração Contínua (CI) e Entrega/Implantação Contínua (CD) para gerenciar a cultura e os objetivos organizacionais

- Measurement
    - Medir o progresso de várias atividades e processos de DevSecOps usando métricas e indicadores-chave de desempenho (KPIs) para garantir a melhoria contínua (requer onível máximo de maturidade)

- Sharing
    - Promove a transparência ao compartilhar novas descobertas, melhores práticas e feedback
    - Ajuda diferentes equipes a trabalharem juntas para atingir o objetivo comum
    - Foca nos ciclos de feedback e permite a melhoria contínua da organização

- Outras variações incluem CALMS, adicionando o Lean (para processos enxutos) e CALMSS, adicionado o Sourcing (para atividades de terceirização)

## Premissas da fase de planejamento

- Segurança da Informação deve ser introduzida sempre no início do projeto/produto no SDLC
- A cultura de segurança no SDLC (ou cultura DevSecOps) deve ser patrocinada pelo Senior Management 
- Políticas de Segurança para o SDLC e guias de melhores práticas devem ser implementadas e adotadas (Controles Organizacionais)
- As equipes (Dev e Ops) devem ser treinadas e conscientizadas
- Redução do Débito Técnico de Segurança (Security Champion pode apoiar)

## Fases típicas do SDLC

- Iniciação e Planejamento
- Levantamento de Requisitos
- Especificação de Design
- Desenvolvimento e Documentação 
- Teste de Software
- Transição para Produção 
- Descomissionamento

## OWASP Proactive Controls

- Defina Requisitos de Segurança
- Utilize Frameworks e Bibliotecas de Segurança
- Acesso Seguro à Base de Dados
- Codifique e Sanitize/Escape os Dados
- Valide Todas as Entradas
- Implemente Identidade Digital Segura
- Aplique Controles de Acesso
- Proteja os Dados
- Implemente Logs e Monitoramento de Segurança
- Faça o Tratamento de Erros e Exceções

## Modelo SD3+C

- Secure by Design
    - Focado em prevenir violações de segurança no SDLC, gerenciamento de acesso, economia de mecanismo (nada desnecessário deve ser implementado), reduzir a superfície de ataque

- Secure by Default
    - Requisitos de segurança devem ser implantados como parte integrante do produto, balanceando entre requisitos e produtividade, falha segura, controle de privilégios, criptografia

- Secure by Deployment
    - Padrões de codificação segura, defesa em profundidade, autenticação, auditoria, criptografia de dados em repouso

- Communication
    - Comunicação segura entre todos e quaisquer componentes para manter a confidencialidade e integridade das informações
    - Estabelecer relações de confiança entre componentes