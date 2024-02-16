- Um construtor é um método especial em uma classe Java que é chamado automaticamente quando um objeto dessa classe é instanciado.
- Ele tem o mesmo nome da classe em que está definido.
- Não possui tipo de retorno, nem mesmo void.
- O principal propósito de um *Construtor* é inicializar os atributos de um objeto e prepará-lo para uso.
- Os construtores são *frequentemente usados para definir valores padrão* para os atributos de uma classe.
- Existem *2 tipos de construtores*: o construtor padrão (que não possui parâmetro) e construtores parametrizados (que recebem *argumentos* para inicializar os atributos).
- Construtores são *opcionais* em Java. Se uma classe não tiver nenhum construtor definido, o compilador Java fornecerá um construtor padrão sem parâmetros automaticamente. Mas se um construtor for explicitamente definido na classe, o Java *Não irá montar o construtor padrão*. 
- Os construtores *SÃO frequentemente usados para criar objetos com estados iniciais ESPECIFICOS*, o que pode ser útil em várias situações, como em classe de modelo, onde diferentes objetos podem precisar de valores iniciais diferentes.


## Resumo

Basicamente o que eu entendi é que, o construtor tem que manter o mesmo nome da Classe, senão não funciona. O construtor ele não retorna nada, ele é um void mas nem precisa colocar a nomeclatura `void`. Apenas public e o nome da Classe (constructor). 

Também entendi que os construtores que tiverem argumentos/parâmetros vai ser os atributos que podem ser modificados, no caso por exemplo:

```Java
public Carro(String modelo){
	this.modelo = modelo; // Isso vai ser modificado quando for instanciado.
}
```

Você vai poder mudar o modelo do carro.
Agora, se você não quiser que seja modificado e que o atributo seja padrão/default, você simplesmente ao invés de colocar no argumento/parâmetro, você só precisa colocar desse jeito:

```Java
public Carro(String modelo) {
	this.modelo = modelo;
	this.cor = "preto"; // vai ser esse default
}
```

**Lembrando**: cada construtor pode ser diferente, por exemplo, se eu quiser que em outro construtor o modelo seja default/padrão e não pode ser mudado, eu faço do mesmo jeito que fiz com a cor. E se eu quiser que a cor possa ser modificado, é só fazer do mesmo jeito que fiz com o modelo. Colocar a cor nos argumentos e etc.. MARCHA!

Cada construtor tem sua personalização, leve em conta assim: cada carro que você for na loja tem suas personalização em algumas coisas, vai ter uns que você pode trocar a cor e etc... trocar o motor e assim vai, e outros que você não vai poder trocar nada.

Segue exemplo de um exercício que eu fiz:
[[ConstrutorExemple.png]]
