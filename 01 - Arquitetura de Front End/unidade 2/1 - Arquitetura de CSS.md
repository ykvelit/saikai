# Arquitetura de CSS

* Facilidade em manter o projeto
* Organização
* Um CSS mal feito prejudica toda a manutenção de um projeto web
* Refatorar CSS não é fácil
* CSS está ligado diretamente a performance
    * Override de estilos é custoso para o browser
    * Evitar o uso de `!important` diminui o número de re-render na fase de "painting"
    * Existem consultorias de performance especializadas em web
        * https://3perf.com/content
* CSS está diretamente ligado à **escala**
    * Manter a consistência de estilos entre as telas é de suma importância
    * Editar estilos antigos não deve ser uma tarefa difícil
    * Reutilizar estilos já criados é extremamente importante
* Colisão e nome de classes
    * Ao dividir em múltiplos arquivos, vamos decorar todos os nomes para evitar de reperi-los em arquivos diferentes ?
    * O nome das classes e ids dizem respeito ao que realmente fazem ?
* Algumas styles-guides e metodologias tentam resolver tais problemas
    * BEM
        * Block - Element - Modifier
    * OOCSS
        * Object Oriented CSS
    * CSS Funcional
        * Tachyons
        * Tailwind
    * CSS-in-JS