# Micro Serviços

- O conceito de micros serviços em aplicações Node veio para facilitar a operação e escala de softwares de grande porte
- Implementações de micros serviços adicionam muita complexidade ao sistema como um todo
    - Desenvolvimento de cada micro serviço precisa de ser pensado no auto-funcionamento (mínimo de dependência possível com outros micro serviços)
    - Troca de informações entre micro-serviços
    - Manutenção de estado compartilhado e troca de mensagens

## Benefícios

### Escala técnica

- Possibilidade de escalar fisicamente (recursos de máquina) serviços que demandam mais processamento e fluxo de dados
- Maior resiliência
    - Se uma parte do sistema para de funcionar, existe uma menor chance das demais áreas serem afetadas
- Independência de stacks
    - Embora estejamos falando da stack Node/Js, uma arquitetura de micro serviços permite o sistema a ter uma liberdade de escolha entre tecnologias

### Escala organizacional

- Possibilidade de segregar o desenvolvimento de serviços por times
- Cada time pode ficar responsável pela manutenção de um serviço/domínio específico
- Os deploys podem ser separados por times, sem criar uma dependência entre as fases dos deploys

## TCP sv Mensageria

### TCP

 - Serviços instanciados na mesma rede, onde a comunicação se dá através de um protocolo externo

- A implementação via TCP é simples e direta entre os micro serviços
    - Se um micro serviço precisa de enviar/solicitar alguma informação para um outro, podemos disparar uma requisição que trafega sob o TCP e chega diretamente do outro lado
    - Possui eventualmente problemas de escalabilidade uma vez que se um micro serviço recebe um tráfego alto de requisições, estas podem criar um gargalo na aplicação, congestionando o sistema com o processamento de dados em larga escala

### Mensageria

- Serviços comunicam entre si através de plataformas terceirizadas de mensageria
    - Kafka 
    - RabbitMq
    
- A implementação via Sistemas de Mensageria é robusta e mais complexa quando comparada ao modelo TCP
    - Isso porque um sistema de mensageria exige um segundo sistema que será responsável por receber e enviar mensagens

- Os sistemas de mensageria possuem os seguintes conceitos
    - Publish
        - Ato de publicar uma mensagem no sistema de mensageria
    - Subscriber
        - Micro serviço que assina mensagens em um determinado tópico
    - Producer
        - Parte da nossa implementação que produz mensagens a serem enviadas à plataforma
    - Consumer
        - Parte da nossa implementação que consome mensagens produzidas pelos producers e encaminhadas pelo sistema de mensageria

#### Requisição-Resposta

- O padrão requisição-resposta é utilizado para troca de mensagens entre micro serviços quando uma requisição feita precisa de uma resposta do serviço de destino
    - Uso de dois canais
        - Um para transferência de dados e outro para esperar respostas
    - Algumas situações não necessariamente irão exigir uma resposta do serviço de destino, como
    - Envio de notificações
    - Disparo de emails

#### Event-based

- O padrão event-based é útil quando queremos publicar eventos sem 
necessariamente precisar esperar por uma resposta

- Se quisermos notificar o ecossistema que uma determinada condição aconteceu em um dos micro serviços, esse modelo é ideal porque podemos escutar por eventos em múltiplas áreas de micro serviços diferentes, sem necessariamente a simulação de um protocolo requisição-resposta (como HTTP)

- Esse tipo de sistema baseado em eventos é escalável e seu uso pode ser combinado com sistemas de mensageria, como RabbitMQ, Kafka ou Redis
