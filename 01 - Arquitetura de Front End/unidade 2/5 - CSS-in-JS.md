# CSS-in-JS

* Formato de escrita de CSS em arquivos JavaScript
* Classes CSS podem ser escritas em formato de função, que são traduzidos em componentes posteriormente
* CSS dinâmico
    * Uma classe CSS pode se comportar de forma diferente de acordo com os parâmetros que são passados
* Suporte a poucos frameworks
    * React 
        * Concentra as maiores opções
        * `styled-components`
        * `emotion`
    * Vue
        * `vue-styled-components`
    * Angular
        * Possui mecanismo próprio
        * Component styles
* Numa árvore de elementos DOM/componentes, fica difícil visualizar o que é componente e o que é estilo

```jsx
import styled from 'styled-components';

export const Header = styled.header`
    background: black;
    color: red;
    font-size: 14px;
`

export const Component = () =>{
    return (
        <div>
            <Header>
                Conteúdo do cabeçalho aqui
            </Header>
        </div>
    )
};
```

```jsx
import styled from 'styled-components';

export const Button = styled.button`
    background: ${props => props.primary ? "green" : "white" };
    color: ${props => props.primary ? "white" : "green" };
`

export const Component = () =>{
    return (
        <div>
            <Button primary>
                Conteúdo do botão
            </Button>
        </div>
    )
};
``` 