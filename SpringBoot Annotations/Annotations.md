**@Controller**: Para marcar classes que tratam requisições **HTTP** e retornam resposta para o cliente.

**@RestController**: Similar ao *@Controller*, mas otimizada para retornar dados no formato JSON em resposta a requisição RESTful.

**@RequestMapping**: É usada em métodos de controle ou em nível de classe em aplicativos Spring MVC para mapear solicitações HTTP para métodos específicos ou para a classe em si.
- Ela pode ser configurada com várias atributos, como `value`, `method`, `params`, `headers`, entre outros, para especificar condições mais precisas de mapeamento.
- Exemplo abaixo:

```java
@Controller
@RequestMapping("/api")
public class MyController {
	@RequestMapping(value = "/hello", method = RequestMethod.GET)
	public String hello() {
		return "Hello World";
	}
}
```
- Nesse exemplo, a URL `/api/hello` mapeia para o método `hello()` quando uma solicitação HTTP GET é feita.

**@RestController**: 
- Essa annotation combina as funcionalidades de *@Controller* e *@ResponseBody*. Ela é usada marcar classes que tratam requisições HTTP e retornam diretamente objetos serializados como respostas (por padrão, no formato JSON).
- É uma abordagem comum para construir APIs RESTful em aplicativos Spring.
```java
@RestController
@RequestMapping("/api")
public class MyRestController {
	@GettingMapping("/hello")
	public String hello() {
		return "Hello World";
	}
}
```

- Esse exemplo retornará simplesmente uma String "Hello World" no corpo da resposta HTTP.

**@RequestParam**: 
- Usada para extrair parâmetros de solicitação HTTP e vinculá-los a parâmetros de método em controladores Spring MVC.
- Ela pode ser usada com vários atributos, como `value`, `required`, `defaultVaue`, etc. 
```java
@GetMapping("/greet")
public String greet(@RequestParam("name") String name) {
	return "Hello, " + name;
}
```

- Nesse exemplo, o parâmetro `name` é extraído da URL da solicitação e vinculado ao parâmetro `name` do método `greet()`.

**@RequestBody**: Usada para vincular o corpo de uma solicitação HTTP a um objeto de domínio ou outro tipo de objeto em controladores Spring MVC.

**@GetMapping**, **@PostMapping**, **@PutMapping**, **@DeleteMapping**: Annotations que são alternativas mais específicas para `@RequestMapping` para lidar com requisições HTTP GET, POST, PUT e DELETE, respectivamente.
