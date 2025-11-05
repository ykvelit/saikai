# Caso Itaú

Estude a apresentação em anexo.

https://d1.awsstatic.com/events/Summits/reinvent2022/ARC309_A-real-world-resilience-evolution-in-the-cloud-framework.pdfLinks para um site externo.

A apresentação em anexo detalha a jornada do Banco Itaú na adoção de práticas de DevOps e na implementação de uma estrutura de Engenharia do Caos para melhorar a resiliência de suas aplicações na nuvem.

O Itaú adotou uma estratégia de modernização que inclui a adoção de uma arquitetura celular desacoplada baseada em microserviços. Isso proporcionou maior agilidade e autonomia para as equipes inovarem através do uso de soluções reutilizáveis. Além disso, a estratégia envolveu o uso de ferramentas que ajudam a monitorar melhor a experiência do cliente e evoluir a plataforma.

A apresentação destaca a importância da observabilidade na evolução da resiliência. O Itaú implementou painéis de controle para monitorar a saúde de seus serviços e mapear as dependências dos serviços. Isso permitiu ao banco garantir que a estrutura pudesse ser usada em larga escala.

A Engenharia do Caos é apresentada como um pilar fundamental do programa de evolução de resiliência do Itaú. O banco desenvolveu um framework para a Engenharia do Caos, que inclui definições de Engenharia do Caos, uma abordagem faseada (preparação, implementação e análise de resultados), um modelo de maturidade de Engenharia do Caos e ferramentas. O banco também realizou uma série de testes de Engenharia do Caos, incluindo o envio de tráfego de clientes (gradualmente de 5% a 50%) de São Paulo para Virgínia e a redução do número de instâncias EC2 ("modo noturno").

A apresentação também discute a validação de dependências críticas. O banco identificou dependências rígidas e suaves em seus serviços e fez um esforço para garantir que as dependências suaves fossem projetadas de forma apropriada para que as interrupções não afetassem o serviço.

O Itaú também revisou sua estratégia de implantação. Anteriormente, o banco usava uma estratégia que distribuía o tráfego entre diferentes zonas de disponibilidade (AZs) em diferentes dias da semana. A nova estratégia envolve a distribuição do tráfego entre as AZs de uma maneira que permita a liberação de novas versões.

Finalmente, a apresentação discute as mudanças nas operações e na observabilidade. O banco implementou painéis executivos para permitir uma visão simples da disponibilidade e facilitar a investigação de problemas. Além disso, o banco explorou maneiras de melhorar o tempo médio para detecção e recuperação de incidentes.