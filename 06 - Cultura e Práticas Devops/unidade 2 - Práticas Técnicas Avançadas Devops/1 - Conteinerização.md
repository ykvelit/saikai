# Conteinerização

## Contexto

- Para maximizar o fluxo, precisamos tornar o trabalho visível, reduzir o tamanho dos lotes e os intervalos de trabalho, aumentar a qualidade evitando que os defeitos sejam passados para os centros de trabalho mais à direita e otimizar constantemente as metas globais

- Mas.. o trabalho tradicional da infraestrutura física em muitas empresas é moroso e repetitivo

- Até pouco tempo atrás, a única forma de disponibilizar  software em produção era através de acesso de trabalho manual de:
    - Provisionamento manual de hardware
    - Instalação manual de SOs e servidores
    - Configuração manual de aplicativos

- O surgimento de tecnologias de virtualização como Hypervisor e programas como o VMWare e VirtualBox começou a facilitar a administração de servidores

- Produtos como o Docker foram criados a partir da evolução de conceitos existentes no Unix nos últimos 30 anos
    - 1979 - chroot system calls
    - 2000 - Free BSD Jails
    - 2001 - Linux Vservers
    - 2004 - Solaris Containers 
    - 2006 - Cgroups (Control Groups)
    - 2013 - Docker

## Conteineres

- São um método de virtualização em nı́vel de sistema operacional que permite executar uma aplicação e suas dependências como processos e com recursos isolados que simulam uma máquina virtual

- Permitem empacotar facilmente o código, as configurações e as dependências de uma aplicação em elementos fundamentais que oferecem consistência ambiental, eficiência operacional, produtividade de desenvolvedores e controle de versões

- Podem ajudar a garantir rapidez, confiabilidade e consistência de implantação, independentemente do ambiente de implantação

- Além disso, eles oferecem um controle mais granular dos recursos, aumentando a eficiência da infraestrutura

## Docker

- O Docker é  uma tecnologia Open Source que permite criar, executar, testar e implantar aplicações distribuı́das dentro de containers de software

- Ele permite que você empacote um software de uma padronizada para o desenvolvimento de software, contendo tudo que é necessário para a execução: 
    - Código
    - Runtime
    - Ferramentas
    - Bibliotecas, etc

- O Docker permite que você  implante aplicações rapidamente, de modo confiável e estável, em muitos ambientes virtuais e fı́sicos
