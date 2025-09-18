<!-- PROJECT LOGO -->
<div align="center">
   <a href="https://github.com/othneildrew/Best-README-Template">
      <img src="https://logodownload.org/wp-content/uploads/2014/12/estacio-logo-1-2048x1641.png" alt="estacio logo" width="80"                  height="80">
   </a>
    <h1 align="center"> Universidade Estácio de Sá </h1>
     <hr>
</div> 

* DESENVOLVIMENTO FULL STACK- 
* Disciplina: DGT2812  - Posso criar um App de outra forma.
* Semestre Letivo: 2025.2
* Repositorio Git:https://github.com/noxxcanjo/Missao-2-Mundo-4/
<hr>

* [Gabriel Arcanjo Garrido ](https://github.com/noxxcanjo) - MATRICULA:  2024.02.62009-6
<hr>
 <h1 align="center"> Missão Prática | Nível 2 | Mundo 4 </h1>
 <h2 align="left" > Posso criar um App de outra forma. </h2> 
 <h3>Microatividade 1: Preparação do ambiente </h3>
 <h3>Microatividade 2: Utilização de Widgets Flutter Básicos - MaterialApp, Scaffold e AppBar </h3>
 <h3>Microatividade 3: Criação de layouts básicos com os Widgets </h3>
 <h3>Microatividade 4: Utilização do Widget ListView em Flutter </h3>
 <h3>Microatividade 5: Desenvolvimento de Outra Funcionalidade para o Widget em Flutter </h3>
 <hr>

 <h2> :clipboard: Objetivos da Prática </h2>

* Instalar e configurar o Flutter SDK e o ambiente de desenvolvimento integrado (IDE)
de acordo com as melhores práticas;
* Empregar Widgets fundamentais, como MaterialApp, Scaffold, AppBar, Text e
RaisedButton;
* Aplicar diferentes Widgets para criar uma interface visual atraente e funcional;
* Aplicar o widget ListView para exibir e gerenciar listas de dados;
* Criar e implementar funcionalidades personalizadas para um Widget específico.
<hr>

<h2> Códigos </h2>

* main.dart

```Dart
import 'package:explore_mundov2/screens/home_screen.dart';
import 'package:explore_mundov2/screens/post_screen.dart';
import 'package:flutter/material.dart';
import 'package:flutter/services.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatefulWidget {
  @override
  State<MyApp> createState() => _MyAppState();
}

class _MyAppState extends State<MyApp> {
  @override
  void initState() {
    super.initState();
    SystemChrome.setEnabledSystemUIMode(SystemUiMode.immersive);
  }

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
        debugShowCheckedModeBanner: false,
        home: HomeScreen(),
        routes: {"/post_screen": (context) => PostScreen()});
  }
}
```

* Contato_screen.dart

``` Dart
import 'package:explore_mundov2/screens/home_screen.dart';
import 'package:explore_mundov2/widgets/post_app_bar.dart';
import 'package:explore_mundov2/widgets/post_bottom_bar.dart';
import 'package:flutter/material.dart';

class ContatoScreen extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    final ThemeData themeData = Theme.of(context);
    return Scaffold(
        body: Column(
      children: <Widget>[
        InkWell(
          onTap: () {
            Navigator.push(
              context,
              MaterialPageRoute(
                builder: (context) => HomeScreen(),
              ),
            );
          },
          child: Container(
            alignment: Alignment.topLeft,
            padding: EdgeInsets.all(10),
            decoration: BoxDecoration(
                color: Colors.white,
                borderRadius: BorderRadius.circular(15),
                boxShadow: [
                  BoxShadow(
                    color: Colors.black26,
                    blurRadius: 6,
                  )
                ]),
            child: Icon(
              Icons.arrow_back,
              size: 28,
            ),
          ),
        ),
        Stack(
          alignment: Alignment.bottomCenter,
          children: <Widget>[
            Image.asset('images/agencia.jpg'),
          ],
        ),
        IntrinsicHeight(
          child: Container(
            decoration: BoxDecoration(
              border: Border(
                bottom: BorderSide(
                  color: themeData.dividerColor,
                ),
              ),
            ),
            child: Row(
              children: <Widget>[
                Expanded(
                  flex: 1,
                  child: Column(
                    children: <Widget>[],
                    mainAxisAlignment: MainAxisAlignment.start,
                  ),
                ),
                Expanded(
                  flex: 4,
                  child: Column(
                    children: <Widget>[
                      Row(
                        children: <Widget>[
                          Expanded(
                            child: Column(
                              crossAxisAlignment: CrossAxisAlignment.start,
                              children: <Widget>[
                                Text('(81)9555-1234'),
                                Text(
                                  'Whatsapp',
                                  style: TextStyle(
                                    fontSize: 11,
                                    color: Colors.grey,
                                  ),
                                ),
                              ],
                            ),
                          ),
                          SizedBox(
                            child: Icon(
                              Icons.message,
                              color: themeData.primaryColor,
                            ),
                            height: 60,
                            width: 60,
                          ),
                        ],
                      ),
                      Row(
                        children: <Widget>[
                          Expanded(
                            child: Column(
                              crossAxisAlignment: CrossAxisAlignment.start,
                              children: <Widget>[
                                Text('(81)3555-6789'),
                                Text(
                                  'Unidade Recife',
                                  style: TextStyle(
                                    fontSize: 11,
                                    color: Colors.grey,
                                  ),
                                ),
                              ],
                            ),
                          ),
                          SizedBox(
                            child: Icon(
                              Icons.call,
                              color: themeData.primaryColor,
                            ),
                            height: 60,
                            width: 60,
                          ),
                        ],
                      ),
                      Row(
                        children: <Widget>[
                          Expanded(
                            child: Column(
                              crossAxisAlignment: CrossAxisAlignment.start,
                              children: <Widget>[
                                Text('(87)3555-6788'),
                                Text(
                                  'Unidade Joao Pessoa',
                                  style: TextStyle(
                                    fontSize: 11,
                                    color: Colors.grey,
                                  ),
                                ),
                              ],
                            ),
                          ),
                          SizedBox(
                            child: Icon(
                              Icons.call,
                              color: themeData.primaryColor,
                            ),
                            height: 60,
                            width: 60,
                          ),
                        ],
                      ),
                      Row(
                        children: <Widget>[
                          Expanded(
                            child: Column(
                              crossAxisAlignment: CrossAxisAlignment.start,
                              children: <Widget>[
                                Text('exploremundo@gmail.com'),
                              ],
                            ),
                          ),
                          SizedBox(
                            child: Icon(
                              Icons.email,
                              color: themeData.primaryColor,
                            ),
                            height: 60,
                            width: 60,
                          ),
                        ],
                      ),
                    ],
                  ),
                ),
              ],
            ),
          ),
        ),
      ],
    ));
  }
}
```

* home_screen.dart

``` Dart
import 'package:explore_mundov2/screens/contato_screen.dart';
import 'package:explore_mundov2/screens/post_screen.dart';
import 'package:explore_mundov2/screens/sobre_screen.dart';
import 'package:explore_mundov2/widgets/home_bottom_bar.dart';
import 'package:flutter/foundation.dart';
import 'package:flutter/material.dart';
import 'package:flutter/rendering.dart';
import 'package:flutter/widgets.dart';

import '../widgets/home_app_bar.dart';

class LugaresModel {
  String lugar_nome;
  String lugar_descricao;
  String lugar_cidadepais;
  String lugar_imagem;

  LugaresModel(this.lugar_nome, this.lugar_descricao, this.lugar_cidadepais,
      this.lugar_imagem);
}

class HomeScreen extends StatefulWidget {
  @override
  _HomeScreen createState() => _HomeScreen();
}

class _HomeScreen extends State<HomeScreen> {
  static List<LugaresModel> lugares = [
    LugaresModel(
        'Rio de Janeiro',
        'Cristo Redentor é uma estátua que retrata Jesus Cristo localizada no topo do morro do Corcovado, a 709 metros acima do nível do mar, com vista para parte considerável da cidade brasileira do Rio de Janeiro. Feito de concreto armado e pedra-sabão, tem trinta metros de altura (uma das maiores estátuas do mundo), sem contar os oito metros do pedestal, sendo a mais alta estátua do mundo no estilo Art Déco. Seus braços se esticam por 28 metros de largura e a estrutura pesa 1145 toneladas.',
        'Rio de Janeiro, Brazil',
        'images/city1.jpg'),
    LugaresModel(
        'Grand Canyon',
        'O Grand Canyon, no Arizona, é uma formação natural constituída de camadas de rocha vermelha, que revelam milhões de anos da história geológica em seção transversal. De vastas proporções, o cânion tem, em média, 16 km de largura e 1,6 km de profundidade ao longo de seu comprimento de 445 km. Grande parte da área é um parque nacional, com as paisagens impressionantes e as corredeiras de águas bravas do Rio Colorado.',
        'Arizona, EUA',
        'images/city2.jpg'),
    LugaresModel(
        'Lisboa',
        ' Torre de Belém, antigamente Torre de São Vicente a Par de Belém, oficialmente Torre de São Vicente,[1] é uma fortificação localizada na freguesia de Belém, concelho e distrito de Lisboa, em Portugal. Na margem direita do rio Tejo, onde existiu outrora a praia de Belém, era primitivamente cercada pelas águas em todo o seu perímetro. Ao longo dos séculos foi envolvida pela praia, até se incorporar hoje a terra firme. Um dos ex libris da cidade, o monumento é um ícone da arquitetura do reinado de D. Manuel I, numa síntese entre a torre de menagem de tradição medieval e o baluarte moderno, onde se dispunham peças de artilharia.',
        'Lisboa, Portugal',
        'images/city3.jpg'),
    LugaresModel(
        'Paris',
        'Torre Eiffel (em francês: Tour Eiffel, /tuʀ ɛfɛl/) é uma torre de treliça de ferro forjado no Champ de Mars, em Paris, França. Tem o nome do engenheiro Gustave Eiffel, cuja empresa projetou e construiu a torre.',
        'Paris, França',
        'images/city4.jpg'),
    LugaresModel(
        'Vaticano',
        'Vaticano ou Cidade do Vaticano, oficialmente Estado da Cidade do Vaticano (em italiano: Stato della Città del Vaticano [tʃitˈta del vatiˈkaːno]; em latim: Civitas Vaticana),[7] é a sede[8] da Igreja Católica e uma cidade-Estado soberana sem costa marítima, cujo território consiste de um enclave murado dentro da cidade de Roma, capital da Itália. Com aproximadamente 44 hectares (0,44 km²) e com uma população estimada de 1 000 habitantes, é a menor entidade territorial do mundo administrada por um Estado.[9][10]',
        'Vaticano, Italia',
        'images/city5.jpg'),
    LugaresModel(
        'Ilhas Maldivas',
        'A República das Maldivas (em divehi: ދިވެހިރާއްޖޭގެ ޖުމްހޫރިއްޔާ, transl. Dhivehi Raajjeyge Jumhooriyya) é um pequeno país insular situado no Oceano Índico ao sudoeste do Sri Lanka e da Índia, ao sul do continente asiático, constituído por 1 196 ilhas, das quais 203 são habitadas, localizadas a cerca de 450 km ao sul da península do Decão. A sua única fronteira real é com o território indiano das Laquedivas, a norte, mas são também os vizinhos mais próximos do Território Britânico do Oceano Índico, um conjunto de ilhas localizadas ao sul das Maldivas.',
        'Ilhas Maldivas',
        'images/city6.jpg')
  ];

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: PreferredSize(
          preferredSize: Size.fromHeight(90.0),
          child: Padding(
            padding: EdgeInsets.all(20),
            child: Row(
              mainAxisAlignment: MainAxisAlignment.spaceBetween,
              children: [
                SizedBox(
                  width: 180,
                  child: TextField(
                    onChanged: (value) => searchLugar(value),
                    decoration: InputDecoration(
                      border: OutlineInputBorder(),
                      labelText: 'Pesquisar Destino',
                    ),
                  ),
                ),
                InkWell(
                  onTap: () {
                    Navigator.push(
                      context,
                      MaterialPageRoute(
                        builder: (context) =>
                            ContatoScreen(), // Fazer a pagina contato screen!!
                      ),
                    );
                  },
                  child: Container(
                    padding: EdgeInsets.all(10),
                    decoration: BoxDecoration(
                        color: Colors.white,
                        borderRadius: BorderRadius.circular(15),
                        boxShadow: [
                          BoxShadow(
                            color: Colors.black26,
                            blurRadius: 6,
                          )
                        ]),
                    child: Icon(
                      Icons.phone,
                      size: 28,
                    ),
                  ),
                ),
                InkWell(
                  onTap: () {
                    Navigator.push(
                      context,
                      MaterialPageRoute(
                        builder: (context) =>
                            SobreScreen(), // Fazer a pagina contato screen!!
                      ),
                    );
                  },
                  child: Container(
                    padding: EdgeInsets.all(10),
                    decoration: BoxDecoration(
                      color: Colors.white,
                      borderRadius: BorderRadius.circular(15),
                      boxShadow: [
                        BoxShadow(color: Colors.black26, blurRadius: 6),
                      ],
                    ),
                    child: Icon(
                      Icons.people,
                      color: Color.fromARGB(255, 0, 0, 0),
                      size: 28,
                    ),
                  ),
                )
              ],
            ),
          )),
      body: SafeArea(
          child: Padding(
        padding: EdgeInsets.symmetric(vertical: 30),
        child: SingleChildScrollView(
          child: Column(
            children: [
              SizedBox(height: 10),
              ListView.builder(
                  physics: NeverScrollableScrollPhysics(),
                  itemCount: display_list.length,
                  shrinkWrap: true,
                  itemBuilder: (BuildContext context, int index) {
                    return Padding(
                      padding: EdgeInsets.all(15),
                      child: Column(
                        children: [
                          InkWell(
                            onTap: () {
                              Navigator.pushReplacementNamed(
                                  context, "/post_screen",
                                  //arguments: index + 1,
                                  arguments: LugaresModel(
                                    display_list[index].lugar_nome,
                                    display_list[index].lugar_descricao,
                                    display_list[index].lugar_cidadepais,
                                    display_list[index].lugar_imagem,
                                  ));
                            },
                            child: Container(
                              height: 200,
                              decoration: BoxDecoration(
                                color: Colors.black,
                                borderRadius: BorderRadius.circular(15),
                                image: DecorationImage(
                                  image: AssetImage(
                                      display_list[index].lugar_imagem),

                                  /// AssetImage("images/city${index + 1}.jpg"),
                                  fit: BoxFit.cover,
                                  opacity: 0.8,
                                ),
                              ),
                            ),
                          ),
                          Padding(
                            padding: EdgeInsets.only(top: 10),
                            child: Row(
                              mainAxisAlignment: MainAxisAlignment.spaceBetween,
                              children: [
                                Text(
                                  display_list[index].lugar_nome,
                                  style: TextStyle(
                                    fontSize: 20,
                                    fontWeight: FontWeight.w600,
                                  ),
                                ),
                              ],
                            ),
                          ),
                          SizedBox(height: 5),
                          Row(children: [
                            Icon(
                              Icons.star,
                              color: Colors.amber,
                              size: 20,
                            ),
                            Text(
                              "4.5",
                              style: TextStyle(
                                fontWeight: FontWeight.w500,
                              ),
                            )
                          ]),
                        ],
                      ),
                    );
                  })
            ],
          ),
        ),
      )),
      //bottomNavigationBar: HomeBottomBar(),
    );
  }

  List<LugaresModel> display_list = List.from(lugares);

  void searchLugar(String valor) {
    setState(() {
      display_list = lugares
          .where((element) =>
              element.lugar_nome.toLowerCase().contains(valor.toLowerCase()))
          .toList();
    });

    print(display_list.first.lugar_imagem);
  }
}
```

* post_screen.dart

``` Dart
import 'package:explore_mundov2/screens/home_screen.dart';
import 'package:explore_mundov2/widgets/post_app_bar.dart';
import 'package:explore_mundov2/widgets/post_bottom_bar.dart';
import 'package:flutter/material.dart';

class PostScreen extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    var data = (ModalRoute.of(context)!.settings.arguments) as LugaresModel;

    return Container(
      decoration: BoxDecoration(
        image: DecorationImage(
          image: AssetImage(data.lugar_imagem),
          fit: BoxFit.cover,
          opacity: 0.7,
        ),
      ),
      child: Scaffold(
        backgroundColor: Colors.transparent,
        appBar: PreferredSize(
          preferredSize: Size.fromHeight(90),
          child: PostAppBar(),
        ),
        bottomNavigationBar: PostBottomBar(),
      ),
    );
  }
}
```

* sobre_screen.dart

``` Dart
import 'package:explore_mundov2/screens/home_screen.dart';
import 'package:flutter/material.dart';

class SobreScreen extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        body: SafeArea(
          child: Column(
            mainAxisAlignment: MainAxisAlignment.center,
            children: <Widget>[
              InkWell(
                onTap: () {
                  Navigator.push(
                    context,
                    MaterialPageRoute(
                      builder: (context) => HomeScreen(),
                    ),
                  );
                },
                child: Container(
                  alignment: Alignment.topLeft,
                  padding: EdgeInsets.all(10),
                  decoration: BoxDecoration(
                      color: Colors.white,
                      borderRadius: BorderRadius.circular(15),
                      boxShadow: [
                        BoxShadow(
                          color: Colors.black26,
                          blurRadius: 6,
                        )
                      ]),
                  child: Icon(
                    Icons.arrow_back,
                    size: 28,
                  ),
                ),
              ),
              CircleAvatar(
                  radius: 70,
                  backgroundImage: AssetImage('images/agencia.jpg')),
              Text(
                'Explore Mundo',
                style: TextStyle(
                    fontFamily: 'Pacifico',
                    fontSize: 30,
                    fontWeight: FontWeight.bold),
              ),
              SizedBox(
                height: 20,
                width: 150,
                child: Divider(
                  color: Color(0xfff07b3f),
                ),
              ),
              Card(
                margin: EdgeInsets.symmetric(vertical: 2, horizontal: 25),
                child: ListTile(
                  leading: Icon(
                    Icons.email,
                  ),
                  title: Text(
                    'Explore Mundo foi fundada em 2024 com o desejo de mudar o mundo. Estabelecemos a melhor plataforma de pacote de viagens do mundo e essa é nossa missão. Nossa equipe está totalmente distribuída ao redor do mundo. Estamos sempre em busca de grandes talentos que compartilhem dos mesmos valores e sejam tão entusiasmados quanto nós. Atendemos a milhares de clientes de 128 países em todo o mundo.',
                    style: TextStyle(
                      fontFamily: 'SourceSansPro',
                      fontSize: 15,
                    ),
                  ),
                ),
              ),
            ],
          ),
        ),
      ),
    );
  }
}
```
* home_app_bar.dart

```Dart
import 'package:explore_mundov2/screens/contato_screen.dart';
import 'package:explore_mundov2/screens/home_screen.dart';
import 'package:explore_mundov2/screens/sobre_screen.dart';
import 'package:flutter/material.dart';
import 'package:flutter/services.dart';

class HomeAppBar extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Padding(
      padding: EdgeInsets.all(20),
      child: Row(
        mainAxisAlignment: MainAxisAlignment.spaceBetween,
        children: [
          SizedBox(
            width: 180,
            child: TextField(
              decoration: InputDecoration(
                border: OutlineInputBorder(),
                labelText: 'Pesquisar Destino',
              ),
            ),
          ),
          InkWell(
            onTap: () {
              Navigator.push(
                context,
                MaterialPageRoute(
                  builder: (context) =>
                      ContatoScreen(), // Fazer a pagina contato screen!!
                ),
              );
            },
            child: Container(
              padding: EdgeInsets.all(10),
              decoration: BoxDecoration(
                  color: Colors.white,
                  borderRadius: BorderRadius.circular(15),
                  boxShadow: [
                    BoxShadow(
                      color: Colors.black26,
                      blurRadius: 6,
                    )
                  ]),
              child: Icon(
                Icons.phone,
                size: 28,
              ),
            ),
          ),
          InkWell(
            onTap: () {
              Navigator.push(
                context,
                MaterialPageRoute(
                  builder: (context) =>
                      SobreScreen(), // Fazer a pagina contato screen!!
                ),
              );
            },
            child: Container(
              padding: EdgeInsets.all(10),
              decoration: BoxDecoration(
                color: Colors.white,
                borderRadius: BorderRadius.circular(15),
                boxShadow: [
                  BoxShadow(color: Colors.black26, blurRadius: 6),
                ],
              ),
              child: Icon(
                Icons.people,
                color: Color.fromARGB(255, 0, 0, 0),
                size: 28,
              ),
            ),
          )
        ],
      ),
    );
  }

}
```

* home_bottom_bar.dart

```Dart
import 'package:curved_navigation_bar/curved_navigation_bar.dart';
import 'package:flutter/material.dart';

class HomeBottomBar extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return CurvedNavigationBar(
      backgroundColor: Colors.transparent,
      index: 2,
      items: [
        Icon(Icons.person_2_outlined, size: 30),
        Icon(Icons.favorite_outline, size: 30),
        Icon(Icons.home, size: 30),
        Icon(Icons.location_city_outlined, size: 30),
        Icon(Icons.list, size: 30),
      ],
    );
  }
}
```
* post_app_bar.dart

```Dart
import 'package:explore_mundov2/screens/home_screen.dart';
import 'package:flutter/material.dart';

class PostAppBar extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Padding(
      padding: EdgeInsets.all(20),
      child: Row(
        mainAxisAlignment: MainAxisAlignment.spaceBetween,
        children: [
          InkWell(
            onTap: () {
              Navigator.push(context,
                                MaterialPageRoute(
                                  builder: (context) => HomeScreen(),
                                ),);
            },
            child: Container(
              padding: EdgeInsets.all(10),
              decoration: BoxDecoration(
                  color: Colors.white,
                  borderRadius: BorderRadius.circular(15),
                  boxShadow: [
                    BoxShadow(
                      color: Colors.black26,
                      blurRadius: 6,
                    )
                  ]),
              child: Icon(
                Icons.arrow_back,
                size: 28,
              ),
            ),
          ),
          InkWell(
            onTap: () {},
            child: Container(
              padding: EdgeInsets.all(10),
              decoration: BoxDecoration(
                color: Colors.white,
                borderRadius: BorderRadius.circular(15),
                boxShadow: [
                  BoxShadow(color: Colors.black26, blurRadius: 6),
                ],
              ),
              child: Icon(
                Icons.favorite,
                color: Colors.redAccent,
                size: 28,
              ),
            ),
          )
        ],
      ),
    );
  }
}
```

* post_bottom_bar.dart

```Dart
import 'package:explore_mundov2/screens/home_screen.dart';
import 'package:flutter/material.dart';

class PostBottomBar extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    var data = ModalRoute.of(context)!.settings.arguments as LugaresModel;
    Column _buildButtonColumn(Color color, IconData icon, String label) {
      return Column(
        mainAxisSize: MainAxisSize.min,
        mainAxisAlignment: MainAxisAlignment.center,
        children: [
          Icon(icon, color: color),
          Container(
            margin: const EdgeInsets.only(top: 8),
            child: Text(
              label,
              style: TextStyle(
                fontSize: 12,
                fontWeight: FontWeight.w400,
                color: color,
              ),
            ),
          ),
        ],
      );
    }

    Color color = Theme.of(context).primaryColor;

    Widget buttonSection = Row(
      mainAxisAlignment: MainAxisAlignment.spaceEvenly,
      children: [
        _buildButtonColumn(color, Icons.call, 'CALL'),
        _buildButtonColumn(color, Icons.near_me, 'ROUTE'),
        _buildButtonColumn(color, Icons.share, 'SHARE'),
      ],
    );

    Widget titleSection = Container(
      padding: const EdgeInsets.all(32),
      child: Row(
        children: [
          Expanded(
            child: Column(
              crossAxisAlignment: CrossAxisAlignment.start,
              children: [
                Container(
                  padding: const EdgeInsets.only(bottom: 8),
                  child: Text(
                    data.lugar_nome,
                    //atracao[int.parse('$data') - 1],
                    style: TextStyle(
                      fontWeight: FontWeight.bold,
                    ),
                  ),
                ),
                Text(
                  data.lugar_cidadepais,
                  //cidadePais[int.parse('$data') - 1],
                  style: TextStyle(
                    color: Colors.grey[500],
                  ),
                ),
              ],
            ),
          ),
          Icon(
            Icons.star,
            color: Colors.red[500],
          ),
          const Text('41'),
        ],
      ),
    );

    Widget textSection = Container(
      padding: const EdgeInsets.all(32),
      child: Text(
        data.lugar_descricao,
        //descricao[int.parse('$data') - 1],
        softWrap: true,
        textAlign: TextAlign.justify,
      ),
    );
    return MaterialApp(
      home: Scaffold(
          body: ListView(
        children: [
          InkWell(
            onTap: () {
              Navigator.push(
                context,
                MaterialPageRoute(
                  builder: (context) => HomeScreen(),
                ),
              );
            },
            child: Container(
              padding: EdgeInsets.all(10),
              decoration: BoxDecoration(
                  color: Colors.white,
                  borderRadius: BorderRadius.circular(15),
                  boxShadow: [
                    BoxShadow(
                      color: Colors.black26,
                      blurRadius: 6,
                    )
                  ]),
              child: Icon(
                Icons.arrow_back,
                size: 28,
              ),
            ),
          ),
          Image.asset(
            data.lugar_imagem,
            //'images/city$data.jpg',
            width: 600,
            height: 400,
            fit: BoxFit.cover,
          ),
          titleSection,
          buttonSection,
          textSection,
        ],
      )),
    );
  }
}
```

 <br>
  <hr>
  
<h1>Resultados: </h1>

<br>
:triangular_flag_on_post: Microatividade 2: 
<img src="https://github.com/Gregdev22/Missao-2-Mundo-4/blob/main/my_app/imagens/MA%205.png" alt="resultado 1" width="640" height="360">

<br>
:triangular_flag_on_post: Microatividade 3: 
<img src="https://github.com/Gregdev22/Missao-2-Mundo-4/blob/main/my_app/imagens/MA%203.png" alt="resultado 1" width="640" height="360">


<br>
:triangular_flag_on_post: Microatividade 4: 
<img src="https://github.com/Gregdev22/Missao-2-Mundo-4/blob/main/my_app/imagens/MA%204.png" alt="resultado 1" width="640" height="360">

<br>
:triangular_flag_on_post: Microatividade 5: 
<img src="https://github.com/Gregdev22/Missao-2-Mundo-4/blob/main/my_app/imagens/MA%205.png" alt="resultado 1" width="640" height="360">

<br>
:triangular_flag_on_post: Explore Mundo App: 
<img src="https://github.com/Gregdev22/Missao-2-Mundo-4/blob/main/explore_mundov2/images/MP%201.png" alt="resultado 1" width="640" height="360">
<img src="https://github.com/Gregdev22/Missao-2-Mundo-4/blob/main/explore_mundov2/images/Home%201.png" alt="resultado 1" width="640" height="360">
<img src="https://github.com/Gregdev22/Missao-2-Mundo-4/blob/main/explore_mundov2/images/Home%202.png" alt="resultado 1" width="640" height="360">
<img src="https://github.com/Gregdev22/Missao-2-Mundo-4/blob/main/explore_mundov2/images/Home%203.png" alt="resultado 1" width="640" height="360">
<img src="https://github.com/Gregdev22/Missao-2-Mundo-4/blob/main/explore_mundov2/images/Contatos.png" alt="resultado 1" width="640" height="360">
<img src="https://github.com/Gregdev22/Missao-2-Mundo-4/blob/main/explore_mundov2/images/Sobrenos.png" alt="resultado 1" width="640" height="360">
<img src="https://github.com/Gregdev22/Missao-2-Mundo-4/blob/main/explore_mundov2/images/Destino%201.png" alt="resultado 1" width="640" height="360">
<img src="https://github.com/Gregdev22/Missao-2-Mundo-4/blob/main/explore_mundov2/images/Destino%202.png" alt="resultado 1" width="640" height="360">
<img src="https://github.com/Gregdev22/Missao-2-Mundo-4/blob/main/explore_mundov2/images/Pesquisa%201.png" alt="resultado 1" width="640" height="360">
<img src="https://github.com/Gregdev22/Missao-2-Mundo-4/blob/main/explore_mundov2/images/Pesquisa%202.png" alt="resultado 1" width="640" height="360">
<img src="" alt="resultado 1" width="640" height="360">

<br>





<br>
<hr>

