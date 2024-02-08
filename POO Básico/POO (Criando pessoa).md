 Na primeira aula que vi de POO, vi sobre criar Packages, por exemplo, caso eu queria criar uma pessoa em POO, eu preciso criar uma *Classe* chamada **Pessoa**. Vou mostrar abaixo de como foi feito:

```Java
package AulaPOO;  
  
public class Pessoa {  
    String nome;  
    int idade;  
    String cpf;  
    String cor;  
  
    String imprimirDadosPessoais() {  
        return "O nome da pessoa é: " + nome + " A idade da 
        pessoa é: " + idade + " O cpf da pessoa é: " + cpf;  
    }  
}
```

#### Packages e Classes

O que são packages? 
As packages (pacotes) são usados para organizar e a agrupar classes relacionadas. Eles ajudam a evitar conflitos

Aqui criamos um Package para aula (AulaPOO), logo após, criamos uma classe que ela é **PÚBLICA**, porque pública? porque ela precisa ser vista por todo a estrutura, para que ela possa ser chamada na instância. Na classe colocamos as características das pessoas, que são:
- Nome (String)
- Idade (Int)
- CPF (String)
- Cor (String)
E podemos colocar mais coisas se quisermos.

#### Método
Logo abaixo de criamos nossa classe de Pessoa com as características de uma pessoa, fizemos um método que retorna algo, o que ela retorna? uma String, pois nela retorna uma frase com o Nome da pessoa, idade da pessoa e o CPF da pessoa.

Se eu não quisesse retorna NADA, eu apenas colocaria **Void** no lugar da **String**. E o que eu colocaria caso eu não quisesse retornar nada?

### Sobre a classe principal que irá rodar o código.

Logo após fazer a classe **Pessoa** nós também precisamos rodar o código, certo? então, tivemos que fazer uma outra classe com o nome *TestePessoa.Java* e nela a gente vai ter que fazer a chamada da Classe **Pessoa** que é onde habita nossas características das pessoas e o método que imprime os dados pessoais. 

Para fazer a instância e chamar os dados para exibir na tela, precisamos fazer as seguintes coisas:

 Vamos ter que instanciar a nossa classe **Pessoa**, mas como? da seguinte forma:
 ```Java
 public static void main(Strings[] args){ 
		Pessoa pessoa = new Pessoa();
 }
```

Aqui estamos fazendo uma **INSTÂNCIA** da nossa classe.
E Logo após vamos ter todas as características da nossa classe **Pessoa** para poder usar nessa instância. Por exemplo:

```Java
pessoa.cpf = "11111";
pessoa.nome = "Mateus";
pessoa.cor = "Negra";
pessoa.idade = 10;
```

Tudo que foi atribuído a classe já estamos podendo usá-la. 
E para podermos exibir isso, vamos ter que fazer o *System.out.println()*.

```Java
System.out.println("O nome da pessoa é: " + pessoa.nome);
//Pode colocar qualquer um.
```

#### Sobre o método que criamos:

O método que criamos que é chamado de Imprimir dados pessoais ele retorna tudo que tem na nossa classe **Pessoa**, pois ele é um método de retorno. No caso, é o seguinte:

O método é:
```Java
String imprimirDadosPessoais() {  
    return "O nome da pessoa é: " + nome + " A idade da pessoa 
    é: " + idade + " O cpf da pessoa é: " + cpf;  
}
```

O método pega o nome, a idade e o CPF, e vai te retornar tudo isso quando você chamar ele lá na classe principal em um SOUT. O que conter na sua chamada que você distribuiu para cada pessoa (nome, CPF, idade etc) colocada em tela, no caso, sem você precisar colocar o ("O nome da pessoa é:  + pessoa.nome) e etc... e o que não tiver, na tela vai aparecer null. E como fariamos essa chamada? 

```Java
System.out.println(pessoa.imprimirDadosPessoais());
```

Desse jeito acima irá mostrar tudo.