# Camada de Serviços

- Exposição de funcionalidades para a camada de interfaces com usuário ou para sistemas externos

- Movimento de padrão SOA (Arquitetura Orientada a Serviços)

## Por que utilizar a camada de serviços ?
    
- Encapsula as camadas de negócio e dados
    - A camada de interface não precisa conhecer as camadas de negócio e de dados, somente a camada de serviços

- Suporta múltiplas interfaces (reuso)
    - Web, App, Softwares externos, APIs, etc
    - Reutilização dos serviços
    - A interface não deve interferir no funcionamento dos serviços

- Ajuda no isolamento de interface
    - Contribui para o baixo acoplamento
    - Dificulta a construção de código de baixa qualidade

- Geram independência de tecnologia e facilidade de integrações com protocolos padrão

## Características 
    
- Deve permitir concorrência
    - Chamadas em paralelo são premissas
    - Muitas chamadas simultâneas
    
- Não armazena estado (Stateless)
    - Cada chamada é independente
    - Envia o conjunto de dados completo
    - Recebe o retorno completo do processamento

## Contrato

- Padrão command

- Desejável uso de objetos como insumo para chamadas
    - Objetos criados na camada de Domínio / Dados
    - Diminui mudanças na escrita dos métodos

- Desejável uso de objetos ou interfaces como retornos

## SOAP x REST

- SOAP é um protocolo
- REST é uma arquitetura (usa protocolo existente)
- SOAP expões comportamento
- REST expõe dados
- SOAP é mais pesado e complexo que REST

## SOAP

- Simples object access protocol
- WSDL 
    - Contrato entre consumidor e provedor
- Opção mais pesada, menor performance
- Independência de transporte (HTTP, TCP, etc)
- Tipos bem tipados
- Transfere dados em formato de XML
- Mais opções de segurança, autenticação e autorização
- Possibilidades de automação

## REST

- Representative state transfer
- Mais flexível (ou permissivo)
- Usa sempre HTTP
- Curva de aprendizado menor
- Qualquer formato (Json, XML, CSS, etc)
- Maior Eficiência

## Camada de domínio

- Desenho de um cenário para cada padrão, contextualizando e explicando a escolha pelo padrão

## Camada de serviço

- Desenho de um cenário para uso de REST e outro para uso de SOAP
