# Oficina 2: Testar e comparar a performance de uma aplicação nativa, uma híbrida e uma PWA

## Objetivo

- Para a Oficina 2, onde o objetivo é testar e comparar a performance de uma aplicação nativa, uma híbrida e uma PWA, siga os passos a seguir para conduzir a avaliação e obter insights práticos
- Essa atividade ajudará a entender melhor as diferenças de desempenho entre as abordagens, bem como suas vantagens e limitações em termos de experiência do usuário

### 1. Comparação

- Avaliar a performance em termos de velocidade de carregamento, resposta e execução de tarefas
- Comparar o consumo de recursos (memória e bateria)
- Observar a experiência do usuário, especialmente em relação à navegação, fluidez de animações, e recursos específicos da plataforma

### 2. Configuração das Aplicações

Prepare uma versão básica de cada tipo de aplicação, todas com funcionalidades semelhantes, para que a comparação seja justa:

- Aplicativo Nativo
    - Desenvolvido em Swift (iOS) ou Kotlin (Android)

- Aplicativo Híbrido
    - Pode ser feito usando React Native ou Flutter

- PWA (Progressive Web App)
    - Desenvolvido com tecnologias web (HTML, CSS, JavaScript), rodando no navegador e com suporte para uso offline

Recomendo que cada versão inclua:
- Uma tela de listagem de dados com rolagem
- Uma funcionalidade de busca
- Uma ação que faça chamadas à API (ex.: consulta de dados online)

### 3. Ferramentas de Teste

Escolha ferramentas que permitam monitorar a performance de cada aplicação:

- Aplicativos Nativos (iOS e Android)
    - iOS
    - Utilize o Xcode Instruments para análise de CPU, memória, gráficos e consumo de bateria

- Android
    - Utilize o Android Profiler do Android Studio para monitoramento de CPU, memória, rede e consumo de energia

- Aplicativo Híbrido (React Native ou Flutter)
    - Utilize as mesmas ferramentas para aplicativos nativos, mas com configurações específicas para o tipo de aplicativo (React Native: Android Studio/Xcode; Flutter: DevTools do Flutter)

- PWA
    - Utilize as DevTools do Chrome (aba Lighthouse e Performance) para monitorar carregamento, tempo de resposta e uso de recursos

### 4. Métricas de Comparação

As principais métricas para comparar a performance dos três tipos de aplicação incluem:

- Tempo de Carregamento Inicial
    - Tempo necessário para que a aplicação esteja pronta para uso após aberta

- Consumo de CPU e Memória
    - Quantidade de CPU e memória consumidas durante o uso

- Consumo de Bateria    
    - Verifique o impacto da execução contínua sobre a bateria

- Tempo de Resposta
    - Tempo necessário para responder às interações do usuário, especialmente em tarefas que envolvem animações ou carregamento de dados

- Desempenho Offline
    - Teste como cada aplicação lida com a ausência de conexão à internet

### 5. Passo a Passo para Testar a Performance

1. Preparação
    - Certifique-se de que todos os dispositivos estejam carregados e conectados a uma rede Wi-Fi confiável
    - Desative notificações e qualquer outro app que possa interferir nos resultados

2. Execução dos Testes
    - Carregamento Inicial
        - Abra cada aplicativo e registre o tempo necessário até que a tela principal esteja pronta para uso
    
    - Interações e Navegação
        - Teste o tempo de resposta de ações como rolagem, transição entre telas e carregamento de novos dados
    
    - Consumo de Recursos
        - Utilize as ferramentas de monitoramento para observar o uso de CPU e memória durante o uso
    
    - Teste Offline
        - Desconecte a rede e verifique como cada aplicativo se comporta (as PWAs são projetadas para funcionar offline em algumas funções, enquanto híbridos e nativos dependem da implementação)
    
    - Repetição dos Testes
        - Execute cada teste múltiplas vezes e anote os resultados para obter uma média e reduzir a influência de variáveis externas

### 6. Registro e Comparação dos Resultados

Utilize uma tabela para organizar os resultados, comparando o desempenho das três versões.
Aqui está um exemplo de como estruturar essa tabela:
| Métrica | Aplicativo Nativo | Aplicativo Híbrido (React Native/Flutter) | PWA |
|---------|-------------------|-------------------------------------------|----|
| Tempo de Carregamento | | | |
| Consumo de CPU | | | |
| Consumo de Memória | | | |
| Consumo de Bateria | | | |
| Tempo de Resposta | | | |
| Desempenho Offline | | | |

### 7. Análise dos Resultados

Baseando-se na tabela de métricas, elabore uma análise detalhada dos resultados:

- Aplicativo Nativo
    - Normalmente, tende a oferecer melhor performance em velocidade e uso de recursos, aproveitando a otimização da plataforma
- Aplicativo Híbrido
    - Em geral, apresenta uma performance boa, mas pode ter leves quedas em comparação ao nativo, especialmente em animações e resposta imediata
- PWA
    - Pode ter desempenho inferior, principalmente no tempo de carregamento e uso de recursos intensivos, mas compensa com a facilidade de acesso e suporte para uso offline

### 8. Conclusão e Discussão
Para encerrar, faça uma conclusão destacando os pontos fortes e fracos de cada abordagem, especialmente em relação aos objetivos do aplicativo e à experiência do usuário. Considere discutir os cenários em que cada tipo de aplicação seria mais adequado, com base nas necessidades de performance e experiência