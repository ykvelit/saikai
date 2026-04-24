# Desafio 1: uma pequena aplicação que utilize um padrão arquitetural definido

## Objetivo

- Para o Desafio 1, vamos desenvolver uma pequena aplicação móvel que utilize um padrão arquitetural definido para organizar o código
- Podemos optar pelo MVC (Model-View-Controller), que é um padrão simples e adequado para apps pequenos, garantindo uma separação clara das responsabilidades
- Neste exemplo, criaremos uma aplicação que consome uma API REST para buscar dados e exibi-los, como informações de CEP ou filmes, utilizando React Native com o padrão arquitetural MVC
- Esse padrão nos ajuda a dividir a aplicação em três camadas principais: Model, View e Controller

## Estrutura do projeto

- `src/`
    - `controller/`
        - Contém a lógica de controle e manipulação de dados
    - `models/`
        - Define a estrutura e métodos para interagir com dados (API ou local)
    - `views/`
        - Contém as telas (interface) do aplicativo

### Model: Estrutura e acesso aos dados

- O Model é responsável por gerenciar os dados e comunicar-se com a API para buscar as informações

```js
import axios from 'axios';

class DataModel {
    static async fetchCEP(cep){
        try {
            const response = await axios.get(`https://viacep.com.br/ws/${cep}/json`);
            return response.data;
        } catch (error) {
            throw new Error('Erro ao buscar CEP');
        }
    }

    static async fetchMovie(title){
        try {
            const response = await axios.get(`https://www.omdbapi.com?apikey=${YOUR_API_KEY}&t=${title}`);
            return response.data;
        } catch (error) {
            throw new Error('Erro ao buscar filme');
        }
    }
}

export default DataModel;
```

### View: Interface do usuário

- A View define o layout da aplicação e exibe os dados
- Ela também captura as interações do usuário (como clicar em botões) e comunica esses eventos ao Controller

```js
import React, {useState} from 'react';
import {View, Text, TextInput, Button, StyleSheet} from 'react-native';

const MainView = ({onSearch, data, error}) => {
    const [input, setInput] = useState('');

    return (
        <View style={styles.container}>
            <Text style={styles.title}>Busca de CEP</Text>
            <TextInput
                style={styles.input}
                placeholder="Digite o CEP"
                value={input}
                onChangeText={setInput}
            />
            <Button 
                title="Buscar"
                onPress={() => onSearch(input)}
            />

            {error && <Text style={styles.error}>{error}</Text>}

            {data && (
                <View style={styles.resultContainer}>
                    <Text>Logradouro: {data.logradouro}</Text>
                    <Text>Bairro: {data.bairro}</Text>
                    <Text>Cidade: {data.localidade}</Text>
                    <Text>Estado: {data.uf}</Text>
                </View>
            )}
        </View>
    )
};

const styles = StyleSheet.create({
    container: {padding: 20},
    title: {fontSize: 20, marginBottom: 10},
    input:{boderColor:'gray', borderWidth: 1, padding: 8, marginBottom: 10},
    error: {color:'red', marginTop: 10},
    resultContainer: {marginTop: 20}
});

export default MainView;
``` 

### Controller: Lógica de aplicação

- O Controller atua como intermediário entre o Model e a View, gerenciando a lógica da aplicação
- Ele define o que fazer com as entradas do usuário e manipula os dados antes de exibi-los

```js
import React, {useState} from 'react';
import DataModel from '../models/DataModel';
import MainView from '../views/MainView';

const MainController = () => {
    const [data, setData] = useState(null);
    const [error, setError] = useState('');

    const handleSearch = async (cep) => {
        try {
            setError('');
            const result = await DataModel.fetchCEP(cep);
            setData(result);
        } catch (e) {
            setError(e.message);
            setData(null);
        }
    };

    return (
        <MainView
            onSearch={handleSearch}
            data={data}
            error={error}
        />
    )
}

export default MainController;
```

### Configuração do arquivo principal do aplicativo

- Aqui, montamos a aplicação, apontando para o Controller principal

```js
import React from 'react';
import MainController from './src/controllers/MainController';

const App = () => {
    return <MainController />;
}

export default App;
```

## Explicação do fluxo

- Usuário Interage com a View
    - O usuário insere um CEP e clica no botão de busca na MainView
- Controller Processa a Interação
    - O MainController recebe o evento onSearch, chamando o método handleSearch com o CEP fornecido
- Model Faz a Requisição à API
    - O handleSearch utiliza o método fetchCEP do DataModel para buscar os dados da API
- Controller Atualiza a View com os Dados
    - Com os dados recebidos da API, o MainController define o estado de data (ou error em caso de falha), que é passado para a MainView
- View Exibe os Dados ao Usuário
    - A MainView exibe os dados ou uma mensagem de erro

## Considerações

- Separação de Responsabilidades
    - O MVC garante que cada parte do código tenha uma responsabilidade específica, facilitando a manutenção e escalabilidade
- Testabilidade
    - Com cada camada separada, é mais fácil testar individualmente a lógica de controle, a interação com a API, e a exibição na interface
- Modularidade
    - Podemos substituir a API sem grandes alterações, pois a lógica está isolada no DataModel