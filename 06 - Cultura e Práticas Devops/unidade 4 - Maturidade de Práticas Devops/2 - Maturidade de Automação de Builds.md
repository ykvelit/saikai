# Maturidade de Automação de Builds

- A automação de builds é prática essencial para garantir que os executáveis dos seus produtos sejam gerados de forma consistente, em base diária

- Esta prática busca evitar o problema comum do código funcionar apenas máquina do desenvolvedor, fornecer executáveis sólido a qualquer momento e reduzir o trabalho manual gasto para gerar executáveis

## 1 - Inicial

- Não temos consciência sobre automação de builds
- Os processos são manuais
- Não temos nenhum automação de testes
- Dependemos das IDEs para compilar o código
- A qualidade é completamente dependente do artesanato individual
- Aqui ouvimos “Na minha máquina funciona” com mais frequência que gostaríamos

## 2 - Consciente

- Temos consciência sobre o processo de automação de builds
- O processo de trabalho de construir builds está emergindo 
- Temos já experimentos em curso com ferramentas como maven, gradle, npm, yarn e não dependemos mais das IDEs para compilar o código
- Estamos começando a testar ferramentas de pipelines de automação de builds
    - GitLab
    - GitHub Actions
    - Azure Devops
- A automação de testes de unidade começa a ser discutida
- A instrumentação do processo de builds ainda não existe e não temos métricas desse processo

## 3 - Gerenciado

- Temos uma suíte de ferramentas para pipelines de builds definido e que suporta o processo de trabalho
- Os builds rodam em base diária, mas ainda temos problemas de qualidade devido a baixa automação de testes ou políticas pobres de gestão de configuração
- Os esforços de aumento da cobertura de testes estão a pleno vapor
- Introduzimos processos técnicos sólidos nos builds, como verificação de qualidade de código ou segurança
- Os resultados começam a surgir, mas ainda não são plenamente efetivos
- Podemos ficar meses ou trimestres aqui até que tenhamos larga automação de testes e mais frequência de builds sólidos

## 4 - Quatitativamente Gerenciado

- Entramos no terreno da Integração Contínua
- Grande frequência de builds e os builds tem processos sólidos de verificação de qualidade de código, segurança e automação de testes
- Abordagens TDD e BDD são comuns para suportar a automação de testes
- A cobertura de código excede em muitas empresas 80%, fornecendo muita solidez para melhorias e inovações
- A instrumentação é sólida
    - Podemos demonstrar a redução de horas humanas, do tempo de entrega e defeitos em produção