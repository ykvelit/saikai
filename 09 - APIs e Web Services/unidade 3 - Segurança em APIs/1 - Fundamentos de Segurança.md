# Fundamentos de Segurança

- Autenticação 
    - Verifica se o usuário é quem diz ser

- Autorização 
    - Verifica as permissões de acesso do usuário

- Message digest
    - Função Hash
        - Algoritmo que produz uma sequência diferentes para cada entrada e de tamanho fixo não reversíveis
            - Não restauram a mensagem original
        - Algoritmos
            - Message Digest Algorithm
                - MD5
                - Resumo de mensagem de 128 bits
                - Documentação RFC-1321
            - SHA-1
                - Resumo de mensagem de 160 bits
                - Padrão no EUA

- Codificação Base64
    - Método utilizado para converter dados binários em texto e vice-versa
    - Base64 é muito utilizado na internet pois vários protocolos de aplicação aceitam apenas dados em texto (email, http)
    - É usado em conjunto com o padrão MIME
    - Senhas são codificadas via Base64 para garantir que os caracteres a serem enviados na comunicação são strings ASCII válidas
    - Embora seja uma codificação, Base64 não é uma forma de criptografia e deve ser considerado como dados sendo passados de forma aberta

## PKI

- Internet X.509 Public Key Infrastructure
- ICP 
    - Infraestrutura de Chaves Públicas
    - Estrutura que abrange um conjunto de entidades AC Raiz, ACs, ARs, certificados para prover requisitos de segurança em comunicação de sistemas
- AC Raiz
    - Autoridade Certificadora Raiz
    - Estabelece a cadeia hierárquica de certificados
    - Estabelece a política de certificados, controla certificados das ACs e mantém a lista de certificados revogados

- AC
    - Autoridade Certificadora
    - Responsável por emitir, distribuir, renovar e gerenciar certificados digitais
- Certificado Digital
    - Arquivo eletrônico contendo a identidade digital de uma entidade reconhecida pela ICP
    - Contém
        - Nome da entidade
        - Período de validade
        - Chave pública
        - Nome 
        - Assinatura da entidade que assinou o certificado, número de série
        