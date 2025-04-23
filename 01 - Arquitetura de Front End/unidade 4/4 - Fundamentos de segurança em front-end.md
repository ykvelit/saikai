# Fundamentos de segurança em front-end

- Duas esferas de análises
    - Boas práticas de desenvolvimento
    - Ferramentas
- OWASP
    - Open Web Application Security Project
    - Organização sem fins lucrativos referência em segurança mundialmente reconhecida por disseminar conhecimentos sobre segurança em projetos web
- OWASP TOP TEN
    - Documento de padronizado para desenvolvedores/pessoas ligadas a segurança de aplicações web.
    - Representa um vasto consenso sobre os riscos de segurança mais críticos para aplicações web
    - [Documentação completa](https://owasp.org/www-project-top-ten/)

## Boas práticas de front-end

### Injection

- Inserção de scripts SQL maliciosos através de campos de formulários mal validados
- Prevenção
    - Validação dos campos de formulário e dupla validação com o schema da API de destino
- [Saiba mais](https://owasp.org/www-project-top-ten/2017/A1_2017-Injection)

### Cross-Site Scripting

- Execução de scripts maliciosos com o objetivo de roubar informações
sensíveis do usuário
- Prevenção
    - Sanitização de HTML em campos de formulário 
    - [DOMPurify](https://github.com/cure53/DOMPurify)
- [Saiba mais](https://owasp.org/www-project-top-ten/2017/A7_2017-Cross-Site_Scripting_(XSS))

### Using Components with Known Vulnerabilities

- Utilização de componentes ou bibliotecas na aplicação com vulnerabilidades conhecidas
- Prevenção
    - Atualização dos pacotes npm
    - Utilização do comando `npm audit` para checagem de pacotes instalados com vulnerabilidades conhecidas
    - Utilização de ferramentas para detecção de vulnerabilidades em dependências
- [Saiba mais](https://owasp.org/www-project-top-ten/2017/A9_2017-Using_Components_with_Known_Vulnerabilities)

### Insufficient Logging & Monitoring

- Impossibilidade de monitorar a aplicação, uma vez que ataques ou comportamentos suspeitos possam estar acontecendo sem o consentimento
do time de desenvolvimento
- Prevenção
    - Utilização de ferramentas de log em tempo real
        - [New Relic](https://newrelic.com/)
        - [Sentry](https://sentry.io/welcome/)
- [Saiba mais](https://github.com/OWASP/Top10/blob/master/2017/en/0xaa-logging-detection-response.md)

## Ferramentas

- [Horusec](https://horusec.io/site/)
    - Ferramenta integrada ao VS Code para detecção de vulnerabilidades no código
- [npm audit](https://docs.npmjs.com/cli/v7/commands/npm-audit)
    - Comando para rodar no terminal com objetivo de identificar pacotes instalados com vulnerabilidades conhecidas;
- [Verdaccio](https://verdaccio.org/)
    - Hospedagem própria de pacotes npm;