### Late em Dart
Utilizar o atributo `late` em variáveis faz com que valores sejam mantidos como nulo por um certo tempo, e caso a variável seja exposta neste tempo o Dart não reconhece esse erro na compilação, ou seja, ocorre um erro de execução. 
### Parâmetros Posicional
```Dart
//aula/person.dart
class Person {
  String name;
  double weight;

  Person(this.name, this.weight) {}
}
```
Dart utiliza parâmetros posicionais, ou seja, os valores dos parâmetros são definidos pela ordem que são inseridos. 
### Parâmetros Nominal

```Dart
//aula/person.dart
class Person {
  String? name;
  double? weight;

  Person({this.name, this.weight}) //parâmetros nominais possui sintaxe própria
}

//aula/main.dart
  var person = Person(name: name, weight: weight);
  var person2 = Person(weight: weight);
  var person3 = Person(name: name);
```
Dart também dá a opção de utilizar parâmetros nominais, na qual preciso nominar cada o atributo que irei passar o valor. 
- Parâmetros nominais são mais flexíveis, então por padrão podem ser nulos, o que significa que não preciso passar todos os parâmetros para instanciar a classe. 

Outra forma de lidar com parâmetros no construtor é utilizar dois pontos (:) e associar os parâmetros aos atributos. 
```Dart
  Person(String name, double weight) : _name = name, _weight = weight;
```

class Person {
  String _name;
  double _weight;

  String get name => _name;
  set nome (String name) => _name = name;

  double get weight {
    return weight;
  }

  void set weight(double weight) {
    if (weight < 0) throw Exception('Invalid weight');
    _weight = weight;
  }
  
  Person(String name, double weight) : _name = name, _weight = weight;
}

[[ddm-atv-01]]