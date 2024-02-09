Polimorfismo refere-se à capacidade de um objeto ser referenciado de várias formas, permitindo que métodos sejam invocados de maneira dinâmica.

- **Exemplo:** Em um cenário polimórfico, uma referência de tipo mais genérico pode ser usada para invocar métodos específicos de objetos de tipo mais específicos, o que permite maior flexibilidade e reutilização do código
- **Outro exemplo:** A classe Animal vai conter: *Barulho do animal*, *Cor*, *Patas*. E os outros animais que podem ser herdados desse Animal padrão, podem usá-lo ou adicionar mais alguns outros métodos.

## Uso de implements com Polimorfismo

- Ao usar `Implements`, uma classe concorda em fornecer implementações para todos os métodos definidos na interface que ela está implementando, no caso, ela concorda em distribuir todo o método que contém nela para outras classes usá-las.
- Isso permite alcançar o polimorfismo ao usar referências do tipo interface, em vez do tipo classe concreta.
- **Exemplo:** Se uma classe *Cachorro* IMPLEMENTA a interface *Animal*, você pode usar a uma referência do tipo *Animal* para acessar os MÉTODOS definidos na INTERFACE, mesmo que o objeto seja um *Cachorro*. 

## @Override

A anotação *@Override* é usada para INDICAR quando um método na *SubClasse* está substituindo um método na *SuperClasse*. Ela é recomendada, mas NÃO é obrigatória, desde que você esteja realmente sobrescrevendo um método. Para que o @Override é bom?

- **Clareza e Legibilidade:** O *@Override* melhora a clareza e legibilidade no código, indicando explicitamente que um método está substituindo outro método na hierarquia de classe (Classe pai, Classe Filha).
- **Verificação de Erros:** O compilador verificará se o método com *@Override* realmente está sendo substituindo um método da *SuperClasse*. Se não houver um método correspondente na superclasse, o compilador gerará um erro, alertando sobre o problema. 
- **Prevenção de Erro de Digitação:** Se você cometer um erro de digitação ao escrever o nome de um método que está tentando substituir, o compilador informará que não encontrou o método correspondente na *SuperClasse*, ajudando a evitar bugs difíceis de detectar.

Em resumo, o `@Override` é uma ferramenta útil para melhorar a legibilidade do código e para ajudar a prevenir erros relacionados à substituição de métodos em hierarquias de classes em Java.
