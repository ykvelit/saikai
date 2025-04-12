# Arquitetura Flux

* Sistema de gerenciamento de 
* Fluxo de execução
    1. UI
    2. Action
    3. Reducer
    4. Store
    5. UI
* Exemplo
    * Redux

## Store

* Armazena o estado de toda a aplicação
* Estado é atualizado a partir de algum *dispatcher*
* Aplicação possui apenas uma única store
* Comparada a um "estado global"

## Actions

* Conteúdos enviados da aplicação para a store
* Descreve **o que** acontece
* Precisa ter uma propriedade *type*
* Apenas uma funcção que retorna um objeto javascript

```js
const SET_USER = 'SET_USER';

const setUser = user => ({
    type: SET_USER,
    payload: user
});
```

## Reducers

* Lógica de negócio
* Descreve **como** as alterações acontecem na store e como os dados são transformados
* Recebe uma *action* como argumento
* Funções puras
    * Não alteram nada diretamente fora do seu escopo

```js
import { SET_USER } from '../actions';

function user(state = {}, action) {
    switch (action.type){
        case SET_USER:
            return {
                ...state,
                user: action.payload
            };
        default:
            return state;
    }
}
```