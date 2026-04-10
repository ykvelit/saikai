# DAST

- Dynamic Application Security Testing

- Ferramentas DAST são adotadas para avaliar aplicações no estado de execução

- Foco em vulnerabilidades OWASP TOP 10, CWE e CVE

- Pode gerar prova de exploração

- Encontra vulnerabilidades críticas como XSS, SQLi, Command Injection, Code Injection

- Ferramentas DAST podem causar interrupção em serviços, por isso, deve-se adotar na fase de Teste
    - Evitar o uso de DAST em ambiente de Produção tanto na perspectiva de segurança (shift-left) quanto da disponibilidade

- Ferramentas SAST são ditas White-Box e ferramentas DAST são ditas Black-Box

- Deve ser integrado ao Pipeline DevOps principalmente para a fase de Test

- A solução DAST deve ser devidamente configurada para refletir sobre o teste, tais como a linguagem da programação, tecnologias, tipos de avaliações esperadas, entre outros

- A solução de DAST deve suportar scan autenticado e suporte a scan de API 

- A solução de DAST deve suportar Single Page Application (SPA)

- Pode haver problemas com aplicações requerem MFA

- Pode haver problemas com aplicações com muitos formulários

- Pode haver problemas com resoluções de CAPTCHA

- Possui menos falso-positivo que soluções de SAST

- O DAST pode ocorrer sempre durante uma tarefa de implantação em Staging/QA

- O DAST pode ocorrer de forma agendada no Staging/QA

- O DAST pode ser integrado no Pipeline de diversas soluções de integração

- O DAST pode ser integrado no Pipeline de Cloud

- Ferramentas
    - w3af
    - OWASP Zed Attack Proxy
    - acunetix
    - Checkmarx
    - detectify
