# IAST

- Interactive Application Security Testing

- IAST adota a Instrumentação de Software como forma de operação

- Uma porção de código é adicionada ao aplicativo para coletar dados e realizar análises, integrando lógica de coleta ao código

- Soluções de APM (Application Performance Monitoring) adotam instrumentação de código, tais como Newrelic, Datadog, Dynatrace, Splunk

- A instrumentação de software pode causar aumento de CPU e lentidão

- IAST só deve ser usado em ambiente não produtivo

- Tecnologia de teste de segurança em tempo de execução que identifica e diagnostica vulnerabilidades, monitorando continuamente em busca de vulnerabilidades (IAST adota um método Gray-Box)

- O IAST pode analisar o código em busca de vulnerabilidades em um aplicativo enquanto ele é executado por um teste automatizado ou outra atividade que possa acessar a funcionalidade do aplicativo 

- Pode encontrar vulnerabilidades conhecidas e não conhecidas

- Geralmente, não possui falso-positivo 

- IAST analisa o código em busca de vulnerabilidades de segurança e as relata em tempo real

- Atua dentro do aplicativo (instrumentação de software), o que o torna diferente tanto da análise estática (SAST) quanto da análise dinâmica (DAST). O IAST testa apenas o que for especificado pelo teste funcional, em vez de testar todo o aplicativo ou código

- O IAST tem acesso ao código e as requisições HTTP; portanto, ele pode executar SAST em cada linha de código e pode executar DAST em cada solicitação e resposta. IAST é um superconjunto de ferramentas SAST e DAST

- IAST Ativo (Partial IAST): Combina um scanner da Web com um agente que funciona dentro do servidor de aplicativos que hospeda o aplicativo para fornecer detalhes de análise adicionais, como o local da vulnerabilidade

- IAST Passivo (IAST Full): Precisa apenas de um componente de detecção que é parte do servidor de aplicativos como um agente de tempo de execução

- IAST deve ser integrado com ferramentas de ITSM ou de gestão de projetos de software, como JIRA, Azure Boards, ServiceNow etc. para abrir tickets e gerar backlog

- IAST deve ser ajustado para encontrar dados que lidam com aspectos legais e regulatórios como GDPR, PCI-DSS, LGPD

- IAST deve fornecer meios de correção adequados e fácil compreensão para os utilizadores

- IAST deve suportar as linguagens de programação e frameworks utilizados pela organização

## Principais vulnerabilidades encontradas com IAST

### Injection

- SQLi
- Reflected XSS
- Path Traversal
- LDAP Injection
- Log Injection
- Execução de código inseguro
- Injeção de Entidade Externa XML (XXE)
- Header Injection
- Injeção de NoSQL
- Stored XSS
- Command Injection
- Xpath Injection
- Injeção de linguagem de expressão
- Injeção de hibernação

### Http Header

- Cache
- Resposta com cabeçalho de CSP de forma insegura
- Controles Anti-Clickjacking
- HSTS
- Resposta sem cabeçalho de CSP
- Cookie inseguro
- Cabeçalho de resposta sem X-Content-Type
- Cabeçalho com versão de software ativado
- Resposta com cabeçalho de segurança de HSTS configurado de forma insegura e resposta com proteção X-XSS desativada

### Configuração insegura

- Verificação de cabeçalho desabilitada
- Mensagens de erro detalhadas
- Posicionamento JSP inseguro
- Validação de evento desabilitada
- Tempo limite de sessão excessivamente longo
- Modo de validação de solicitação desabilitado
- Comprimento máximo de solicitação grande
- Rastreamento habilitado
- Rastreamento habilitado para ASPX
- Decodificação XML insegura
- Metadados de serviço habilitados
- Validação de solicitação desabilitada

### Parsing

- Entidades externas XML
- DoS de expressão regular
- Redirecionamento não validado
- Vinculação automática não verificada
- Desserialização insegura
- Poluição de parâmetro
- Uso de readLine em fluxos não confiáveis e violação de limite de confiança

### Autenticação e Autorização

- Senha codificada
- Cookie de sessão sem a flag “HttpOnly” e “Secure”
- Protocolo de autenticação inseguro
- Regravação de sessão
- Cadeias de conexão desprotegidas
- Redirecionamento de aplicativos cruzados de autenticação de formulários
- IDs de sessão expirados não regenerados
- Modo de proteção de autenticação de formulários
- Formulários sem prevenção de preenchimento automático
- Incluem modo de proteção do gerenciador de função
- CSRF
- Fraqueza de adulteração de verbo HTTP
- SSR

### Criptografia

- Validação de MAC desativada
- Algoritmos de hash inseguros
- Oráculo de preenchimento
- Algoritmos de criptografia inseguros
- Geração de números aleatórios fracos

## Testes de software e segurança

- Teste de Abuso
- Teste de Intrusão (Pentest)
- Teste Unitário
- Teste de Integração
- Teste de Regressão/Teste de Regressão de Segurança
- Smoke Test Automatizado de Segurança
    - Autenticação
    - Autorização
    - Funções críticas do sistema

- Alguns autores (FOWLER, Susan J. Microsserviços Prontos Para a Produção. NOVATEC. 2017.) recomendam realizar os testes de software antes da revisão de código realizando todo processo de teste em uma Branch separada, fazendo com que o código que for aprovado já foi devidamente testado

- De certa forma, isso reduz o número de revisões em função de eventual refatoração de código em caso de falhas nos testes

- Nesse processo foi considerado o Teste Unitário, Teste de Integração e Teste Fim-a-Fim

- A adoção de microsserviços podem trazer novas perspectivas para lidar com os testes
    - A base da pirâmide sempre deve constituir em escala os testes mais rápidos, caso contrário pode se tornar um antipadrão (snow cone, pirâmide invertida)