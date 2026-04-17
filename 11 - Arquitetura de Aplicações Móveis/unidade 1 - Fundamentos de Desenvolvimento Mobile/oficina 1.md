# Oficina 1: Configuração e Instalação dos Ambientes de Desenvolvimento para iOS, Android e Híbridos

## Objetivo

O objetivo desta oficina é a instalação e configuração dos principais ambientes de desenvolvimento necessários para criar aplicações móveis nativas e híbridas. Ao final da oficina, terão um ambiente pronto para começar a desenvolver aplicativos para as plataformas iOS, Android, e soluções híbridas.

## Pré-requisitos
- Computador com permissões administrativas para instalar softwares.
- Conexão estável com a internet.
- Conhecimento básico de desenvolvimento de software.

## Passos para Configuração

### 1. Configuração do Ambiente para Android

- Ferramentas Necessárias:
    - Android Studio: IDE oficial para desenvolvimento Android.
        - Download: [Android Studio](https://developer.android.com/studio?hl=pt-br)
        - Instalar o Android Studio seguindo as instruções da plataforma (Windows, macOS ou Linux).
        - Durante a instalação, certifique-se de incluir o Android SDK, Android Emulator e o Android Virtual Device (AVD).
    - JDK (Java Development Kit): Necessário para compilar aplicativos Android.
        - Para Android Studio, o JDK é configurado automaticamente, mas certifique-se de que está instalado.
        - Verificar a versão: java -version no terminal.

- Configuração Inicial
    - Após instalar o Android Studio, abra-o e crie um novo projeto.
    - Configure um emulador Android na aba AVD Manager.

### 2. Configuração do Ambiente para iOS

- Ferramentas Necessárias:

    - Xcode: IDE oficial para desenvolvimento iOS.
        - Download: Via Mac App Store ou [Apple Developer](https://developer.apple.com/xcode/).
        - Instale e configure o Xcode, incluindo as ferramentas de linha de comando.
    - Xcode Command Line Tools: Ferramentas necessárias para compilar aplicativos iOS via terminal.
        - Comando para instalar: xcode-select --install.
- Configuração Inicial:
    - Abra o Xcode e crie um novo projeto.
    - Verifique se o simulador de iPhone está funcionando corretamente.

### 3. Configuração do Ambiente para Desenvolvimento Híbrido

- Ferramentas Necessárias:

    - Node.js e npm: Ambiente de execução e gerenciador de pacotes.
        - Download: [Node.js](https://nodejs.org/pt-br).
        - Verificar a instalação: node -v e npm -v no terminal.
    - Frameworks Híbridos: Para esta oficina, recomendamos a configuração de frameworks como:
        - React Native:
            - Comando de instalação: npm install -g react-native-cli.
            - Testar a instalação criando um projeto com: react-native init MeuProjeto.
        - Ionic:
            - Comando de instalação: npm install -g @ionic/cli.
            - Criar um novo projeto: ionic start MeuProjeto blank.

- Configuração Inicial:
    - Para React Native: Configurar a conexão com o Android e iOS seguindo a documentação oficial.
    - Para Ionic: Testar o projeto em um emulador Android ou iOS.

## Verificação Final
- Certifique-se de que todos os ambientes estão corretamente instalados.
- Teste a execução de um aplicativo de exemplo em um emulador Android e iOS, bem como a execução de um projeto híbrido.

## Recursos Úteis
- [Documentação do Android Studio](https://developer.android.com/studio/intro?hl=pt-br)
- [Guia de Instalação do Xcode](https://developer.apple.com/support/xcode/)
- [Configuração do React Native](https://reactnative.dev/)