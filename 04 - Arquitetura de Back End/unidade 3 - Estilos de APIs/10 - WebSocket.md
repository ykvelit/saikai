# WebSocket

- O WebSocket é um protocolo usado para estabelecer um canal de comunicação de 
streaming bidirecional sobre uma única conexão de Protocolo de Controle de Transporte (TCP)
- Embora o protocolo seja geralmente usado entre um cliente web (por exemplo, um navegador) e um servidor, às vezes é usado também para comunicação servidor-servidor
- Fonte: https://developer.mozilla.org/pt-BR/docs/WebSockets

## Vantagens

- Emula canais bidirecionais de comunicação para facilitar conversações
- Aplicações que demandam atualizações de eventos com frequência fazem uso desse tipo de modelo
    - Exemplos
        - Slack
        - Trelllo
        - Blockchain
- WebSockets podem habilitar a comunicação full-duplex(servidor e cliente podem se comunicar simultaneamente) com baixo custo
- Além disso, eles são projetados para trabalhar sobre a porta 80 ou 443, permitindo-lhes trabalhar bem com firewalls que podem bloquear outras portas
- WebSockets são ótimos para dados rápidos e para transmissão ao vivo se você 
tiver conexões de longa duração
- Tenha cuidado se você planeja disponibilizá-los em dispositivos móveis ou em regiões onde a conectividade pode ser irregular. Isso porque os clientes devem 
manter a conexão viva. Se a conexão morrer, o cliente irá precisar reiniciá-la
