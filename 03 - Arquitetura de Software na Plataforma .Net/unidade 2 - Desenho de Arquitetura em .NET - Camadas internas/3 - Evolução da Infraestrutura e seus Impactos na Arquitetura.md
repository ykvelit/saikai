# Evolução da Infraestrutura e seus Impactos na Arquitetura

## Infraestrutura

- Data center > Nuvem > Híbrido / Container

### Data center

- Compra de equipamentos para data center próprio
- Comum superdimensionamento
- Alto custo de manutenção e atualização
- Demanda diversos profissionais especialistas
- Comum subutilização dos equipamentos
- Comprar para quanto tempo ?
- Custos adicionais
    - Redes
    - Climatização
    - Energia elétrica
    - Segurança física e virtual
    - Geradores
    - No breaks
    - etc

### Nuvem / Virtualização

- Terceirizar data center é abstrair complexidades
- Pool de recursos compartilhados
- Menor subutilização de recursos
- Fácil redimensionamento e expansão
    - Quando existe coragem para fazê-lo

### Containers

- Portabilidade
- Inicialização rápida
- Automatização de cenários extremos
- Foco na aplicação
- Orquestrador cuida de muitos aspectos
- .Net core é feito para containers
    - É possível .NET Framework

## Impactos na Arquitetura

- Para migração para containers é preciso ajustes na arquitetura
- Como implementar micro serviços sem containers? Como fazer deploy manual de muitos serviços paralelos
- Tendência: arquiteto entender de infraestrutura
