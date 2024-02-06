HashSet é uma coleção em Java, que faz parte da interface `set` . Ele é uma coleção que *NÃO* permite elementos duplicados e NÃO garante a **ORDEM** de inserção, no caso, ele não garante as ordem se for por exemplo: 1, 2, 3, 4, 5. Ele irá ir totalmente aleatório. 

1.   **Sem Duplicatas:** Como mencionado, o `HashSet` não permite elementos duplicados.  Se você precisa armazenar elementos únicos em uma coleção, o HashSet é uma escolha adequada.
2. **Rápida Busca:** As operações de adição, remoção e busca em um `HashSet` têm complexidade O(1) em média, o que significa que são MUITO eficientes.

### Exemplo de Uso:

```Java
importa java.util.HashSet;
public class ExemploHashSet {
	public static void main(Strings[] args) {
		//Criando um HashSet
		Set<String> conjunto = new HashSet<>();

		//Criando Elementos
		conjunto.add("Maça");
		conjunto.add("Banana");
		conjunto.add("Pera");
		conjunto.add("Maça"); //Não será adicionado, já existe.

		//Exibindo conjunto
		System.out.println("Conjunto: " + conjunto);
		//Verificando se contém elemento
		System.out.println("Contém Banana? :" + 
		conjunto.contains("Banana"));
		//Removendo um elemento
		conjunto.remove("Pera");
		System.out.println("Conjunto após remoção " + 
		conjunto);
	}
}
```

### Quando usar HashSet?

- **Sem Duplicatas** : Quando você precisa armazenar elementos **Únicos**.
- **Eficiência em Busca**: Se você precisa realizar *operações de buscas*, adição e remoção eficientes, especialmente quando a ordem dos elementos não são importantes (ordenadas).
- **Não se importar com a ordem**: Se a ordem da inserção dos elementos não é importante para a sua aplicação, o *HashSet* é uma escolha eficiente para sua aplicação.

	Lembre-se, se precisar de uma ordem *especifica* ou **ORDENAÇÃO DOS ELEMENTOS**, você deve considerar o uso de outros `Set` como: *LinkedHashSet* ou *TreeSet*.