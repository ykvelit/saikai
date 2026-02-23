# APIs SOAP

- Simple Object Access Protocol

- Protocolo de troca de dados baseado em XML para envio e recebimento de mensagens na Internet

- Independente de plataforma ou linguagem de programação

- Arquitetura
    - SOAP – Protocolo de troca de dados baseado em XML
    - XML – Linguagem de marcação para descrição dos dados
    - WSDL – Descritor de serviços baseado em XML
    - UDDI – Registro e descoberta de serviços

## Estrutura da Mensagem SOAP

- Envelope
    - Define o início e o final da mensagem
    - É obrigatório

- Header
    - Traz atributos opcionais da mensagem utilizada para o seu processamento
    - É opcional

- Body
    - Possui o conteúdo da mensagem em formato XML
    - É obrigatório

## WSLD

- Web Services Description Language

- Linguagem de descrição de um web service baseada em XML

- Define os seguintes objetos:
    - Tipos de dados suportados pelo serviço
    - Padrão de mensagens de entrada e saída
    - Protocolos de comunicação permitidos pelo Web Service (binding) 
    - Serviços e portas de comunicação onde operações são disponibilizadas pelo Web Service
    - Definições sobre schemas e namespaces utilizados no contexto do Web Service

## UDDI

- Universal Description and Discovery Interface

- Serviço de diretório que mantem referência para os Web Services registrados

- Funcionam como páginas amarelas para localização dos Web Services

- Reúne informações como:
    - Nomes endereços e números de telefones dos fornecedores de serviços
    - Serviços oferecidos por cada fornecedor, bem como informações técnicas sobre a interface de cada um
