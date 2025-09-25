# Automação de Builds

- Times de baixa maturidade DevOps
    - Passam a maior parte do tempo de um projeto com o software sem funcionar
    - Operam durante muito tempo com códigos isolados
    - Adiam tarefas de integração e testes de aceite para o final do projeto

- O que é a automação de builds ?
    - A automação de builds é prática essencial para garantir que os executáveis dos seus produtos sejam gerados de forma consistente, em base diária

    - Esta prática busca evitar o problema comum do código funcionar apenas  máquina do desenvolvedor

- Como a automação de builds funciona ?
    - A automação de builds externaliza todas as dependências de bibliotecas e configurações feitas dentro de uma IDE para scripts e que possa ser consistentemente executado por robôs
    - Ela é pilar básico para avançarmos em direção a fluxos de CI

- Embora a automação de builds, na sua definição inicial, lide apenas com a construção de um build, a prática comum de mercado é que builds devam executar um conjunto mínimo de testes de unidade automatizados (smoke tests) para estabelecerem confiabilidade mínima ao executável sendo produzido

## Requisitos

1. Acordos entre o time
2. Gestão de configuração
3. Compilação automatizada
4. Checkins diários de código
5. Testes de unidade automatizados
6. Suíte abrangente de testes
7. Processo leve de compilação e testes
