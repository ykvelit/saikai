# Maturidade de Automação de Entregas

- A automação das entregas é uma prática que buscar garantir que o processo de promoção do executável para os ambientes de testes, homologação e produção sejam automatizados e assim tornados consistentes e eficientes

## 1 - Inicial

- Não temos consciência sobre automação de entregas
- Aqui ouvimos “Na minha máquina funciona” com mais frequência que gostaríamos
- A promoção de builds é manual
- Os processos de transporte de esquemas e dados nos bancos de dados são morosos
- Temos muitas instabilidades em produção
- Não é incomum que o transporte para produção demore horas ou dias

## 2 - Consciente

- Temos consciência sobre o processo de automação de entregas
- Ferramentas como Chef, Puppet ou Azure Pipelines começam a ser experimentadas
- O conceito de conteinerização de ambientes começa a ser discutido e ferramentas como Docker começam a ser usadas
- Promoções do ambiente de integração para ambiente de testes começam ser realizados de forma automatizadas

## 3 - Gerenciado

- Temos uma suíte de ferramentas para promoção de builds
- Os processos de gestão de mudanças ITIL começam a ser incorporados nas ferramentas de automação de entregas
- A promoção de contêineres é usual já e temos propriedade no uso de contêineres
- Introduzimos processos técnicos sólidos nos builds, como verificação de qualidade de código ou segurança
- Os resultados começam a surgir, mas ainda não são plenamente efetivos
- Ainda podemos lutar com o transporte automatizados de dados de banco de dados e dependências de outras aplicações
- Podemos ficar meses aqui até que tenhamos resolvido a automação do transporte de dados e dependências de outras aplicações

## 4 - Quantitativamente Gerenciado

- Entramos no terreno do CD (Implantação Contínua e Entrega Contínua)
- Entregamos na frequência demandada pelo negócio
- O transporte de builds, esquema e dados são todos automatizados
- Conteineres são usados em largas escala e já temos repositórios privativos implementados
- Os processos de entrada em produção são sólidos, inclusive a reversão de builds
- Práticas como implantações canários, implantações azul-verde e testes A/B são suportadas sem maiores problemas
- Medimos o efeito econômico da melhoria de qualidade, tempo e custos associados aos processos de entrega