# Automação de Testes

- Automação de testes é peça fundamental nos processos DevOps

- O que deve ser automatizado ?
    - Velocidade
        - Unitário > Serviço > UI

    - Custo
        - Unitário < Serviço < UI

    - Quantidade
        - Unitário > Integração > Componente > End-to-end > Exploratório

## Testes em produção

- Ambientes produtivos podem ter pipelines para proteção de novas publicações
- Tipicamente testes preparados para leituras e/ou gravações que não irão gerar impacto em dados reais
- Chamados de “smoke tests”