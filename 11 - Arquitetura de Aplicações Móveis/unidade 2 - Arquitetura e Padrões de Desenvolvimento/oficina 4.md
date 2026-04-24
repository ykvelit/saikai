# Oficina 4: Consumir uma API REST para buscar dados e exibí-los em um aplicativo móvel

## Objetivo

- Para a Oficina 4, vamos desenvolver um aplicativo móvel completo que consuma uma API REST para buscar e exibir dados
- Usaremos exemplos como a busca de informações de CEP ou filmes
- Vamos sugerir o uso de React Native para a criação do app, pois é uma linguagem versátil que permite desenvolver para iOS e Android ao mesmo tempo
- Outras opções podem incluir Swift para iOS ou Kotlin para Android, dependendo das necessidades  do app/projeto

### 1. Configuração do Ambiente

- Instale as ferramentas necessárias
    - Para React Native
        - Configure o ambiente com Node.js, npm, e o CLI do React Native
    - Para Swift (Xcode) ou Kotlin (Android Studio)
        - Instale e configure o ambiente conforme a plataforma de destino

- API para Testes
    - API de CEP
        - Pode-se usar a ViaCEP (https://viacep.com.br/ws/{cep}/json/)
    - API de Filmes
        - Exemplo com OMDb API (https://www.omdbapi.com/?apikey={sua_api_key}&t={nome_do_filme})

### 2. Estrutura do Projeto

- Organize o Projeto com pastas para componentes, telas, e serviços (onde a lógica da API será implementada)
- Dependências  
    - Para React Native, adicione axios para facilitar as requisições HTTP
    - `npm install axios`

### 3. Criação do Layout

- Tela de Entrada
    - Campo de Texto
        - Para que o usuário insira o CEP ou o nome do filme
    - Botão de Busca
        - Um botão que, ao ser pressionado, aciona a requisição à API

- Tela de Exibição dos Dados
    - Exiba os dados retornados da API, como endereço completo (no caso do CEP) ou detalhes do filme (título, ano, descrição, pôster)

### 4. Implementação do Consumo de API

- Criar o Serviço de Requisição
    - Em uma pasta de serviços (/services), crie um arquivo api.js para configurar o consumo da API.
    - Use axios para realizar a requisição

```js
import axios from 'axios';

export const fetchAddress = async (cep) => {
    const response = await axios.get(`https://viacep.com.br/ws/${cep}/json/`);
    return response.data;
}
```

- Função para chamar a API
    - Na tela de busca, chame a função fetchAddress passando o CEP inserido pelo usuário
    - Para filmes, adapte a URL e parâmetros conforme a API OMDb

### 5. Exibição dos Dados no App

- Estados para manipular os dados
    - Utilize useState para gerenciar o valor do CEP ou nome do filme e os dados recebidos da API

```js
const [input, setInput] = useState('');
const [data, setData] = useState(null);
```

- Função para buscar e exibir
    - Crie uma função que seja executada ao pressionar o botão de busca, que chamará a função da API e armazenará os dados no estado

```js
const handleSearch = async () => {
    try{
        const result = await fetchAddress(input);
        setData(result);
    } catch(error){
        console.error(error);
    }
};
```

- Renderizar os dados na tela
    - Na tela de exibição, renderize os dados obtidos da API usando componentes de texto e imagem

```jsx
{data && (
    <View>
        <Text>{data.logradouro}</Text>
        <Text>{data.bairro}</Text>
        <Text>{data.localidade}</Text>
        <Text>{data.uf}</Text>
    </View>
)}
```
        
### 6. Validação e Tratamento de Erros

- Verifique a Entrada do Usuário
    - Antes de realizar a requisição, valide o formato do CEP ou nome do filme

- Tratamento de Erros
    - Adicione um tratamento para exibir uma mensagem de erro caso a API retorne um erro (exemplo: CEP inexistente)

### 7. Testes e Ajustes Finais

- Testes Locais
    - Simule diferentes entradas para verificar se o app responde adequadamente

- Ajuste de Layout
    - Certifique-se de que o layout seja responsivo e intuitivo para o usuário

### 8. Compilação e Distribuição (Opcional)

- Compile o aplicativo para o emulador ou dispositivos físicos para testar a integração completa com a API