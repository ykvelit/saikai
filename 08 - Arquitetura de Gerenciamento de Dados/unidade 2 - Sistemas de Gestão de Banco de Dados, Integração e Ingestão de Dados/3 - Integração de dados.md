# Integração de dados

## Tipos de integração de dados

### Dados de sistemas transacionais

- Estruturados para suportarem o armazenamento  e processamento 
de dados de transações de negócio  como vendas,  compras, pagamentos,  reservas, etc

- Dados devem estar em conformidade  com o ACID (Atomicidade, Consistência,  Isolamento e Durabilidade)

- Otimizados para operações de criação, escrita e leitura

- Devem ter sempre uma referência temporal associada a cada 
transações e ligação com todos os dados de contexto dessa 
transação

### Integração entre sistemas transacionais

- Garante a comunicação de dados entre produtos ou sistemas de 
dados

- As integração podem ser:
    - Orientadas a evento
        - Mensageria
    - Consulta transacional de dados
        - API REST
    - Consulta de histórico e/ou dados de conceitos
        - API GraphQL
    - Integração direta entre bancos

### Dados para Analytics e Ciência de Dados

- Repositório  de dados que reúne todos os dados da companhia  de forma centralizada

- Constituído  por camadas para preparação e disponibilização  de dados para diferentes finalidades

- Dados não são orientados a transação e sim a consulta  de grandes volumes

- Podem ser constituídos  por Data Lake, Data Warehouse ou Data Lakehouse

### Integração entre camadas do repositório de dados

- Processamentos de dados devem ser garantidos para transitar o dados entre as camadas de um repositório  de dados

- Essa transação deve acontecer orientada à transação ou bloco bloco de dados por processos batch

- Entre cada camada os dados passam por processos de consolidação,  limpeza, consistência,  controle de qualidade  e orientação aos indicadores  de negócio

### Integração entre sistemas transacionais e repositórios de dados

- Processamentos de dados para garantir que todas as informações que são geradas, alteradas ou inativadas  nos sistemas transacionais são integradas  nos repositórios  de dados da plataforma

- Os dados podem ser integrados via streaming (quase tempo real) ou via Batch (por operações agendadas ou programadas em função de outros eventos)

- Carregamento de dados em Batch pode acontecer por ETL (Extract, Transform  and Load) ou por ELT (Extract, Load and Transform)

## Soluções de publicação/subscrição de eventos

- Mensageria

Microserviço Produtor -> Mensagem -> Broker -> Mensagem -> Microsserviço consumidor

## Soluções IoT

- IoT ("Internet of Things") 
    - Internet das coisas 

- É uma metodologia para interligar uma ou várias rede de objetos na nossa vida cotidiana

- O objetivo da Internet das Coisas é de interligar objetos, e trocar informações para cumprir tarefas para seus usuários de uma forma integrada