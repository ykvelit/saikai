# RPC e gRPC

- A Chamada de Procedimento Remoto (RPC) é um dos paradigmas mais simples de API, em que um cliente executa um bloco de código em outro servidor

- Enquanto o REST é sobre recursos, a RPC é sobre ações. Os clientes tipificam um nome e argumentos de método para um servidor e recebem de volta JSON ou XML

- As APIs estilo RPC não são exclusivas do HTTP. Existem outros protocolos de alto desempenho que estão disponíveis para APIs estilo RPC, incluindo o Apache Thrift e Google gRPC
    - https://thrift.apache.org
    - https://grpc.io

## Vantagens

- APIs baseadas em verbos facilitam a organização de contratos extensos (dezenas ou centenas de funcionalidades)

- Fornecem facilidade e extensibilidade para produção de APIs

- APIs específicas gRPC possuem performance melhor pois operam obrigatoriamente sobre HTTP/2 e usam protocolos de dados como ProtoBuffer
    - Comparativo: https://github.com/david-cao/gRPCBenchmarks

## Desvantagens

- Curvas de aprendizado de protocolo de dados específicos
- Curvas de aprendizado de protocolos de transporte específicos como o gRPC
