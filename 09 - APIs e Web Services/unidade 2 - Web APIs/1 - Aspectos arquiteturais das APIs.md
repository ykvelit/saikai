# Aspectos arquiteturais das APIs

## Abordagens de Comunicação em APIs

### Request/Response

- Cliente faz uma requisição ao servidor
- Servidor retorna uma resposta para o cliente

- Exemplos
    - SOAP
    - REST
    - GraphQL
    - gRPC

### Event Driven

- Um gerador de evento envia um evento para um distribuidor de evento
- O distribuidor de evento passa o evento para os consumidores
- As conexões são de vida longa

- Exemplos
    - WebSocket
    - WebHook

## Estilos Arquiteturais

### SOAP

- Simple Object Access Protocol

- O SOAP é uma proposta robusta para a construção de APIs, que mescla complexidade e potência

- Utiliza XML para definir comunicações estruturadas e se baseia em um par de cliente e servidor SOAP

- Casos de uso
    - Integração de sistemas empresariais, como sistemas de gerenciamento de pedidos e contabilidade
    - Serviços de pagamento online

### REST

- Representational State Transfer

- REST é um estilo arquitetural que aproveita principalmente os métodos HTTP

- Permite uma interação fácil com recursos, tornando-se um padrão de referência para uma infinidade de aplicações e APIs modernas

- Casos de uso 
    - APIs de mídia social, onde os clientes acessam dados de usuário e publicações
    - APIs de serviços da Web

### GraphQL

- Graph Query Language

- GraphQL oferece flexibilidade e precisão

- Permite que os clientes solicitem exatamente o que precisam, reduzindo a redundância e melhorando o desempenho

- Alguns percebem o GraphQL como um substituto do REST, porém os padrões podem coexistir se complementando

- Casos de uso
    - Aplicações com diferentes clientes requerendo de diferentes conjuntos de dados, como aplicativos de análise de dados

### gRPC

- Google Remote Procedure Call

- gRPC utiliza o protocolo HTTP/2 com transmissão de dados binários

- Prioriza desempenho e velocidade, especialmente para arquiteturas de microsserviços

- Casos de uso
    - Arquiteturas de microsserviços onde a eficiência de comunicação é crucial, como em sistemas de transporte público em tempo real

### WebSocket

- Oferece uma alternativa de comunicação em tempo real e bidirecional

- São ideais para aplicativos de chat, transmissão ao vivo e troca de dados em tempo real, evitando o polling (short polling ou long poling)

- Casos de uso 
    - Aplicativos de chat em tempo real
    - Plataformas de jogos online com funcionalidade multiplayer
    - Placar de jogos

### WebHook

- Voltados para as arquiteturas orientadas a eventos, fornecem uma alternativa para que servidores notifiquem clientes quando eventos específicos ocorrem

- Casos de uso 
    - Notificações de transações financeiras
    - Atualizações em tempo real em aplicativos de colaboração

## Comparativo entre estilos arquiteturais

### Geral

| Abordagem | Vantagens | Desvantagens |
|-----------|-----------|--------------|
| REST | •Fácil interação com recursos •Padrão amplamente adotado | •Pode levar a múltiplas requisições para ações complexas •Falta de flexibilidade em algumas situações |
| SOAP | •Comunicação estruturada e rica em recursos •Integração com sistemas corporativos | •Complexidade de implementação •Overhead devido ao uso de XML •Requer cliente e servidor SOAP |
| GraphQL | •Flexibilidade para clientes obterem o que precisam •Melhor eficiência de rede | •Requer mecanismo de consulta mais complexo no servidor •Gera consultas complexas e ineficientes se mal projetado
| gRPC | •Performance pela comunicação binária e multiplexação •Geração automática de código | •Requer suporte a HTTP/2 •Pode ser mais difícil de depurar devido à natureza binária •Maior curva de aprendizado em comparação com APIs REST |
| WebSockets | •Atualizações em tempo real para clientes •Redução da latência em comparação com polling | •Requer suporte em ambos os lados (cliente e servidor) •Maior complexidade em comparação com APIs tradicionais |
| Webhooks | •Resposta em tempo real a eventos específicos •Redução de overhead de consulta constante | •Pode exigir lógica adicional para confirmações e repetições •Falha de entrega pode ocorrer se não implementado corretamente |

### SOAP x REST

| Aspecto | SOAP | REST |
|---------|------|------|
| Estrutura | Protocolo baseado em XML | Protocolo baseado no estilo arquitetural |
| Comunicação de Dados | Utiliza um padrão de mensagens baseado em XML |Utiliza XML ou JSON para envio e recebimento dos dados |
| Comunicação | Invoca serviços por meio de HTTP e RPC (remote procedure call) | Baseado 100% em HTTP e nas URIs |
| Formato da Mensagem | Resultado codificado no padrão SOAP | Resultado facilmente interpretado por um humano |
| Compatibilidade com Javascript | Complexa | Simplificada |
| Desempenho | Médio | Alto |

### GraphQL x REST

| GraphQL | REST |
|---------|------|
| Linguagem de consulta oferece eficiência e flexibilidade para resolver problemas comuns ao integrar APIs | Um estilo arquitetural amplamente visto como padrão para o desenho de APIs |
| Disponível via um único endpoint HTTP que provê todas as funcionalidades do serviço | Disponível via um conjunto de URLs, cada uma expondo um único recurso | 
| Utiliza uma arquitetura baseada no cliente | Utiliza uma arquitetura baseada no servidor |
| Dificulta o uso do mecanismo de cache | Utiliza cache de maneira simplificada e automática |
| Não trabalha com versionamento de API | Suporta múltiplas versões da API |
| Trabalha apenas com JSON | Suporta múltipos formatos de dados ( JSON, XML, etc) |
| Oferece uma única forma de documentação: GraphiQL | Oferece uma faixa de opções para documentação automatizada (OpenAPI e API Blueprint) |
| Dificulta o uso de códigos de status do protocolo HTTP para 
identificação de erros | Utiliza os códigos de status do protocolo HTTP para identificar facilmente os erros |

## Representação de Dados em APIs

- A representação de Dados é a maneira como os dados trocados entre aplicações são organizados e/ou descritos

- Alguns formatos utilizados em APIs
    - XML
    - JSON
    - YAML
    - CSV
    - ProtoBuf
    - BSON
    - MessagePack

### MIME 

- Multipurpose Internet Mail Extensions

- Padrão utilizado para indicar o formato do conteúdo em uma mensagem de e-mail e muito utilizado em outras aplicações da Internet

- Tipos possíveis definidos pela Internet Assigned Numbers Authority (IANA) 
- Um tipo é dividido em duas partes tipo/subtipo e pode ter parâmetros opcionais (charset, boundary)
- Os valores expressos no cabeçalho Content-Type seguem o padrão denominado MIME

- Exemplos
    - Image/jpg: transmissão de imagens (jpe, jpg, jpeg, ...)
    - text/html: transmissão de textos em HTML
    - x-application/java: transmissão de classes java (.class)
    - application/json;charset=UTF-8: dados em formato JSON com codificação UTF-8

## Padrões de Documentação de APIs

- SOAP
    - WSDL
        - Web Services Description Language
- REST
    - OpenAPI Initiative
    - Swagger
    - API Blueprint
    - RAML
        - RESTful API Modeling Language
    - WADL 
        - Web Application Description Language
