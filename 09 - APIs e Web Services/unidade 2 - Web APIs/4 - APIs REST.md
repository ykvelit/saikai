# APIs REST

- REST é um estilo arquitetural para construção de serviços Web que significa a Transferência de Estado Representacional (Representational State Transfer)

- O termo RESTful caracteriza serviços Web que seguem integralmente as recomendações REST, diferentemente daqueles (RESTlike) que implementam parcialmente suas  recomendações

## Requisitos 

- Cliente e servidor
    - Cliente e servidor são independentes e não se preocupam com os detalhes de implementação do outro

- Stateless
    - O servidor não mantém estado sobre a sessão do usuário/aplicação etoda requisição deve conter todas as informações requeridas 
- Cache
    - As respostas podem ser armazenadas em cache (cliente ou proxies reversos) 
    - As respostas devem definir se permitem ou não o cache
- Interface uniforme
    - A interface entre cliente e servidor deve identificar adequadamente os recursos por meio de uma URI e representações padronizadas 
- Sistema em camadas
    - Os componentes não têm visibilidade além da camada seguinte, podendo interagir com interlocutores intermediários de forma natural

## Princípios de design

### Definições do protocolo HTTP
- Utilizar os métodos HTTP de maneira clara em função do seu propósito semântico
    - GET Recuperar um recurso (SELECT)
    - POST Criar um recurso no servidor (INSERT)
    - PUT | PATCH  Alterar um estado de um recurso ou atualizá-lo (UPDATE)
    - DELETE  Remover um recurso (DELETE)
    - OPTIONS Lista as operações de um recurso
- Métodos GET e parâmetros de query não devem alterar estado de recursos

### Estrutura uniforme de Endpoint
- Uma URI intuitiva direta, auto-documentada, e compreensível
- Ter uma estrutura hierárquica semelhares a diretórios
- Ocultar a extensão da tecnologia empregada (asp, jsp, php, etc)
- Manter tudo em caixa baixa (minúsculo)
- Evitar espaços nos caminhos da URI
- Evite parâmetros de QueryString, o máximo possível

### Abordagem stateless (sem estado)
- Servidor não mantem estado sobre sessão do usuário/aplicação
- Toda requisição deve conter todas as informações requeridas (como parte da URI, na query string, no corpo ou no cabeçalho)
- Simplifica o servidor
- Maior escalabilidade uma vez que o servidor não mantém informações sobre sessão
- Servidores de balanceamento de carga não precisam se preocupar com dados de sessão
- Maior confiabilidade (recuperação de falhas)

### Controle do versionamento da API
- Incorporar a versão do serviço na URI
- Incluir informações da versão na representação de estado do recurso

### Controle adequado do cache

#### Cabeçalhos HTTP
- Date 
    - Data e hora de geração da representação
- Last Modified
    - Data e hora de última alteração da representação
- Cache-Control
    - O cabeçalho utilizado pelo HTTP 11 para controle de cache
- Expires
    - Data e hora de expiração da representação Para compatibilizar com clientes HTTP 10
- Age
    - Tempo passado em segundos desde que a representação foi extraído do servidor 
    - Pode ser inserido por um cache intermediário
- ETag
    - Indicador de versão específica de uma representação Se houver alteração, a terá um novo valor
    
#### Valores para o cabeçalho Cache-Control
- Public 
    - Valor padrão 
    - Indica que a representação pode ser armazenada em qualquer cache 
- Private
    - Indica que a representação é para um único cliente e caches intermediários não podem armazenar a representação, apenas um cache privativo
- no-cache/no-store
    - Armazenamento da representação em cache desabilitado
- max-age
    - Tempo máximo de validade da representação (em segundos), tomando como base a data informada no cabeçaho "Date"
- s-maxage
    - Similar a max-age, porém válido apenas para caches intermerdiários
- must-revalidate
    - Indica que a representação deve ser revalidada pelo servidor evitando o uso de recursos expirados
- proxy-validate
    - Similar ao must-revalidate porém se aplica apenas aos caches intermediários

### Documentação clara e adequada da API
- OpenAPI Specification
    - Padrão para definição de APIs RESTful
    - Independente de linguagem de programação
    - Permite a geração automática de código