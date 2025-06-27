# Estilo baseado em Pipelines

- É um modelo de processamento de dados em que as tarefas são divididas em estágios (filters) consecutivos, conectados por pipes (tubulações) e executadas em paralelo. As principais caracteristicas dessa arquitetura eincluem a divisão do processamento em estágios, o encadeamento de estágios e a execução em paralela de tarefas em diferentes estágios

- Os estágios em uma arquitetura de ppeline são as etapas discritas pelas quais os dados passam durante o processamento. Cada estágio executa uma parte específica do processamento e passa os resultados para o próximo estágio. Isso permite que várias tarefas sejam executadas simultaneamente, melhorando a eficiência e o desempenho

- Algumas vantagens de utilizar uma arquitetura de ípeline incluem maior eficiência do processamento, desempenho aprimorado, paralelismo e a possibilidade de balanceamento de carga entre os estágios

- Muito utilizado em BI
    - Extração de dados

- ETL
    - Extract
    - Transform
    - Load

- Serveless 
    - AWS Lambda
    - Azure Functions