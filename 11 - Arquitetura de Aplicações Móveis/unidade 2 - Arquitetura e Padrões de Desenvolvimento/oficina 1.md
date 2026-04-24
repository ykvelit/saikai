# Oficina 1: Implementar um simples aplicativo utilizando o padrão MVC em uma das plataformas escolhidas

## Objetivo

- Para a Oficina 1, onde você implementará um simples aplicativo utilizando o padrão MVC em uma das plataformas, vou orientar cada etapa que pode ser aplicada para as tecnologias sugeridas

### 1. Escolha da Plataforma e Ambiente de Desenvolvimento

Primeiro, escolha a tecnologia para seu app. Aqui estão algumas orientações sobre como começar com cada uma delas:

- React Native
    - Para construir um app em Android e iOS com uma única base de código
    - Instale Node.js, Expo CLI ou React Native CLI
    - npx react-native init MyApp

- Android Nativo (Java/Kotlin)
    - Focado em dispositivos Android
    - Baixe e instale o Android Studio
    - Java ou Kotlin
    - app/src/main/java/com/meuapp

- iOS Nativo (Swift)
    - Para construir um app exclusivo para iOS.
    - Xcode (macOS necessário).
    - Swift.
    - MyApp/Controllers.

- Flutter
    - Para apps multiplataforma em iOS e Android com uma única base de código
    - Instale o Flutter SDK
    - Dart
    - flutter create my_app.

- Progressive Web App (PWA)
    - Para um app acessível via navegador
    - Utilize um editor como Visual Studio Code
    - HTML, CSS, JavaScript (ou frameworks como React.js)
    - Estrutura de pastas padrão com /public para arquivos estáticos

### 2. Estrutura do App com Padrão MVC

O padrão MVC (Model-View-Controller) é uma boa escolha para organizar o código e separar responsabilidades:

- Model
    - Representa a lógica de dados e estado do aplicativo

- View
    - É a interface do usuário (UI), onde os dados são exibidos

- Controller
    - Faz a comunicação entre Model e View, atualizando a UI conforme necessário

Abaixo está o guia para organizar o app com base neste padrão, independente da plataforma

### 3. Implementação do App

Exemplo de um Contador Simples

- Model
    - Gerencia o estado do contador
    
- View
    - Exibe o valor do contador e botões para interação

- Controller
    - Atualiza o valor do contador e comunica as mudanças para a View

- Estrutura do Projeto
    - React Native, Flutter e PWA
        - Crie as pastas model, view, e controller para organizar o código
    - No Android e iOS nativo, utilize pacotes ou namespaces para separar as responsabilidades

### 4. Implementando o Código

Exemplo de Implementação para React Native

Model (Contador.js)
```js
export default class Contador{
    constructor(){
        this.valor = 0;
    }

    incrementar(){
        this.valor += 1;
    }

    decrementar(){
        this.valor -= 1;
    }
}
```

View (App.js)
```js
import React, { useState } from 'react';
import { View, Text, Button } from 'react-native';
import Contador from './model/contador';
import ContadorController from './controller/ContadorController';

const App = () => {
    const [contador, setContador] = useState(new Contador());
    const controller = new ContadorController(contador, setContador);

    return (
        <View>
            <Text>Contador: {contador.valor}</Text>
            <Button title="Incrementar" onPress={() => controller.incrementar()} />
            <Button title="Decrementar" onPress={() => controller.decrementar()} />
        </View>
    )
}

export default App;
```

Controller (ContadorController.js)
```js
export default class ContadorController{
    constructor(model, setModel){
        this.model = model;
        this.setModel = setModel;
    }

    incrementar(){
        this.model.incrementar();
        this.setModel({...this.model});
    }

    decrementar(){
        this.model.decrementar();
        this.setModel({...this.model});
    }
}
```

### 5. Testando o Aplicativo

Execute o aplicativo no emulador ou dispositivo para testar.
- Dependendo da tecnologia escolhida
    - React Native
        - npx react-native run-android 
        - npx react-native run-ios

    - Android Studio
        - Clique em "Run"

    - Xcode
        - Use o botão de "Play" para executar no simulador
    
    - Flutter
        - flutter run
    
    - PWA
        - Abra index.html no navegador

### 6. Resultados e Discussão

Analise os resultados do código, focando em como o padrão MVC permitiu uma separação clara das responsabilidades entre lógica de dados, interface e controle de fluxo