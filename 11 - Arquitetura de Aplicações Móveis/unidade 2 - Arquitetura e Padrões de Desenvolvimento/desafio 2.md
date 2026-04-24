# Desafio 2: Construir uma aplicação básica usando um framework híbrido flutter e detalhar o fluxo de desenvolvimento

## Objetivo

- Para o Desafio 2, vamos criar uma aplicação básica em Flutter, que é um framework híbrido muito usado para desenvolvimento de aplicativos móveis, permitindo criar interfaces nativas tanto para iOS quanto para Android a partir de um único código-fonte

- Esse desafio incluirá o uso de widgets básicos e um fluxo simples para exibir dados vindos de uma API REST

- Vamos desenvolver um app que permite ao usuário buscar informações de um filme ou série pelo nome, consumindo uma API pública (como a OMDb API) e exibindo os resultados na interface

## Estrutura e fluxo do aplicativo

### Requisitos

- Tela inicial com campo de busca e botão para pesquisa
- Ao buscar, exibir os detalhes do filme ou série: título, ano de lançamento, gênero e uma breve sinopse
- Tratar erros e exibir uma mensagem caso o filme não seja encontrado

## Etapas do desenvolvimento e fluxo

### Configuração do ambiente de desenvolvimento flutter

- Instalar o Flutter SDK e configurar o Android Studio ou Visual Studio Code
- Criar um novo projeto Flutter:
    - `flutter create movie_search_app`
- Abrir o projeto no editor

### Configuração de dependências

- Adicionar o pacote http para realizar requisições HTTP à API REST
- Atualizar o pubspec.yaml com a dependência
```yaml
dependencies:
    flutter:
        sdk: flutter
    http: ^0.13.3
```
- Executar o comando `flutter pub get` para instalar as dependências

## Estrutura de arquivos sugerida

- `lib/`
    - `main.dart`  
        - Arquivo principal que configura o app
    - `screens/`
        - `search_screen.dart`
            - Tela de busca com o campo de pesquisa e resultados
    - `models/`
        - `movie_model.dart`
            - Classe de dados para o modelo de filme
    - `services/`
        - `api_service.dart`
            - Serviço para realizar a requisição à API

## Desenvolvimento do código

### Definindo o modelo de dados

- Crie o modelo MovieModel para organizar os dados do filme

```dart
class MovieModel{
    final String title;
    final String year;
    final String genre;
    final String plot;

    MovieModel({required this.title, required this.year, required this.genre, required this.plot});

    factory MovieModel.fromJson(Map<String, dynamic> json){
        return MovieModel(
            title: json['Title'] ?? 'N/A',
            year: json['Year'] ?? 'N/A',
            genre: json['Genre'] ?? 'N/A',
            plot: json['Plot'] ?? 'N/A'
        );
    }
}
```

### Criando o serviço de API

- O serviço `ApiService` é responsável por fazer a chamada à API OMDb para buscar os detalhes do filme

```dart
import 'dart:convert';
import 'package:http/http.dart' as http;
import '../models/movie_model.dart';

class ApiService {
    static const String apiUrl = "http://www.omdbapi.com?apikey=YOUR_API_KEY&";

    static Future<MovieModel?> fetchMovie(String title) async {
        final response = await http.get(Uri.parse('${apiUrl}t=${title}'));

        if(response.statusCode == 200){
            final data = json.decode(response.body);
            return MovieModel.fromJson(data);
        } else {
            throw Exception("Erro ao buscar filme");
        }
    }
}
```

### Criando a tela de busca

- A tela principal exibe o campo de busca e os resultados

```dart
import 'package:flutter/material.dart';
import '../services/api_service.dart';
import '../models/movie_model.dart';

class SearchScreen extends StatefulWidget {
    @override
    _SearchScreenState createState() => _SearchScreenState();
}

class _SearchScreenState extends State<SearchScreen> {
    final TextEditingController _controller = TextEditingController();
    MovieModel? _movie;
    String _errorMessage = '';

    void _searchMovie() async {
        try {
            final movie = await ApiService.fetchMovie(_controller.text);

            setState((){
                _movie = movie;
                _errorMessage = '';
            });
        } catch (e) {
            setState((){
                _errorMessage = 'Filme não encontrado';
                _movie = null;
            });
        }
    }

    @override
    Widget build(BuildContext context){
        return Scaffold(
            appBar: AppBar(title: Text('Busca de filme')),
            body: Padding(
                padding: const EdgeInsets.all(16.0), 
                child: Column(
                    children: [
                        TextField(
                            controller: _controller,
                            decoration: InputDecoration(
                                labelText: 'Nome do filme',
                                suffixIcon: IconButton(
                                    icon: Icon(Icons.search),
                                    onPressed: _searchMovie
                                )
                            )
                        ),
                        SizedBox(height: 20),
                        _errorMessage.isNotEmpty
                            ? Text(_errorMessage, style: TextStyle(color: Colors.red))
                            : _movie != null
                                ? Column(
                                    crossAxisAlignment: CrossAxisAligment.start, 
                                    children: [
                                        Text('Título: ${_movie!.title}', style: TextStyle(fontSize: 20, fontWeight: FontWeight.bold)),
                                        Text('Ano: ${_movie!.year}'),
                                        Text('Gênero: ${_movie!.genre}'),
                                        Text('Sinopse: ${_movie!.plot}')
                                    ]
                                )
                                : Container()
                    ]
                )
            )
        );
    }
}
```

### Configurando o arquivo principal do App

- O main.dart será responsável por definir a SearchScreen como a tela inicial

```dart
import 'package:flutter/material.dart';
import 'screens/search_screen.dart';

void main() {
    runApp(MyApp());
}

class MyApp extends StatelessWidget {
    @override
    Widget build(BuildContext context){
        return MaterialApp(
            title: 'Movie Search App',
            theme: ThemeData(
                primarySwatch: Colors.blue
            ),
            home: SearchScreen()
        );
    }
}
```

## Explicação do fluxo lógico

- Tela de Busca (SearchScreen)
    - O usuário digita o nome do filme e clica no botão de busca
    - O método _searchMovie() é acionado, que chama o ApiService para buscar o filme pela API

- Chamada à API (ApiService)
    - O ApiService.fetchMovie() faz uma requisição HTTP à API OMDb
    - Se a requisição for bem-sucedida, retorna um objeto MovieModel com os detalhes do filme
    - Caso contrário, gera uma mensagem de erro que é exibida ao usuário

- Exibição de Dados
    - Após receber os dados, o setState() é utilizado para atualizar a tela com o título, ano, gênero e sinopse do filme
    - Se ocorrer um erro, exibe a mensagem "Filme não encontrado"

## Considerações finais

- Este desafio oferece uma introdução à arquitetura de um aplicativo Flutter
    - Separação de responsabilidades entre Model, Service e UI
    - Tratamento de erros para melhorar a experiência do usuário
    - Uso de widgets básicos e chamadas a uma API REST para dados externos

- Este fluxo é uma boa base para aplicativos maiores e mais complexos, permitindo a expansão para adicionar novas funcionalidades e componentes de forma modular