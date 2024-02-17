A criação de objetos criados para embrulhar os dados do tipo primitivo, no wrapper classes tem um objeto sendo criado de forma que eu consiga manipular os meus dados, e para cada tipo primitivo nós temos um wrapper classes.

Ás vezes você pode precisar tratar esses tipos primitivos como objetos. É ai que entram as classes wrappers.

As classes wrappers em Java são classes que fornecem uma maneira de encapsular (ou "empacotar") valores primitivos em objetos.

- int -> Integer
- double -> Double
- boolean -> Boolean
- char -> Character
- byte -> Byte
- short -> Short
- long -> Long
- float -> Float

Por exemplo, se você precisar passar um valor int para uma estrutura de dados que aceita apenas objeto (como uma coleção), você pode usar a *classe wrapper* Integer para encapsular esse valor int como um objeto. Da mesma forma, se você precisar de um array de valores booleanos em vez de um array de booleanos primitivos, você pode usar a classe wrapper *Boolean*.


```Java
public class WrapperExample {
	public static void main(Strings[] args) {
		// Usando a classe Wrapper Integer
		Integer num1 = new Integer(10);// Criando um objeto Integer
		int value = num1.intValue(); //Obtendo o valor primitivo
		
		// Usando uma classe Wrapper boolean
		Boolean bool1 = new Boolean(true);// Criando um objeto boolean
		boolean bValue = new.booleanValue(); // obtendo o valor primitivo
	}
}

```

Mas atualmente o jeito que está acima foi depreciado, só estava até o Java 9/8, agora segue assim: 

```Java
Integer tipoInteger = 1;  
  
  
int num22 = tipoInteger.intValue();  
System.out.println(num22);
```

Em resumo, as classes wrappers em Java são classes que permitem que você trabalhe com tipos primitivos como objetos, fornecendo uma camada de abstração e funcionalidades adicionais. Elas são úteis em situações onde você precisa tratar valores primitivos como objetos ou quando precisa usar funcionalidades específicas fornecidas pelas classes wrappers.
