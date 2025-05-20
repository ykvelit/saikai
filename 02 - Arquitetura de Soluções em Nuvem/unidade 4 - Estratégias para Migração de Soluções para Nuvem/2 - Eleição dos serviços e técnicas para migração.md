# Eleição dos serviços e técnicas para migração

- Uma área diretamente afetada pela nuvem é a disponibilidade do serviço onde quando o produto for acessado ou dependendo da Internet, há uma boa chance de que a nuvem possa ser significativa na criação de valor aos clientes deixando-os satisfeitos

- Monitoramento, segurança, backup e recuperação, conformidade e o conhecimento necessário para gerenciar e otimizar a infraestrutura de nuvem

- Para fazer uma migração precisamos avaliar se os aplicativos e sistemas são aderentes aos padrões abertos e utilizam tecnologias de código aberto para poder aumentar a portabilidade e reduzir a dependência de plataformas proprietárias

## Eficiência

- Lei de Moore
    - Previsão de 1965 de que o número de transistores por chip de silício dobrará a cada ano e com isto, deixa claro que os serviços básicos de TI, como computação e armazenamento, perdem valor rapidamente

- Escalada de eficiência na mão de obra
    - Um exemplo típico é com administradores de banco de dados, que poderão gerenciar x vezes mais bancos de dados na nuvem porque muitas de suas tarefas típicas são tratadas pelo fornecedor da nuvem

- Automatização dos processos manuais
    - É o foco principal do DevOps, ao qual a maioria dos fornecedores de nuvem oferece suporte onde com o processo automatizado de implantação e testes economiza tempo dos administradores de sistema e testadores

- Tempo de deploy e mitigação de erros nas publicações
    - Ainda falando de DevOps é impressionante como a quantidade de erros em produção diminui

## Estratégias de migração

- Em um compilado de melhores práticas vamos falar então dos famos R’s da estratégia da migração para a nuvem

- O início desta abordagem se deu com o Gartner e, os fornecedores de solução foram adaptando o modelo original e propondo melhorias

- Vamos às possibilidades que podem ser avaliadas onde sua utilização é opcional e, a partir daí sua implantação pode levar ao sucesso na migração

- O foco do planejamento deve ser a potencialização da utilização da infraestrutura e a redução do tempo de migração, o custo e o risco

### Modelo de Rs

#### Rehost

- É conhecido como migração lift-and-shift, é o processo em mover seus workloads para nuvem sem modificações. Essa estratégia envolve menor esforço e risco de migração, e é um dos modelos mais utilizados geralmente usando ofertas de infraestrutura como serviço (IaaS)

- É comum ser escolhida por empresas que estão com contrato de data center próximo ao vencimento, precisam migrar rapidamente e não possuem possibilidade de realizar modificações nas aplicações

#### Refactor ou Replataform

- É conhecido como lift-tinker-and-shift, por ajustar um workload para o modelo baseado em PaaS deixando de lado o modelo convencional IaaS

- Nessa estratégia, poucas otimizações são feitas antes de migrar para a nuvem

- Utiliza-se comumente quando temos domínio da infraestrutura que é ofertada com plataforma e alguns serviços podem ser apontados para a oferta de PaaS como bancos de dados por exemplo

#### Retire

- Uma migração de larga escala, quando se analisa toda a infraestrutura atual, é muito comum encontrar aplicações legadas que não são mais utilizadas

- Aproximadamente 5% das aplicações podem ser desligadas completamente e ninguém vai reclamar

- São aplicações que tiveram uma versão nova desenvolvida e deveriam ser desligadas e foram esquecidas. Ambientes de testes e desenvolvimento de aplicações que ficaram esquecidas e continuaram consumindo recursos estão na lista

#### Retain

- É um método que consiste em manter os aplicativos em seu ambiente de origem pois, em alguns casos não há sentido para o negócio migrar uma aplicação porque ela teve uma renovação contratual ou está próxima de ser descontinuada

- Pode também incluir aplicativos que precisam de refactor e tendo a possibilidade de adiar para uma nova avaliação futura

- O esforço maior é identificar quais são estas aplicações e os responsáveis por elas pois desligar algo que alguém, por ventura possa estar utilizando é complicado

#### Relocate

- Com o avanço da tecnologia de virtualização e de containers, criou-se uma nova estratégia, de recolocação das aplicações. Esta estratégia está ligada a identificar características mínimas de compatibilidade de aplicações entre ambientes Docker e virtuais

- Essa estratégia é comumente confundida com a Rehost em alguns casos, porém vale ressaltar que a ideia é levar a aplicação para dentro do container e automatizar o máximo que podemos com tecnologias como o K8’s

#### Rearchitect 

- Se concentra na modificação e na extensão da funcionalidade do aplicativo e na base de código para otimizar a arquitetura do aplicativo para a escalabilidade da nuvem. 
 
- Ligada diretamente à agilidade de inovação da empresa, busca por escalabilidade e aumento desempenho, que seriam difíceis de alcançar utilizando uma arquitetura tradicional

- Um exemplo muito comum, é mudar a arquitetura monolítica para uma arquitetura de microsserviços ou fazer uma implementação de tecnologias serverless

#### Rebuild

- É a abordagem mais radical e leva a modificação do código-fonte de forma a reescrever o aplicativo do zero. A decisão é tomada quando as soluções atuais não atendem às necessidades do negócio ou quando um aplicativo legado não pode ser executado em nuvem

- Aplicativos com tecnologias muito antigas e que não tem suporte nos ambientes em nuvem seguem este padrão principalmente as que tiveram entraram na obsolescência da curva tecnológica

#### Replace

- Aplicativos SaaS podem fornecer toda a funcionalidade necessária para um certo workload a ser migrado.

- Pode ser mais interessante substitui-lo por completo e eliminar o esforço de rearchitect e rebuild da aplicação. 

- Essa abordagem requer pouco esforço, uma vez que só é necessária a carga dos dados existentes no novo workload

- Modernização de plataforma pode ser um exemplo para utilização deste tipo de modalidade