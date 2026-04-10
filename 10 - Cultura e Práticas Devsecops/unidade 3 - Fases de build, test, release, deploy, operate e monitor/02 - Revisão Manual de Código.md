# Revisão Manual de Código

- Processo de leitura do código-fonte linha por linha para identificar possíveis vulnerabilidades 
    - Pode-se adotar a estratégia de revisão em pares

- Requer muita habilidade, experiência e paciência 

- Problemas identificados nesta revisão ajudarão a organização a aumentar sua eficiência e esclarecer o contexto das decisões de codificação

- Foco em vulnerabilidades como problemas de lógica de negócios, autenticação, autorização, criptografia e validação geral de dados. Deve-se inspecionar caminhos de código raramente percorridos

- Pode encontrar código que atua como backdoor ou que realiza ações de fraude

- Pode encontrar vulnerabilidades que SAST, DAST e Pentest eventualmente não encontrariam

- Pontos de atenção que devem ser revisados
    - Processo de validação de dados
    - Tratamento de erros
    - Logging
    - Autenticação, Autorização e Gerenciamento de Sessão
    - Criptografia

- Revisão manual de código deve ser parte da cultura da empresa

- Automatizações podem ser consideradas

- A revisão manual de código deve preceder a aprovação do código-fonte

- Deve ser um requisito por meio de política específica por tema (ou normas internas)

- Deve haver treinamentos sobre o tema de revisão de manual de código

- Geralmente é um requisito para PCI-DSS, HIPAA, outros
