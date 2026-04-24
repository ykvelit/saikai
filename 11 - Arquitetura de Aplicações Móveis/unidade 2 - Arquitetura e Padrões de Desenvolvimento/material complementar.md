# Material Complementar

## Notas de aula

### Arquitetura e Padrões de Desenvolvimento

- Padrões Arquiteturais para Aplicações Móveis
    - MVC (Model-View-Controller), MVVM (Model-View-ViewModel), MVP (Model-View-Presenter), entre outros
        - Esses padrões separam a aplicação em componentes distintos, facilitando a manutenção e escalabilidade
        - Cada padrão possui características próprias
            - MVC
                - Organiza a aplicação em Model, View e Controller
                - É comumente usado em projetos pequenos a intermediários
            - MVVM
                - Recomendado para interfaces reativas, separa a lógica da interface em Model, View e ViewModel, ideal para projetos que exigem alta atualização de dados
            - MVP
                - Utilizado para maior controle sobre a lógica da interface e favorece a testabilidade
                - Comum em desenvolvimento Android
    - Aplicação dos Padrões em Contextos Móveis 
        - O uso de cada padrão depende do contexto
        - MVC é adequado para projetos simples, MVVM para interfaces dinâmicas e MVP para ambientes que requerem alta testabilidade
    - Melhores Práticas e Casos de Uso
        - Exemplos práticos e dicas para aplicar cada padrão de forma eficiente, com foco em escalabilidade e redução de acoplamento

### Web Workers e Progressive Web Apps (PWA)

- Conceito de Web Workers e sua Aplicação em Desenvolvimento Móvel
    - Web Workers permitem processamento paralelo em JavaScript, mantendo a interface responsiva durante operações intensas

- Introdução ao Conceito de Progressive Web Apps (PWAs)
    - PWAs são aplicações web que se comportam como apps nativos, podendo ser instaladas no dispositivo e funcionar offline

- Benefícios e Desafios na Implementação de PWAs
    - PWAs têm vantagens como acessibilidade multiplataforma e custo reduzido, mas enfrentam limitações em performance e acesso a funcionalidades específicas do dispositivo

## Reflexão

- Arquitetura e Padrões de Desenvolvimento
    - Qual padrão arquitetural você usaria em um aplicativo móvel ?
    - Que fatores influenciam essa escolha ?

- Progressive Web Apps
    - Como PWAs poderiam beneficiar seu projeto ? 
    - Que limitações você deve considerar ?

## Outros materiais

- Explore implementações em diferentes padrões arquiteturais para compreender melhor o funcionamento de MVC, MVVM e MVP
- Conheça as ferramentas mais usadas para desenvolvimento e teste de apps, como Xcode, Android Studio, e React Native

## Leitura complementar

- Leitura sobre os avanços em Progressive Web Apps e os benefícios dos Web Workers no processamento paralelo
- Consulte a documentação oficial do Android, iOS e PWA para mais detalhes técnicos sobre desenvolvimento em cada plataforma