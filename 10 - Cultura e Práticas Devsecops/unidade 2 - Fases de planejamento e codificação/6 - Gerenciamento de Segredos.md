# Gerenciamento de Segredos

- Informações sigilosas incorporadas ao código-fonte (ou hard-coded secrets) são fontes comuns de violação de dados

- Informações como secrets, chaves de criptografia, tokens de API, Chaves de SSH, Senhas, tokens Oauth, entre outros, sejam devidamente protegidos e não façam parte do código-fonte

- Segredos não devem ser transmitidos de um estágio para outro no pipeline de CI/CD, onde não são necessários
- Apenas a pessoa ou máquina autorizada tenha acesso ao recurso de Vault
- Usar controle de acesso adequado e garantir que apenas o privilégio necessário seja atribuído a um usuário ou máquina
- Garantir mecanismos de backup da solução de Vault

- Papéis e responsabilidades
    - Desenvolvimento
        - Adotar bibliotecas para as linguagens de desenvolvimento para integração com o Vault
        - Definir o controle de acesso ao Vault
        - Reportar incidentes envolvendo hard-coded
        - Identificar falsos-positivos (código de Teste)

    - Segurança
        - Desenvolver políticas para garantir que informações sigilosas não residem em código-fonte
        - Propor melhores práticas do uso de Vault
        - Adotar análise estática de código para auditar ocorrências de hard-coded e realizar análise de causa raiz
        - Realizar a revisão de acesso ao Vault
        - Realizar conscientização e treinamento

    - Operações
        - Realizar a implantação de Vault
        - Garantir que somente recursos de Cloud autorizados possuam acesso ao Vault
        - Garantir que nenhum recurso de Cloud e Banco de Dados sejam acessados diretamente, somente com o token autorizado
        - Provisionamentos automatizados
        - Garantir meios de recuperação do Vault
        - Reportar incidentes relacionados ao Vault
        - Acesso à Produção Exclusivamente  por GMUD 
        - Adotar Jump Server
        - Adotar Cofre de Senhas (sessão monitorada e gravada)
        - Modificações em Produção Exclusivamente Automatizada
        - Infraestrutura Imutável
    