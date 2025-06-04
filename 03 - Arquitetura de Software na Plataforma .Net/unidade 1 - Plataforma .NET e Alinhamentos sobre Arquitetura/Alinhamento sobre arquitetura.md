# Alinhamento sobre Arquitetura de Software

## O que é ?

- Desenho técnico 
- Organização do software e suas ligações
- Definição de protocolos
- Padrões de projeto e de comunicações

## Histórico da arquitetura de software

- Etapa 1
    - Caixa única
    - Tudo gerenciado pelo software
        - Armazenamento de dados
        - Regra de negócio
        - Relatórios e análises 
        - Interface com o usuário

- Etapa 2
    - Separação do banco de dados
    - Duas camadas
    - Dados compartilhados e distribuído

- Etapa 3
    - Separação da interface, regra de negócio e banco de dados
    - 3 camadas

- Etapa 4
    - Separação completa de cada componente 
    - Barramento de serviços
        - APIs
        - Comunicação e protocolos
    - Conjunto de interfaces (mobile, web, smart watch, sensores etc)
    - N camadas
    - Cortes por tecnologia

- Etapa 5
    - Microsserviços
    - Divisão por módulos

## Qual o papel do arquiteto ?

- Dado um determinado projeto e cenário, escolher o melhor desenho possível
    - Melhor arquitetura e infraestrutura
    - Conhecimento de negócio

- É só escolher o mais moderno ? Escolher a tendência ? 
    - Não

- Alguns fatores que influenciam 
    - Demanda de escala do projeto
        - Número de usuários
    - Complexidade do negócio
        - Software orientado a dados
    - Infraestrutura que o sustentará
        - Analisar o cenário, como em um IoT os dados devem ser pequenos
    - Interfaces com o usuário
        - Web
        - Smart Watch
        - Mobile
    - Ciclo de vida de um projeto
    - Sustentação e manutenção do código

## Acoplamento e coesão

- Baixo acoplamento
    - Dependência entre os elementos

- Alta coesão
    - Quão especializada é cada parte, um único e bem definido objetivo

## Arquitetura e engenharia

### Engenharia

- Engenharia sabe o modo de fazer
- Processo de criação do software
    - Metodologia Ágil
    - Entregas contínuas
    - Documentação
    - Tarefas
    - Comunicação com usuários

### Arquitetura

- Arquitetura define como fazer
- Técnica de desenho de software
    - Padrões de Projeto
    - Frameworks
    - Protocolos

### Infraestrutura

- Servidores (Nuvem, Containers, Serviços)
- Redes / Telecom (Lora, LPWA, Wi-Fi, 4G, Fibra Óptica)
- Interfaces (SmartPhones, Computadores, Wearables, Coisas, Sensores, etc)

## Padrões de projetos

- Arquitetura é parcialmente empírica
    - Eu já vi este cenário em outro projeto...

### Padrões de criação

- Abstraem e adiam a forma com que os objetos são criados
- Ajudam a tornar um sistema independente de como seus objetos são criados, compostos e representados

- Singleton
    - Garante a existência de apenas uma instância de uma classe, mantendo ponto global de acesso

### Padrões estruturais

- Como as classes e objetos são compostos
- Organização interna das classes

- Business Delegate
    - Separar a camada de apresentação da camada de negócios, reduzir o acoplamento entre as camadas

### Padrões comportamentais

- Delegação de responsabilidade
- Padrões de comunicação entre objetos

- Command
    - Encapsular toda informação necessária para executar uma ação

## Arquiteto .NET

- Boas notícias
    - Arquiteto de Software é um profissional muito valorizado

- Más notícias
    - O mundo de arquitetura de Software está mudando (mais uma vez), é preciso reaprender
    - Fronteira prestes a se extinguir entre Software e Infraestrutura (DevOps)
    - O conjunto de possibilidades só cresce

### Trabalho

- Principais funcionalidades e cenário do projeto
- Desenho da arquitetura de software em alto nível
- Desenho da infraestrutura para suportar
- Padrões de projeto utilizados
- Tecnologias e frameworks .NET
- Protocolos de comunicação
- Justificativas de cada escolha comparando com outras possibilidades
- Apresentação e debate

### Cenários 

#### Caso 1 - Alagamentos em Cidade

- Sensores de chuva e alagamento espalhados pela cidade
- Informações disponíveis em tempo real para o cidadão via App e Web
- Plataforma de gestão de alertas para Defesa Civil
- Cliente: Cidade de São Paulo
- Infraestrutura dos sensores rede LPWA

#### Caso 2 - Microsserviços

- Software a sua escolha com utilização de Microserviços
- Negócio divisível por contexto
- Infraestrutura de containers

#### Caso 3 - Hospitalar

- Hospitalar paperless, sem utilização de papel
- Operação de missão crítica: internações, prescrições
- 10 unidades hospitalares interligadas por FO, total de 400 leitos de internação e 200 mil pacientes atendidos por mês

#### Caso 4 – StartUp de Educação

- Software de gestão educacional integrada com Pais e Familiares dos alunos
- Em fase de validação de mercado, é preciso construir de forma rápida e barata a versão inicial
- Software multiusuários pode ser utilizado pelos seguintes atores via App (3G, 4G): Professores, Pais e Alunos; e via Web: Gestores e Administrativo
- A primeira fase pretende-se entregar funcionalidades mais básicas e, se o projeto for validado será construída a plataforma de gestão

### Resultado esperado

- Conhecer tecnologias .NET
- Melhorar habilidades de desenho de software
- Experiências de cenários reais (principalmente exemplos de não sucesso)