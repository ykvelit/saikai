# Maturidade de Automação de Ambientes

- A automação de ambientes e infraestrutura como código busca garantir que o provisionamento de ambientes seja realizado de forma automatizada e consistente para o aumento da produtividade e segurança no uso de ambientes virtualizado e de nuvens

## 1 - Inicial

- Aqui softwares, aplicativos e servidores Web são instalados manualmente
- A infraestrutura é física ou virtualizada. Não temos consciência sobre contêineres e orquestradores de contêineres
- O trabalho de infraestrutura e produção é manual e temos, se existirem, scripts locais usados no nível pessoal dos vários SysAdmins

## 2 - Consciente

- Temos consciência sobre o processo de automação de ambientes
- Ferramentas como Docker, Kubernetes, Chef, Puppet, Ansible, Terraform e outras começam a ser experimentadas
- Pequenos scripts de automação de ambientes começam a ser experimentados
- A cultura de infraestrutura como aluguel (nuvens) se torna lugar comum

## 3 - Gerenciado

- Temos uma suíte de ferramentas para automação de ambientes e elas são usadas em larga escala pelos times de produção
- Times de desenvolvimento tem governança para uso de ambientes provisionados dinâmica
- O uso de Docker com repositórios privativos e o uso de Kubernetes e soluções como OpenShift se torna pervasivo por toda a TI
- Ainda não temos instrumentação do processo nem medições dos seus benefícios econômicos

## 4 - Quantitativamente Gerenciado

- Aqui temos automação da infraestrutura em larga escala
- O time está apto a operar seus ambientes em estruturas virtualizadas, nuvem e até mesmo multi-nuvem, conforem direcionadores de negócio e critérios de aptidão dos seus produtos
- O uso de plataformas como Ansible, Terraform e Kubernetes está largamente disseminado, até mesmo em ambientes de desenvolvimento
- Práticas avançadas como Engenharia do Caos são experimentadas
- Temos indicadores claros sobre os benefícios econômicos, temporais e de qualidade no uso da infraestrutura como código