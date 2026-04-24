# Oficina 3: Aplicar um padrão arquitetural (MVC ou MVVM) em um protótipo simples de aplicação

## Objetivo

- Para a Oficina 3, vamos desenvolver um protótipo de um app usando o padrão arquitetural MVC ou MVVM em uma ferramenta de design, como Figma ou Adobe XD

- Este protótipo será simples, mas deve refletir a estrutura e a interação do padrão arquitetural escolhido

### 1. Escolha do Padrão Arquitetural

- MVC (Model-View-Controller)
    - Separação entre a interface do usuário (View), a lógica de controle (Controller) e os dados (Model)

- MVVM (Model-View-ViewModel)
    - Similar ao MVC, mas o "ViewModel" serve como intermediário para vincular dados do Model à View

### 2. Estrutura do Protótipo

- Objetivo
    - Crie um app que permita ao usuário realizar uma ação simples, como adicionar uma tarefa a uma lista ou consultar informações de um produto

- Fluxo de Navegação
    - Decida as telas e como elas serão conectadas
    - Exemplo
        - Tela inicial, tela de detalhes e tela de confirmação

### 3. Definição das Telas

- Tela Inicial (Lista de Itens)
    - Exibe uma lista de itens ou dados. Por exemplo, uma lista de tarefas ou produtos

- Tela de Detalhes
    - Exibe informações detalhadas sobre um item selecionado na lista

- Tela de Confirmação
    - Confirma a adição ou edição de um item na lista

### 4. Estruturação das Telas no Figma ou Adobe XD

- Defina a Resolução das Telas
    - Escolha o tamanho da tela para mobile, como iPhone ou Android padrão.
- Componentes de Interface
    - Headers e Footers
        - Use um header para o título e navegação básica
    - Botões e Ações
        - Adicione botões para interagir com a lista, como "Adicionar", "Editar", "Excluir"
- Campos de Texto e Listas
    - Para exibir e editar informações

- Interações
    - Adicione links entre as telas para simular o fluxo de navegação
    - Configure o protótipo para que o usuário possa clicar e ser direcionado de uma tela para outra

### 5. Implementação do Padrão Arquitetural no Protótipo

- MVC
    - Model
        - Defina quais dados serão exibidos. Exemplo: uma lista de tarefas com título e descrição
    - View
        - Estruture os elementos visuais da interface, como listas, botões e campos de texto
    - Controller
        - Simule as interações. Configure a troca entre telas para representar a lógica de controle
- MVVM
    - Model
        - Estruture os dados a serem manipulados
    - ViewModel
        - Simule a conexão entre o Model e a View. Em Figma ou XD, isso pode ser feito configurando ações interativas para demonstrar o fluxo de dados
    - View
        - A interface onde os dados e interações são exibidos

### 6. Teste e Avalie a Usabilidade

- Teste de Interatividade
    - Garanta que o fluxo entre as telas funcione sem problemas
- Ajuste de Intuitividade
    - Revise os rótulos e a organização dos elementos para tornar o uso intuitivo

### 7. Exportação e Compartilhamento

Após finalizar o protótipo, exporte-o em PDF ou como link interativo, se a ferramenta permitir, para que outros possam visualizar e testar. Este processo cria um protótipo que simula a interação com o app e mostra como o padrão arquitetural organiza a aplicação
