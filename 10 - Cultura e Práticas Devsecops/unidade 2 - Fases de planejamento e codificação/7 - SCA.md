# SCA

- Software Composition Analysis

- SBOM
    - Software Bill of Materials (SBOM) é um inventárioabrangente de todos os componentes de código-aberto como parte dos artefatos  de software, incluindo suas versões e dependências
    - Soluções de SCA geram SBOM e administram automaticamente 
    - Suportam a detecção de vulnerabilidades, conformidade de licenças e auditorias  de segurança

- Realiza um inventário de todos os pacotes constituintes do software por meio do SBOM 
- SCA fornece uma análise profunda de pacotes de código aberto incorporados ao software
- Avalia vulnerabilidades e violações de conformidade quanto ao uso das licenças das dependências
- Geralmente usado com soluções de análise estática de código e integrado ao Pipeline

- Semantic Version
    - X.X.X
    - Major version
        - Break change
        - Mudanças significativas, introdução de novas features, pode causar refatoração de código
        - Pode “quebrar” o software
    
    - Minor version
        - Non-breaking
        - Adição de recursos ou funcionalidades, mantendo a compatibilidade
        - Geralmente não “quebra” o software

    - Patch version
        - Non-breaking
        - Correções de bugs, patches ou pequenas atualizações sem introduzir recursos
        - Geralmente corrige vulnerabilidades

- Ferramentas
    - Synopsys
    - Veracode
    - Checkmarx
    - Snyk
    - SonarQube
    - OWASP Dependency-Check
    - Dependabot