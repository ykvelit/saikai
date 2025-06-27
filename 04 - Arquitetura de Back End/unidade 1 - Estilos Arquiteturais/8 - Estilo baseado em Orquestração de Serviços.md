# Estilo baseado em Orquestração de Serviços

- O estilo arquitetural baseado em orquestração de serviços é uma abordagem onde um componente central (o orquestrador) coordena e controla a execução de vários serviços para realizar um processo de negócio completo. Ao contrário da coreografia, onde os serviços interagem de forma descentralizada, na orquestração o controle do fluxo é centralizado.

## Principais Características

- Controle Centralizado
    - Um orquestrador (como um motor de workflow ou processo) define e executa a lógica de integração entre os serviços.

- Sequenciamento de Atividades
    - O orquestrador chama os serviços em uma ordem específica, conforme regras de negócio e lógica de processo.

- Gerenciamento de Estados
    - O orquestrador mantém o estado da execução do processo, podendo realizar compensações ou retentativas.

- Integração Sincronizada ou Assíncrona
    - Pode orquestrar serviços via chamadas REST, SOAP, mensageria ou eventos.

## Vantagens

- Clareza no Fluxo de Negócio
    - Fácil visualizar e manter os processos de ponta a ponta.

- Reuso de Serviços
    - Serviços são modulares e podem ser reutilizados em diferentes orquestrações.

- Gestão Central de Falhas e Compensações
    - O orquestrador pode implementar padrões como Saga para garantir consistência eventual.

- Automação e Monitoramento
    - Facilitado por motores de processo com suporte a BPMN (como Camunda ou Zeebe).

## Exemplos de Aplicação

- Processos de negócio com múltiplos passos (ex: abertura de conta, processamento de pedido)
- Sistemas de BPM (Business Process Management)
- Arquiteturas orientadas a serviços (SOA) tradicionais

## Tecnologias Comuns

- Camunda, Zeebe
- Apache Airflow (para orquestrações baseadas em tarefas)
- Azure Durable Functions, AWS Step Functions
- JBoss jBPM, Netflix Conductor