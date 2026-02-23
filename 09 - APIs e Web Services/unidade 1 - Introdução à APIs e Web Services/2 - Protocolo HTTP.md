# Protocolo HTTP

- Hypertext Transfer Protocol (HTTP)
- É um protocolo da camada de aplicação para sistemas distribuídos e colaborativos de informação no formato de hipertextos
    - RFC 2068

- Visão geral sobre o protocolo HTTP e sua importância na criação de aplicações Web e APIs

- A comunicação HTTP baseada em requisição/resposta, além do formato das requisições e respostas trocadas entre clientes e servidores na Web

- Os métodos do protocolo HTTP, suas características e suas funcionalidades em uma aplicação Web

- Os cabeçalhos do protocolo HTTP, seus tipos e alguns exemplos, destacando a sua aplicabilidade

- Mudanças nas novas versões do protocolo HTTP

- Características
    - Requer a atuação de dois programas
        - Cliente e Servidor
    - Atua na camada de aplicação da pilha TCP/IP
    - A comunicação utiliza conexões TCP (e UDP no caso do HTTP v3.0)
    - O servidor HTTP, por padrão, utiliza a porta 80 
    - Protocolo que não guarda estado do cliente 
        - Stateless

- Histórico
    - (1991) HTTP/0.9
    - (1994) HTTPS
    - (1996) HTTP/1.0
    - (1999) HTTP/1.1
    - (2009) SPDY 1.0
    - (2015) HTTP/2
    - (2016) QUIC
    - (2018) HTTP/3

## Códigos de retorno

| Código | Propósito        | Descrição                                                     |
| ------ | ---------------- | ------------------------------------------------------------- |
| 1xx    | Informacional    | Requisição recebida, processo em continuidade                 |
| 2xx    | Sucesso          | A ação foi recebida, entendida e aceita                       |
| 3xx    | Redirecionamento | Ações adicionais devem ser executadas para completar o pedido |
| 4xx    | Erro no cliente  | O pedido contém erro de sintaxe ou não pode ser completado    |
| 5xx    | Erro no servidor | O servidor falhou em completar um pedido aparentemente válido |

## Métodos (Verbs)

| Método  | Propósito                                                                                                       | Safe (readonly) | Idempotente |
| ------- | --------------------------------------------------------------------------------------------------------------- | --------------- | ----------- |
| GET     | Requisitar a representação de um recurso específico                                                             | Sim             | Sim         |
| POST    | Enviar dados a serem processados por um recurso. Usado para incluir recursos ou submeter dados de processamento | Não             | Não         |
| HEAD    | Similar ao GET, porém retorno deve ser somente do conjunto de cabeçalhos associados ao recurso solicitado       | Sim             | Sim         |
| PUT     | Requisitar a criação ou atualização de um recurso no servidor a partir dos dados no corpo da requisição         | Não             | Sim         |
| DELETE  | Excluir um recurso do servidor                                                                                  | Não             | Sim         |
| TRACE   | Solicita ao servidor uma cópia (eco) da requisição. Usado para testar se a requisição foi alterada no caminho   | Sim             | Sim         |
| PATCH   | Utilizado para realizar alterações parciais de um recurso                                                       | Não             | Não         |
| OPTIONS | Usado pelo cliente para entender, ou descobrir, os métodos HTTP e outras opções suportadas por um servidor web  | Sim             | Sim         |
| CONNECT | Usado quando o cliente estabelece uma conexão HTTPS com um servidor via um proxy                                | Não             | Não         |

### GET

- Tem por objetivo requisitar a representação de um recurso ao servidor

- Por definição, não deve alterar o estado do servidor (safe)

- As requisições podem ser mantidas em cache (favoritos ou bookmarks)

- Envia dados ao servidor via parâmetros na query string que ficam visíveis na URL

- Tem restrição quanto ao tamanho e ao formato das informações enviadas ao servidor
    - Formato: limitado a caracteres textuais (ASCII) incluídos na query string
    - Tamanho: 
        - Apache: 4.000 caracteres
        - MS IIS: 16.384 caracteres
        - Tomcat: padrão 8.192 podendo chegar até 65.536 caracteres

- Este é o método mais utilizado em aplicações Web.

- Ao informar uma URL em um navegador, o usuário está disparando uma requisição do tipo GET

### POST

- Envia dados ao servidor para serem processados

- Por definição tem objetivo de alteram o estado do servidor (not safe)

- Pode enviar dados via query string ou via corpo da requisição 
    - Os dados enviados pelo corpo não ficam visíveis na URL
    - Muito utilizado para envio de dados sensíveis como senhas de acesso

- Não podem ser ‘favoritados’ (bookmarked)

- Não possuem restrição quanto ao tamanho e ao tipo de dados a serem enviados ao servidor

- Normalmente é utilizado em conjunto com formulários HTML

- Observe os dados enviados no corpo da Requisição

### HEAD

- Possui estrutura e objetivo similar às requisições de GET, porém o servidor deve enviar apenas o conjunto de cabeçalhos associados ao recurso informado

### PUT

- Requisita a criação ou atualização de um recurso no servidor a partir dos dados no corpo da requisição. 

- Utilizado no upload de arquivos para servidores Web

### DELETE

- Solicita ao servidor a exclusão de dados ou representações associados ao recurso informado

### TRACE

- Usado para ecoar o conteúdo de uma requisição HTTP ao servidor

- Usado para verificar se a requisição é alterada no caminho por agentes intermediários (servidores de cache ou proxy)

### OPTIONS

- Usado para descobrir métodos HTTP e outras opções suportados pelo servidor

- O cliente pode especificar uma URL para o método de opções ou um asterisco (*) para se referir a todo o servidor

### CONNECT

- Usado pelo cliente para estabelecer uma conexão com o servidor web que pode ser via protocolo seguro (TLS)

- É utilizado no caso de requisições a proxies

### GET vs POST

|                                | GET                                                                                                                                | POST                                                                                                                        |
| ------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| Botão Voltar / Recarregar      | Inofensivo                                                                                                                         | Os dados serão reenviados (o navegador deve alertar o usuário de que os dados estão prestes a ser reenviados)                  |
| Favoritos (Bookmark)           | Pode ser adicionado aos favoritos                                                                                                  | Não pode ser adicionado aos favoritos                                                                                           |
| Cache                          | Pode ser armazenado em cache                                                                                                       | Não é armazenado em cache                                                                                                       |
| Tipo de codificação            | application/x-www-form-urlencoded                                                                                                  | application/x-www-form-urlencoded ou multipart/form-data. Use multipart para dados binários                                 |
| Histórico                      | Os parâmetros permanecem no histórico do navegador                                                                                 | Os parâmetros não são salvos no histórico do navegador                                                                         |
| Restrição de tamanho dos dados | Sim. Ao enviar dados, o método GET adiciona os dados à URL, e o tamanho da URL é limitado (máx. ~2048 caracteres)                  | Não há restrições                                                                                                               |
| Restrição de tipo de dados     | Apenas caracteres ASCII permitidos                                                                                                 |	Sem restrições. Dados binários também são permitidos                                                                            |
| Segurança                      | GET é menos seguro que POST, pois os dados enviados fazem parte da URL. Nunca use GET para enviar senhas ou informações sensíveis! |	POST é um pouco mais seguro que GET, pois os parâmetros não ficam armazenados no histórico do navegador nem nos logs do servidor |
| Visibilidade                   | Os dados ficam visíveis para todos na URL                                                                                          | Os dados não são exibidos na URL                                                                                               |

## Cabeçalhos (Headers)

- Os cabeçalhos utilizados em requisições e respostas do protocolo HTTP carregam informações adicionais sobre a comunicação entre cliente e servidor

- Tipos de cabeçalhos

    - Request header
        - Informações sobre a requisiçãofeita ou sobre o cliente Web
    
    - Response header
        - Informações sobre a resposta encaminhada ou sobre o servidor Web
    
    - Entity header
        - Informações sobre o conteúdo da entidade trocada como tamanho e tipo
    
    - General header
        - Usado tanto em requisições quanto em respostas

### Cabeçalhos de requisição

| Cabeçalho           | Utilidade                                                                 | Exemplo |
|---------------------|---------------------------------------------------------------------------|---------|
| Accept              | Lista os tipos de mídia aceitáveis para a resposta. Indica que a solicitação está limitada a um conjunto específico de tipos desejados. | `Accept: application/json`<br>`Accept: text/html,application/xhtml+xml, application/xml;q=0.9,*/*;q=0.8` |
| Accept-Charset      | Lista os conjuntos de caracteres aceitáveis para a resposta.              | `Accept-Charset: utf-8, iso-8859-1;q=0.5` |
| Accept-Encoding     | Lista os tipos de codificação de conteúdo aceitáveis para a resposta.     | `Accept-Encoding: gzip, deflate` |
| Accept-Language     | Lista os idiomas naturais aceitáveis e a preferência do usuário para a resposta. | `Accept-Language: pt-BR, en;q=0.9, *;q=0.8` |
| Authorization       | Informa as credenciais de autenticação do User Agent para acessar o recurso. | `Authorization: Basic SGxsdfRp32hgIKVrw5VzW1` |
| Host                | Indica o host e a porta do servidor onde o recurso está sendo solicitado. | `Host: pucminas.br` |
| Referer             | Informa a URL do recurso de origem que direcionou o usuário para a requisição atual. | `Referer: https://acesso.gov.br/login?id=acesso.gov.br` |
| User-Agent          | Informa ao servidor detalhes sobre o cliente (navegador ou agente) que está fazendo a requisição. | `User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.163 Safari/537.36` |

### Cabeçalhos de resposta

| Cabeçalho          | Utilidade                                                                 | Exemplo |
|--------------------|---------------------------------------------------------------------------|---------|
| Server             | Informa detalhes do software que implementa o servidor Web.               | `Server: Apache/2.4.34 OpenSSL/1.0.2k-fips PHP/5.5.38` |
| Set-Cookie         | Apresenta cookies a serem armazenados pelo cliente e enviados ao servidor nas próximas requisições. | `Set-Cookie: MLPRICING=1; Domain=magazineluiza.com.br;` |
| ETag               | Identificador da versão do recurso. É alterado sempre que o recurso muda e é usado no controle de cache. | `ETag: "353-527867f65e8ad"` |
| Location           | Redireciona o cliente Web para outra URI.                                 | `Location: https://www.pucminas.br/Paginas/main.aspx` |
| WWW-Authenticate   | Indica que o servidor requer autenticação do usuário para acessar o recurso e especifica o método. | `WWW-Authenticate: Basic realm="Site X", charset="UTF-8"` |

### Cabeçalhos de entidade

| Cabeçalho        | Utilidade                                                                              | Exemplo |
|------------------|----------------------------------------------------------------------------------------|---------|
| Content-Encoding | Indica uma modificação ao tipo de mídia empregado no conteúdo                          | `Content-Encoding: gzip` |
| Content-Language | Descreve a linguagem na qual o conteúdo foi criado (en, pt, etc)                       | `Content-Language: pt-br` |
| Content-Length   | Indica a quantidade em número de bytes na notação decimal                              | `Content-Length: 17515` |
| Content-Location | Local alternativo para o recurso solicitado                                            | `Content-Location: /index.htm` |
| Content-Type     | Indica o tipo de mídia do conteúdo                                                     | `Content-Type: text/html; charset=utf-8` |
| Expires          | Informa a data e hora em que o recurso recebido expira e deixa de ser válido em cache. | `Expires: Sun, 31 Jul 2016 05:00:00 GMT` |
| Last-Modified    | Informa a data e hora da última modificação do recurso no servidor.                    | `Last-Modified: Tue, 06 Nov 2018 22:45:26 GMT` |

## Versões

- 1991 - O HTTP 0.9 é lançado
- 1994 - O HTTPS foi criado pela Netscape
- 1996 - O HTTP 1.0 foi lançado
    - Conceito de cabeçalhos
    - Códigos de Status
- 1999 - O HTTP 1.1 foi lançado
    - Conexões TCP persistentes 
    - Suporte a Virtual Host (Cabeçalho Host)
    - Autenticação Digest
    - Controle de cache
    - Possibilidade de compressão de dados
- 2009 - Google propõe o SPDY
- 2015 - O HTTP 2.0 é lançado
    - Baseado no SPDY
    - Compressão de dados obrigatória
    - Cabeçalhos binários
    - Requisições paralelas
    - Envio apenas de cabeçalhos alterados nas próximas requisições
    - Priorização de requisições
    - Server PUSH – Envio automático de arquivos adicionais
- 2018 – O HTTP 3 é lançado
    - Protocolo de transporte QUIC baseado em UDP

### HTTP/1.1 vs HTTP/2

| HTTP 1.1 | HTTP 2.0 |
| --- | --- |
| Protocolo textual | Protocolo binário |
| Protocolo sequencial | Requer mais de uma conexão para simular o paralelismo de requisições |
| Protocolo assíncrono | Utiliza multiplexação para realizar requisições paralelas em uma única conexão |
| Não prioriza requisições | Possui priorização de requisições |
| Apenas o cliente pode iniciar uma requisição | Possui o mecanismo de server push (servidor infere requisições futuras e realizar o envio antecipado) |
| Compressão de dados é opcional | Compressão de dados é padrão e obrigatória |
| Envia todos os dados de cabeçalho em cada mensagem |Comprime cabeçalhos para enviar apenas os dados que sofreram alteração ou são desconhecidos |

### Protocolo HTTP/2

- Conexão única e persistente
    - Apenas uma conexão é usada para cada página da web
    - A mesma conexão é usada enquanto a página da Web estiver aberta

- Multiplexação 
    - Requisições e respostas são paralelas e assíncronas, o navegador solicita vários arquivos e os recebe assim que estiverem prontos na mesma conexão

- Compressão de cabeçalhos e codificação binária 
    - Os cabeçalhos são comprimidos usando um novo padrão separado e seguro de compressão, chamado HPACK, que reduz a quantidade de dados que cruzam a rede. As informações de cabeçalho são enviadas em formato compacto e binário, não como texto simples

- Priorização 
    - As solicitações recebem níveis de dependência e solicitações no mesmo nível são priorizadas
    - O servidor utiliza essas informações para ordenar e atribuir recursos para atender às solicitações

- Criptografia SSL 
    - O  HTTP/2 permite adicionar suporte SSL com, em alguns casos, nenhuma penalidade de desempenho, tornando o seu site mais seguro
