Uma requisição em uma **API REST** pode receber diferentes tipos de parâmetros, que são utilizados para fornecer informação adicionais ao servidor. Alguns tipo de parâmetros principais:

-  **Query Parameters**: São parâmetros passados na *URL* da requisição após o ponto de interrogação (**?**). Geralmente são usados para *filtrar*, *ordenar* ou *paginar* resultados. Por exemplo, em uma requisição para buscar livros por título, poderíamos ter algo como: */livros?titulo=HarryPotter*.
```java 
@GetMapping("/metodoComQuery")  
public String metodoComQuery(@RequestParam Map<String, String> allParams){  
    return "O parâmetro com metodoQueryParams é " + allParams.entrySet(); 
}
```
```java
@GetMapping("metodoComQuery/{id}")
public String metodoComQuery(@RequestParam String id) {
	return "O parâmetro com metodoQueryParams é " + id;
}
```
Tem essas 2 formas, mas a primeira é a melhor para se fazer. Deixa muito mais dinâmico e com performance.

-  **Path Parameters**: São parâmetros que fazem parte da **PRÓPRIA URL** e são utilizados para **identificar** um recurso específico. Por exemplo, em */usuarios/{id}*, o *{id}* é um parâmetro de caminho que indica o ID do usuário que deseja acessar.

```java
@GetMapping("/primeiroMetodo/{id}")  
public String primeiroMetodo(@PathVariable String id) {  
    return "O parâmetro é " + id;  
}
```

-  **Request Body**: São dados enviados no **corpo da requisição**, geralmente utilizando os métodos **POST**, **PUT**, ou **PATCH**. Esses dados podem ser formatados em **JSON, XML** ou em outros formatos. O corpo da requisição é frequentemente utilizado para enviar dados para criar ou atualizar algum recurso. Por exemplo, ao criar um *novo usuário*, podemos enviar os dados do usuário no corpo da requisição.

```java
@PostMapping("/metodoComBodyParams")  
public String metodoComBodyParams(@RequestBody Usuario usuario) {  
    return "metodoComBodyParams" + usuario.username();  
}  
  
record Usuario(String username) {  
}
```
o username que está sendo escrito ali, está no body do postman, o record é uma classe sem getters e setters, uma classe simples.

- **Header Parameters**: São parâmetros incluídos no cabeçalho da requisição *HTTP*. Eles são usados para fornecer informações adicionais sobre a requisição, como *autenticação*, *tipo de conteúdo aceito, codificação de caracteres*, entre outros. Por exemplo, um cabeçalho **Authorization**, pode ser usado para enviar um token de AUTH.