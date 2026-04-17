# Tipos de Aplicações Móveis

- Nativo, Web e Híbrido
    - Recursos e diferenças, prós e contras de cada tipo e qual tipo de aplicativo é melhor para diferentes situações

- Qual o tipo de aplicação adequado para diferentes cenários?
    - A escolha entre aplicações nativas, web ou híbridas depende do contexto e das necessidades específicas do projeto
    - Se o desempenho e a experiência do usuário forem prioridades, as aplicações nativas são a melhor escolha
    - No entanto, se a rapidez no lançamento e o custo forem fatores decisivos, as aplicações híbridas oferecem um bom equilíbrio
    - Para aplicações mais simples, onde o foco é o conteúdo e o acesso universal, uma aplicação web pode ser a solução mais prática e econômica

## Aplicativos nativos

- As aplicações nativas são desenvolvidas especificamente para um sistema operacional, como Android (usando Kotlin ou Java) e iOS (usando Swift ou Objective-C)

- Elas são compiladas diretamente para o dispositivo, o que permite o uso total dos recursos nativos, como GPS, câmera, e notificações push

- Vantagens
    - Desempenho otimizado para hardware e sistema operacional
    - Acesso total às APIs e funcionalidades nativas do dispositivo
    - Melhor experiência do usuário, com interfaces otimizadas para a plataforma
    - Maior segurança, pois o código roda diretamente no aparelho

- Desvantagens
    - O custo de desenvolvimento é maior porque necessita de equipes diferentes para cada plataforma
    - É necessária uma manutenção mais complexa porque as atualizações devem ser aplicadas aos sistemas iOS e Android
    - Maior tempo de desenvolvimento
    - Aplicativos que precisam de desempenho rápido, como jogos ou que consomem muita energia do dispositivo, como aplicativos de AR e GPS

- Cenários adequados
    - Aplicações que exigem alto desempenho, como jogos, ou que utilizam recursos intensivos do dispositivo, como aplicativos de realidade aumentada e navegação

## Aplicativos da Web

- Aplicações web são acessadas por meio de navegadores e construídas utilizando tecnologias como HTML, CSS e JavaScript

- Elas rodam em qualquer dispositivo com um navegador moderno e não precisam ser instaladas

- Vantagens
    - Este aplicativo funciona em qualquer dispositivo com navegador da web, independentemente do sistema em execução
    - Simplificado: use o mesmo código para todos os dispositivos para economizar tempo e dinheiro
    - Não é necessária aprovação em lojas de aplicativos (App Store, Google Play)
    - O usuário sempre obtém a versão mais recente do conteúdo ao acessá-lo pelo navegador

- Desvantagens
    - Desempenho limitado, especialmente em comparação com aplicativos nativos
    - O dispositivo restringiu o acesso a determinados recursos (como alertas e armazenamento local de dados)
    - Depende da conexão com a internet para pleno funcionamento
    - Use aplicativos ou serviços simples que não precisam de muito hardware de dispositivo, como sites de notícias, blogs ou sistemas empresariais

- Cenários adequados
    - Aplicações simples, focadas em conteúdo ou serviços que não exigem grande interação com o hardware do dispositivo, como sites de notícias, blogs ou sistemas corporativos

## Aplicações híbridas

Aplicações híbridas combinam elementos de aplicações nativas e web
Elas são desenvolvidas usando tecnologias web (HTML, CSS, JavaScript) e envoltas em um container nativo, permitindo que sejam distribuídas pelas lojas de aplicativos
Frameworks como React Native e Ionic são amplamente utilizados para esse tipo de desenvolvimento

- Vantagens
    - Um desenvolvimento mais simples e barato pode ser feito com uma base de código para diferentes plataformas
    - Use as funções integradas do dispositivo para serviços de câmera e localização
    - O aplicativo apresenta desempenho aprimorado em comparação com uma solução baseada na Web, mas fica aquém dos recursos de um aplicativo nativo

- Desvantagens
    - Simplificado: aplicativos nativos funcionam melhor do que outros, especialmente para aplicações difíceis ou que necessitam de muitos recursos
    - O aplicativo pode não fornecer a experiência de usuário mais tranquila, pois algumas interações podem ser menos contínuas em comparação com aplicativos nativos
    - Dependência de estruturas de terceiros, o que pode dificultar a manutenção a longo prazo
    - Aplicações que precisam iniciar rapidamente em diferentes sistemas e não precisam de alta velocidade, como lojas online, mídias sociais ou ferramentas empresariais

- Cenários adequados
    - Aplicações que precisam ser lançadas rapidamente em várias plataformas e não exigem alto desempenho, como aplicativos de comércio eletrônico, redes sociais, ou sistemas internos de empresas