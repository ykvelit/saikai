# Observabilidade

- O processo de administração de ambientes de produção tem se automatizado

- As tecnologias para monitoração, registro (logging) e rastreamento permitem observar e analisar eventos diversos em ambientes de software, banco de dados, infraestrutura, eventos de negócio

- Análise de tendências, correlações complexas e capacidade de antecipação também tem sido incorporadas a tecnologias de análise de ambientes

- Processos de observabilidade nascem ainda com os times de desenvolvimento

- Uma boa arquitetura técnica para geração de registros (logs) é essencial para facilitar a análise de problemas e incidentes em produção

- Processos de observabilidade nascem ainda com os times de desenvolvimento

- Uma boa arquitetura técnica para geração de registros (logs) é essencial para facilitar a análise de problemas e incidentes em produção

## Níveis de observabilidade

### Monitoramento

- Instrumentação de um aplicativo para coletar, agregar e analisar registros e métricas para melhorar nossa compreensão de seu comportamento

- O monitoramento inclui tudo, desde observar o espaço em disco, o uso da CPU e o consumo de memória em nós individuais até fazer transações sintéticas detalhadas para ver se um sistema ou aplicativo está respondendo corretamente e em tempo hábil

### Registro (log)

- Os aplicativos emitem um fluxo constante de mensagens de log descrevendo o que estão fazendo a qualquer momento

- Essas mensagens de log capturam vários eventos acontecendo no sistema, como ações com falha ou bem-sucedidas, informações de auditoria ou eventos de saúde

- As ferramentas de registro coletam, armazenam e analisam essas mensagens para rastrear relatórios de erros e dados relacionados

### Rastreamento

- Em um mundo de microsserviços, os serviços estão constantemente se comunicando uns com os outros pela rede

- O rastreamento, um uso especializado de registro, permite rastrear o caminho de uma solicitação à medida que ela se move através de um sistema distribuído