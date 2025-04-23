# Web Assembly

- WASM
- Tipo de código diferente do javascript que consegue rodar nos browsers modernos
- Possibilidade de escrever código web em múltiplas linguagens
    - C++
    - C#
    - Rust
- Linguagem de baixo nível, similar ao Assembly, em um formato binário compacto que roda em cima da plataforma nativa
- Permite que outras linguagens de baixo nível com baixa utilização de memória (C++, Rust) consigam utilizar recursos da web
- Javascript pode ser problemático ao executar aplicações de altíssima complexidade
    - Jogos 3D
    - Realidade aumentada e virtual
    - Edição de image/vídeo
    - [WebAssembly cut Figma's load time by 3x](https://www.figma.com/blog/webassembly-cut-figmas-load-time-by-3x/)
    - [Get Started](https://webassembly.org/getting-started/developers-guide/)
    - [Outros casos de uso](https://webassembly.org/docs/use-cases/)

## Blazor

- Projeto da Microsoft para rodar C# para construção de interfaces ao invés do JS
- C# com .NET Core compila para WebAssembly e roda diretamente no browser
- Compartilha de algumas APIs do JS para uso de funções no browser
- [Get Started]( https://docs.microsoft.com/pt-br/aspnet/core/tutorials/build-a-blazor-app)