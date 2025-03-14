Nesta aula começamos a por a mão na massa e iniciamos a desenvolver em Dart, além de aprender lições como a relevância em dominar termos da programação:
	Saber os nomes técnicos é importante tanto para entrevistas de empregos, quanto para se comunicar de forma eficiente no meio profissional.
### Erro de compilação é melhor do que erro de execução
Quando ocorre um erro de compilação temos um retorno imediato do compilador e vemos o erro sublinhado e destacado no código em si. Já no erro de execução o código, o compilador não é capaz de apontar o local exato do erro, o que exige horas, ou até semanas de debugging para ser solucionado.
### Código e anotações
Abaixo o código exemplo da aula e algumas anotações.

```dart
void main() {

  print("Hello world");
  var id; // usado quando não sei qual será a tipagem do valor. Depois de definido o valor, a tipagem se torna fixa;
  int id2; // tipagem pré-definida.
  dynamic id3; // esse tipo de dado é semelhante ao var, porém a tipagem se torna 
  String nome;
  int idade;
  double peso;
 String? resposta; // em dart temos a política de null-safety, onde elemenos nulos não são permitidos por padrão afim de evitar erros de execução. 
  print('Informe a sua idade: ');
  resposta = stdin.readLineSync()!;
  if (resposta != null) {
    try {
      idade = int.parse(resposta);
      print('a idade é $idade');
    } catch (e) {
      print('a resposta ser número');
    }
  }


  print('Informe o seu nome: ');
  resposta = stdin.readLineSync()!;
  nome = resposta;

  print('O seu nome é $resposta \nvocê tem $idade anos');

}
```
