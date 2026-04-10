# SDLC: Build e Test

- A automação de compilação (build) é crucial para os processos de DevOps, pois permite a compilação do código-fonte em código binário
- Evita erros humanos ao executar as etapas manualmente 
- Automação de build e de teste permitem que os desenvolvedores verifiquem o aplicativo e as dependências de terceiros em busca de vulnerabilidades de segurança
- As principais tecnologias abordadas nestas fases incluem SAST e DAST
- Test-driven security
    - Na abordagem de Test-Driven Security, testes de segurança são aplicados em todo o Pipeline
    - Para cada vulnerabilidade encontrada nas fases, requer-se feedback imediato para a devida remediação

> Testes de software mostram a presença de bugs, mas não a sua ausência
> Edsger W. Dijkstra

## SAST

- Static Application Security Testing

- Ferramentas SAST durante a fase de Build utilizam regras OWASP para avaliar vulnerabilidades no código-fonte

- O scan executa como uma tarefa do Pipeline que deve ser avaliado para não impactar no tempo de análise

- Build Time-Check
    - Integrado ao Pipeline
    - Configuração de regras abrangentes
    - Configuração de avaliação de SCA
    - Testes automatizados baseado em risco
    - Alertar partes interessadas de alertas de risco
    - Validar assinatura digital dos artefatos de software

- No estágio de pré-commit, a ferramenta SAST deve verificar os objetos antes de ocorrer o commit no repositório

- No estágio de commit, a verificação SAST deve verificar todos os objetos relacionados ao código

- No estágio de compilação, a varredura SAST deve fazer parte da compilação

- No estágio de implantação, a ferramenta SAST deve ser iterativa (IAST) e deve garantir que nenhuma vulnerabilidade seja encontrada

- Aspectos chave da escolha da solução de SAST
    - Suporte às linguagens de programação adotadas pela organização
    - Alta acurácia e baixa taxa de falso-positivo
    - Tempo de scan
    - Otimização dos filtros e regras de scan (código de teste, Objeto Mock e Stub, arquivos de imagem, documentos, entre outros)
    - Avaliação de SCA, Contêineres e Infraestrutura como Código (IaC)
    - Interface amigável e fácil gestão
    - Definição de Papéis e Responsabilidades
    - Suporte a integração com as soluções de Pipeline em Cloud (Azure, AWS, GitHub) e On-premises (Jenkins) existentes
    - Suporte para integração de ferramentas de colaboração e ITSM (Jira, ServiceNow, Azure Boards) existentes
    - Suporte a consumo de API para consumo de informações, coleta de métricas e geração de indicadores
    - Integração com Plugin de IDE existentes das estações de trabalho e treinamento
    - Relatórios e Analytics (principalmente, risco dos projetos)

## Acurácia

| Evento | Significado |
|--------|-------------|
| Falso Positivo | Identificado como um problema, quando na verdade não é. Baixa Acurácia. |
| Falso Negativo | Problemas potenciais que não são identificados. Pior caso. |
| Verdadeiro Positivo | O problema identificado é real. Melhor caso.  |
| Verdadeiro Negativo | Geralmente informativo. Comportamento normal e esperado. |

- Muitos falsos positivos perpetuam a fadiga e podem tornar o trabalho de análise de segurança repetitivo e estressante, impactando potencialmente a eficácia das atividades

- Falso negativo pode fazer com que vulnerabilidades críticas na Aplicação não sejam identificadas, sendo causa de eventual exploração

- O OWASP Benchmark usa o Índice de Youden para medir a precisão da ferramenta

- Esta fórmula irá gerar um número entre -1 e 1. O resultado mais próximo de 1 denota nenhum falso positivo, enquanto -1 denota apenas falso positivo

> j = truePositives/(truePosites + falseNegatives) + trueNegatives/(trueNegatives + falsePositives)