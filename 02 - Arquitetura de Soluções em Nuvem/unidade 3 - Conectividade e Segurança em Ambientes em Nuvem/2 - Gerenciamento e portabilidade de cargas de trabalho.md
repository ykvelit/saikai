# Gerenciamento e portabilidade de cargas de trabalho

## Migrando soluções para cloud

- O desafio de gerenciar cargas de trabalho de forma previsível é o grande desafio em um ambiente de nuvem distribuído onde deveremos considerar novos desafios e novas tecnologias

- Conhecemos os contextos de funcionamento da nuvem como a nuvem pública, privada e nuvem híbrida (quando combinamos a nuvem pública e privada) e vimos que o novo horizonte de computação é multicloud

- Com esta visão, pode-se implantar e operar cargas de trabalho em todos os contextos de nuvem para atender às expectativas dos clientes quanto à disponibilidade e desempenho das ferramentas de software das quais eles dependem todos os dias

- Gerenciar softwares e cargas de trabalho de forma simples é o desejo das empresas quando procuram soluções de gerenciamento de nuvem e elas podem oferecer detalhes de plataforma de baixo nível, permitindo que as empresas se concentrem em suas necessidades estratégicas

- Sistemas ainda são baseados na boa e velha lógica matemática, as bases de dados também compartilham as mesmas tecnologias

- As questões naturais que surgem desta discussão são
    - Será que minha aplicação executará na sua nuvem tudo corretamente?
    - Ficará mais caro ou mais barato?
    - Uma parte ficará na sua nuvem e outra parte em outro CSP, será que vai funcionar?
    - Minha equipe sabe operara uma nuvem mas e como será com este novo recurso?
    - Comprei um montão de equipamentos, o que faço com todo esse aparato tecnológico que tenho?

- Quem está envolvido em projetos de adoção de nuvem, principalmente quando o workload já foi construído em outra arquitetura precisa se adequar a essa nova realidade

- É necessário conhecer bem mais do que features e functions de seu provedor

- Começam as perguntas dos arquitetos
    - Qual o formato que vou adotar edge? Container?
    - Qual o tipo de storage mais apropriado?
    - E a interconexação qual utilizar?
    - Utilizo este serviço em SaaS ou desenvolvo algo próprio?
    - Levo isto para a nuvem ou deixo aqui no meu ambiente?

### Site Reliability Engineering (SRE) 

- É um time que vai tratar da confiabilidade das operações de TI
- Usam software como uma ferramenta para gerenciar sistemas, solucionar problemas e automatizar tarefas operacionais e, padronização e automação são dois componentes importantes do modelo de SRE
- Como o DevOps, a SRE tem como foco a cultura e os relacionamentos e têm como objetivo aproximar a operação do desenvolvimento para acelerar a entrega de serviços

### Cargas de trabalho ou workloads 
- São programas executados em uma nuvem privada, um mainframe ou em uma nuvem pública e, em nuvem, remete mais do que a várias VMs executando em unidades computacionais

- Temos envolvido neste conceito capacidades de processamento, interação com storage, interconexão com redes internas e externas, isolamento de unidades de processamento e operações de automação

- As cargas de trabalho compreendem o conjunto completo de software usado por pessoas ou outro software e mudam ao longo de seu ciclo de vida, adicionando recursos

- Nesta mudança, podem estar envolvidos número crescente de usuários, interação com outras cargas de trabalho e principalmente, a evolução dos recursos de computação oferecendo novos recursos em novos contextos em diferentes níveis de preços

- A dimensão arquitetura de aplicações passa a ser fundamental neste tipo de análise que envolve é a integração corporativa

- Os CSP’s oferecem modelos de computação, networking, storage, segurança e até plataforma das mais distintas formas

- Isto acontece porque cada carga de trabalho tem a necessidade de isolamento, tolerância a falhas, operar e escalar conforme a demanda e de consumir recursos computacionais da forma mais otimizada

- O grande benefício proporcionado pela nuvem é a automatização dos fluxos de trabalho onde e se não forem escolhidos e acompanhados de perto podem fazer um estrago na fatura da subscrição contratada

#### Workload Estático

- A aplicação apresenta um perfil cuja previsão da carga de trabalho é sempre a mesma da carga executada e, como não possui crescimento e nem decrescimento de demanda a tendência é que este tipo de carga não tire muito benefício de ambiente pago por uso por se manter sempre constante

#### Worload Periódico

- É o perfil de aplicações mais presente no nosso dia a dia e visualizando o consumo, são sistemas que ficam aguardando parte do período de disponibilização de recursos e que somente quando necessário lançam mão de processamento otimizando custos de utilização

#### Workload “Once-in-Lifetime”

- A repetição de picos de consumo ocorre em eventos conhecidos (como o Natal, por exemplo) e possibilita que a preparação de recursos seja planejada e alocada muitas vezes manual e dirigida nos recursos da nuvem

#### Workload Imprevisível

- É um tipo de pico demandado por situações não previstas de processamento (como ataques a websites) e neste caso existe alocação/desalocação de recursos de nuvem de forma automatizada e com alertas para apontar anomalias

#### Workload de Mudança Contínua

- Este tipo de carga está propensa transformado em a ser outra aplicação ou crescerá conforme a demanda deutilização

### O que não levar para nuvem 

- Assim como algumas cargas de trabalho são apropriadas para executar a nuvem, outras não são

- Mesmo que estas cargas de trabalho possam ser inadequadas para a nuvem precisamos ter em mente que os fornecedores de nuvem estão oferecendo cada vez mais ambientes de nuvem especializados para atender aos requisitos de diferentes tipos de cargas de trabalho

- Aplicativos que não foram arquitetados para a nuvem: aplicativos grandes e monolíticos que foram projetados para servidores físicos não poderão aproveitar os recursos da nuvem, como dimensionamento horizontal para fornecer melhor desempenho

- Esta definição do que vai e o que não vai para o ambiente de nuvem, tem que englobar a análise sobre a continuidade de negócios, com movimentação e cópia de recursos da nuvem, criação e gerenciamento de políticas para backups e gerenciamento de interrupções e falhas

#### Cargas de trabalho que precisam de armazenamento de alto desempenho

- Como os dados precisam ser acessados muito rapidamente, essas cargas de trabalho podem não ser adequadas para a nuvem, onde você depende da Internet para obter velocidade de rede

#### Cargas de trabalho de aplicativos que exigem latência muito baixa

- Cargas de trabalho legadas não foram arquitetadas para serem executadas em um ambiente de computação distribuído, principalmente web ou cliente servidor

#### Aplicativos regulamentados que exigem segurança e auditoria

- O armazenamento em nuvem pública é quase sempre armazenado em data centers que não permitem visitantes, os dados auditáveis devem ser armazenados em um data center local ou de terceiros para que os auditores possam visitar o armazenamento para verificar se as medidas de segurança estão em vigor
