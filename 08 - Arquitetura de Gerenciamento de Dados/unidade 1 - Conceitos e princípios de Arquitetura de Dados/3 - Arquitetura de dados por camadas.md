# Arquitetura de dados por camada

## Arquitetura Moderna e Big Data

- Orientada a resultados
- Automatização dos processos
- Flexível nos dados no consumo e no processamento
- Adaptável às mudanças
- Segura
- Inteligente
- Colaborativa

## Os 5Vs do Big Data

- Volume 
    - Grande volume de dados ao nível de tera e peta bytes

- Variedade
    - Dados estruturados, semi-estruturados e não estruturados
    - Vídeos, imagens e aúdio

- Velocidade 
    - Dados produzidos por dispositivos móveis o todo o tempo em vários locais distintos

- Veracidade
    - Importância de garantir que os dados quando salvos e tratados mantêm a representação correta da verdade, do evento original

- Valor
    - Importância de garantir que todos os dados guardados e processados criam valor para quem vai utilizar

## Arquitetura por camadas

- Sistema fonte
    - Sistema que gerenciam os processos de negócio e geram os dados

- Ingestão
    - Métodos de ingestão dos dados para a plataforma
    - ETL, ELT, Pub/Sub, Fila, Api e etc.

- Orquestrador 
    - Serviço que controla os processamentos de dados
    - Hora, método, frequência e etc

- Processamento em Batch
    - Executa os processamentos de forma espaçada no tempo e para um volume grande de dados

- Processamento quase-tempo-real
    - Executa os processamentos assim que o registro chega ou em intervalos muito curtos de tempo (micro batch)
    - Pouco volume

- Bronze
    - Orientado ao evento
    - Dados no formato que foi ingerido
    - Por evento

- Silver
    - Orietado ao registro
    - Dado limpo e tratado na sua granularidade mais baixa

- Gold
    - Orientado ao negócio
    - Dado consolidado e orientado ao indicadores de negócio

- Consumo
    - Dados disponibilizados em ferramentas de apresentação de dashboards, relatórios, modelos de ML e outros sistemas transacionais

- Metadados
    - Informação complementar sobre os dados

- Catálogo
    - Inventário, descrição e contexto dos dados

- Segurança
    - Gestão de acessos, encriptação de dados sensíveis

- Qualidade
    - Gestão da qualidade dos dados, consistência e precisão

- Governança
    - Politicas, diretrizes, processos, matriz de responsabilidade, documentação

