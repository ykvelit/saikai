# REST

## O paradigma REST

> A Transferência de Estado Representacional (REST) é a escolha mais popular para o desenvolvimento da API nos últimos anos

- O paradigma REST é baseado no conceito central de recursos

- Um recurso é uma entidade que pode ser identificada, nomeada, endereçada ou tratada na web

- As APIs REST expõem dados como recursos e usam métodos HTTP padrão para representar transações Criar, Ler, Atualizar e Excluir (CRUD) contra esses recursos

- Por exemplo, a API da Stripe representa clientes, encargos, saldos, reembolsos, eventos, arquivos e pagamentos como 

- REST se tornou o paradigma mais popular para criar APIs nos últimos anos.Ao implementar APIs REST, considere as melhores práticas e guias de desenho

## Regras comuns

- Métodos HTTP como GET, POST, UPDATE e DELETE informam o servidor sobre a ação a ser realizada

- Diferentes métodos HTTP invocados na mesma URL fornecem funcionalidades diferentes

- Criar: Use o POST, na maioria dos casos, para criar novos recursos

- Ler : Use o GET para ler recursos. Requisições GET nunca mudam o estado do recurso. Elas não têm efeitos colaterais. O GET é idempotente

- Atualização: Use o PUT para substituir um recurso e PATCH para atualizações parciais para os recursos existentes. O PUT também é idempotente

- Excluir: Use o DELETE para excluir recursos existentes. O DELETE também é idempotente

- Os recursos fazem parte de URLs, como /usuarios

- Para cada recurso, duas URLs são geralmente implementadas: uma para a coleção, como `/usuarios`, e uma para um elemento específico, como `/usuarios/U123` 

- Nomes são usados em vez de verbos para definir recursos. Por exemplo, em vez de `/lerInformacoesUsuario/U123`, use `/usuarios/U123`

- Os códigos de status de resposta HTTP padrão são devolvidos pelo servidor indicando sucesso ou falha

- Geralmente, códigos na faixa 2XX indicam sucesso, os códigos 3XX indicam que um recurso se moveu, e códigos na faixa 4XX indicam um erro do lado do cliente (como um parâmetro necessário ausente ou muitas solicitações)

- Códigos na faixa 5XX indicam erros do lado do servidor
    - Para saber mais: https://developer.mozilla.org/pt-BR/docs/Web/HTTP

- AS APIs REST podem devolver respostas JSON ou XML. E devido à sua simplicidade e facilidade de uso com JavaScript, o JSON tornou-se o padrão para APIs modernas

- O XML e outros formatos ainda podem ser suportados para facilitar a adoção para clientes que já estão trabalhando com esses formatos usando APIs semelhantes

- No Brasil, o XML é comum em APIs do governo para facilitar a governança de dados (exemplos: NF-E ou E-Social)

- Além das operações típicas da CRUD que acabamos de olhar, as APIs REST às vezes precisam representar operações não-CRUD. 

- As seguintes abordagens são comumente usadas nesse caso
    1. Crie uma ação como um subrecurso. Exemplo:  GET `livros/empromocao`
    2. Crie uma ação através de parâmetros de entrada. Exemplo: GET `livros?tipo=empromocao&categoria=autoajuda`
