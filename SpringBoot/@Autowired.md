O *@Autowired* indica um ponto aonde a injeção automática deve ser aplicada. Esta pode ser usada em *Métodos, atributos e construtores*. No exemplo abaixo, podemos verificar um exemplo de uso do Autowired.

```Java
@Service
public class UsuarioService {
	@Autowired
	private ProdutoRepository produtoRepository;

	private final UsuarioRepository usuarioRepository;

	@Autowired
	public UsuarioService(UsuarioRepository usuarioRepository) {
		this.usuarioRepository = usuarioRepository;
	}
}
```

Definimos a anotação acima do local onde queremos que o Spring injete a dependência. É importante lembrar que o Autowired pode ser utilizado apenas *uma vez por construtor*. E também é necessário que a classe a ser injetada pelo Spring esteja anotado com Component (*@Component*) ou uma das suas especialidades (*@Service, @Repository, ou @Controller*).

É possível também definir um parâmetro *required* para injeção obrigatória ou não.

```java
@Autowired(required=true) // ou false.
```

Com o required setado como true, caso o Spring tenha um problema e não consiga injetar a dependência, será disparado uma exceção `UnsatisfiedDependencyException.`

Com o Autowired definido, o Spring pode fazer a sua parte e injetar as dependências.