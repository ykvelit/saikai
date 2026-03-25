# Segurança

> Segurança sempre é vista comoexcessiva, até o dia que não é suficiente
> Debate sobre asegurança nacional e a liberdadepessoal, 2002
> William H. Webster (Diretor do FBI e CIA)

- Risco
    - Risco é o efeito da incerteza sobre os objetivos 
        - ISO 31000
    - Uma medida da extensão em que uma entidade é ameaçada por uma circunstância ou evento potencial e normalmente uma função de: 
        1. Os impactos adversos que surgiriam se a circunstância ou evento ocorrer
        2. A probabilidade de ocorrência (NIST)
    - Probabilidade + Impacto + Ameaça + Vulnerabilidade

- Riscos de segurança da informação
    - São aqueles que surgem através da perda da confidencialidade, integridade ou disponibilidade de informações ou sistemas de informação, e considerar os impactos na organização (incluindo ativos, missão, funções, imagem ou reputação), indivíduos, outras organizações e a Nação

- Fator de Exposição
    - Fator de Exposição é quão suscetível a perda de um ativo está ante uma ameaça
    - Ativos na DMZ, Public-Facing Applications, Vulnerabilidade, Ausência de controles de segurança da informação, ausência de controle de acesso

## Controles de segurança
- A função primária de um controle de segurança é suportar o processo de tratamento de riscos, principalmente quanto à mitigação de riscos de segurança

- Controle técnico
    - Medidas técnicas ou tecnologias, tais como Firewalls, sistemas de alarmes, CFTV

- Controle Legal
    - Relacionado à aplicação de uma legislação, requisitos regulatórios ou obrigações contratuais

- Controle Administrativo
    - Relacionado à estrutura organizacional, tais como segregação de função, rotação de trabalho, férias obrigatórias, descrição de trabalho, processo de aprovação 

- Controle Gerenciais 
    - Relacionado à gestão de pessoas, tais como treinamento, conscientização, auditoria interna

- Funções
    - Preventivo
    - Dissuasivo
    - Diretivo
    - Detectivo
    - Recuperativo/Corretivo
    - Compensatório

## SCAP

- Security Content Automation Protocol

- Conjunto de especificações interoperáveis projetadas para padronizar as convenções de formatação e nomenclatura usadas para identificar e relatar a presença de falhas de software, como configurações incorretas e/ou vulnerabilidades

### CPE
- Common Platform Enumeration
- Usa uma sintaxe semelhante aos Uniform Resource Identifiers (URI)
- CPE é um formato de nomenclatura padronizado usado para identificar sistemas e software

### CVE
- Common Vulnerabilities and Exposures
- Uma lista de registros onde cada item contém um identificador exclusivo usado para descrever vulnerabilidades publicamente conhecidas
- Identificadores exclusivos começam com CVE, seguido pelo ano de identificação e um número exclusivo 
- CVE-YEAR-#####

### CCE
- Common Configuration Enumeration
- Semelhante à CVE, exceto pelo foco em problemas de configuração que podem resultar em uma vulnerabilidade

### CVSS
- Common Vulnerability Scoring System
- Representa uma pontuação numérica para refletir a gravidade de uma vulnerabilidade
- A pontuação varia de 0 a 10 com classificações qualitativas 

## Análise de vulnerabilidades

- Avaliam vulnerabilidades conhecidas e conformidade em Sistemas Operacionais, Aplicações, Servidores de Aplicações, Protocolos
- Podem ser conduzidos de forma manual e/ou automatizados 
- Soluções
    - Nessus
    - OpenVAS
    - Nexpose
    - W3AF
    - Acunetix
    - Defender for Cloud
    - CSPM
    - Quallys
    - BurpSuite
    - Nmap

## Pentest

- Teste de intrusão
- Metodologia de teste em que os testadores visam componentes computacionais individuais ou o aplicativo como um todo para determinar se vulnerabilidades podem ser exploradas para comprometer o aplicativo, dados ou recursos de ambiente

- As auditorias de terceiros são conduzidas por ou em nome de outra organização

- No caso de uma auditoria de terceiros, a organização que inicia a auditoria geralmente seleciona os auditores e projeta o escopo da auditoria

## DevSecOps

- DEV
    - Aumentar o valor para o negócio
    - Agilidade para inovar
    - Requisitos funcionais
- OPS
    - Proteger valor para o negócio
    - Estabilidade do ambiente
    - Requisitos não funcionais
- SEC
    - Segurança integrada e automatizada no Pipeline
    - Mitigação de riscos de segurança no SDLC e do produto
