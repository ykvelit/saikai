# Atividades

## Estudo de Caso - Aplicação de Práticas Técnicas, Processo e Culturais.
A ACME, uma das mais proeminentes empresas varejistas do Brasil, com sede no Rio de Janeiro e presença expressiva em todas as regiões do país, está enfrentando desafios significativos. Sua infraestrutura de TI, uma herança de décadas de crescimento e aquisições, se tornou arcaica e complexa, resultando em custos operacionais significativos e dificuldade em se manter competitiva no cenário digital emergente.

Hoje ela se encontra no olho do furacão devido a uma série de desafios de TI. Há seis meses, durante a Black Friday, a ACME sofreu uma crise inimaginável. Um vazamento em seu sistema de e-commerce permitiu que hackers roubassem dados de cartões de crédito de milhares de clientes. Esta falha gerou uma perda significativa de confiança por parte dos clientes, além de um dano considerável à reputação da marca. As repercussões financeiras do incidente ainda são sentidas, com a empresa enfrentando uma onda de reembolsos e litígios.

Como se isso não fosse suficiente, a ACME sofreu outro golpe no Natal. Sua infraestrutura própria, juntamente com processos de implantação ineficientes, não conseguiu lidar com a avalanche de pedidos do período natalino. Milhares de presentes de Natal não foram entregues a tempo, causando um verdadeiro furor entre os consumidores e mais publicidade negativa para a ACME.

No dia a dia, os desafios da ACME persistem. Seus clientes estão constantemente frustrados com a lentidão e instabilidade do aplicativo móvel da ACME, enfrentando carregamentos demorados e travamentos frequentes. Isso resulta em uma experiência ruim para o cliente, e também limita o potencial de vendas do aplicativo.

Internamente, o clima é de tensão e frustração. As equipes de TI e desenvolvimento sofrem com o peso de um código legado pesado e processos lentos e burocráticos. Comentários expressos pelos funcionários, como Pedro, um desenvolvedor veterano, são cada vez mais comuns: "Estamos correndo em uma esteira, nos esforçando, mas estamos parados no mesmo lugar. Nossas ferramentas são desatualizadas, nossos processos são lentos, e não temos voz ou poder de mudar as coisas".

No aspecto técnico, a ACME opera uma combinação de sistemas legados e tecnologias emergentes. A empresa gerencia desde sistemas de ponto de venda baseados em mainframes até plataformas de comércio eletrônico construídas com arquiteturas de microserviços. A integração desses sistemas diversos se tornou um desafio considerável. Além disso, a entrega e estabilidade do software têm sido prejudicadas pela falta de práticas ágeis e DevOps.

Do ponto de vista de negócios, o cenário competitivo está se transformando rapidamente. Novos competidores digitais estão surgindo e os padrões de comportamento do consumidor estão mudando. A ACME precisa se adaptar mais rapidamente para atender às expectativas dos clientes e manter sua participação de mercado.

## Desafio Devops

Diante desse cenário, peço que você considere abordagens potenciais de DevOps que poderiam ser implementadas na ACME para resolver esses problemas. Em particular, vocês devem analisar como as capacidades técnicas do Capítulo 1 (ex. infraestrutura como código, integração contínua, entrega contínua, monitoramento e observabilidade) e as capacidades de processo e cultura do Capítulo 2 (ex. colaboração entre desenvolvimento e operações, aprendizado contínuo, automação de processos) podem ser aplicadas.

Por favor, traga um racional para a escolha de cada prática e explique como ela pode ajudar a ACME a superar seus desafios atuais. Lembre-se de citar explicitamente as capacidades técnicas e de processo/cultura em sua resposta.

Segue aqui um exemplo da resposta esperada, para uma prática específica.

Nome da prática: Infraestrutura com código

Tipo de Prática: Técnica

Racional: A ACME enfrenta desafios na gestão eficiente de sua infraestrutura heterogênea, que é composta por sistemas legados e tecnologias emergentes. Implementar o IaC pode proporcionar um gerenciamento mais eficaz e sistemático da infraestrutura, ajudando a ACME a superar esses desafios.

Benefícios: A Infraestrutura como Código permitirá à ACME automatizar o provisionamento e a configuração de seus servidores, resultando em economia de tempo e redução de custos operacionais. A infraestrutura se torna mais previsível e confiável, e a colaboração entre as equipes de desenvolvimento e operações é facilitada, pois ambos terão uma compreensão clara e compartilhada do ambiente de infraestrutura.

Exemplos de Tecnologia: A ACME poderia utilizar ferramentas como Terraform, Ansible ou Chef para implementar a Infraestrutura como Código. Por exemplo, o Terraform permite que a ACME defina e forneça infraestrutura de data center usando uma linguagem declarativa simples. O Ansible pode ser usado para automação de TI, incluindo provisionamento, configuração de sistemas, implantação de aplicações e orquestração. O Chef permite gerenciar infraestrutura como código, desenvolvendo 'cookbooks' e 'recipes' que descrevem como os recursos de infraestrutura devem estar em um formato de código que pode ser versionado e testado.

Observações adicionais: A transição para a Infraestrutura como Código pode exigir um investimento inicial significativo da ACME em treinamento e adaptação a novas ferramentas e processos. No entanto, a longo prazo, a adoção da IaC pode trazer benefícios substanciais em termos de eficiência operacional, redução de custos e confiabilidade da infraestrutura.

Por favor, aplique o mesmo formato ao considerar outras práticas de DevOps para a ACME, e se a prática for técnica, não se esqueça de incluir exemplos de tecnologias que podem ser utilizadas.