# SLDC: Release e Deploy

- Esta fase adota tecnologias de RASP

- Caracterizada pela forte adoção de Infraestrutura como Código (IaC)

- Gestão do ambiente das aplicações por gestão de configuração

- Segurança de gerenciadores de contêineres, dos contêineres e imagens de contêineres

- Adoção de Pentest

## RASP

- Runtime Application Self-Protection

- Tecnologia de segurança construída dentro de um aplicativo ou ambiente de tempo de execução do aplicativo usado em ambiente de Homologação e Produção

- Pode controlar a execução de um aplicativo para detectar e prevenir ataques em tempo real com baixíssimo (ou inexistente) falso-positivo 

- Protege o aplicativo contra explorações implementado segurança em tempo de execução do aplicativo analisando o comportamento do aplicativo e o contexto do comportamento

- Amplamente adotado para proteção de aplicações móveis críticas

- Pode funcionar nos seguintes modos
    - Desligado
    - Monitoramento
    - Bloqueio (comportamento)
    - Bloqueio Perimetral (regras pré-determinadas)

- O RASP deve ser integrado no Pipeline no ciclo de desenvolvimento de sistemas 

- Abordagens de segurança RASP
    - Servlet Filters, SDK e Plugins
        - Filtros ou plugins são adicionados para analisar as solicitações HTTP e inspeção do payload para bloqueio
    - Instrumentação binária
        - Assim como no IAST, para monitorar a aplicação
    - Substituição de JVM
        - Pode substituir bibliotecas padrão como JAR ou JVM por uma camada RASP
    - Virtualização
        - Uma cópia da aplicação é gerada e regras são estabelecidas e replicadas na aplicação original

- Virtualização adota uma cópia da aplicação é gerada e regras são estabelecidas e replicadas na aplicação original

- O RASP permite que as organizações implantem software por meio do conceito de Secure by Default

- Principais vulnerabilidades e ameaças protegidas
    - Command injection
    - Clickjacking
    - Cross-Site Scripting (XSS)
    - Cross-Site Request Forgery (CSRF/XSRF)
    - Database Access Violation (Advanced SQLI)
    - HTML injection
    - HTTP method tampering
    - HTTP response splitting
    - Insecure Cookies
    - Insecure transport
    - JSON injection
    - Large requests
    - Logging sensite information
    - Malformed Content-Types
    - OGNL injection
    - Path traversal
    - SQL injection
    - Unauthorized network activity
    - Uncaught exceptions
    - Unvalidated requests
    - Vulnerable dependencies
    - Weak authentication
    - Weak browser cache management
    - Weak cryptograph & cliphers
    - XML external entity injection (XXE) 
    - XML injection