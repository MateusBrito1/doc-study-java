Validation serve para validar as coisas da sua aplicação, como: `Email`, `Password`, `username`, etc... por exemplo, Ao acessar essa página o usuário requisita a plataforma inserindo seus dados de acesso com 30 caracteres. Porém, a aplicação responde com uma falha que informa que são permitidos apenas 25 caracteres.

Nessa situação acima, a gente pode resolver com **Spring Validation**, uma especificação Java que tem a finalidade de lidar com as validações de dados de um modo centralizado.

## Por que usar o Spring Validation?

1. Proporciona uma resposta mais rápida.
2. Reduz erros (Define um padrão a ser seguido ao longo da programação)
3. Aumentar a produtividade (Reduz a verbosidade do código)

## Como aplicar o Spring Validations nos meus códigos?

A aplicação do Spring Validation é bastante simples e prática. Para isso, a primeira coisa a se fazer é acrescentar dependências no “pom.xml” da plataforma em desenvolvimento.
```java
<dependency>  
    <groupId>org.springframework.boot</groupId>  
    <artifactId>spring-boot-starter-validation</artifactId>  
</dependency>
```

Não é necessário utilizar nenhum **IF and ELSE**, comando responsável por modificar o fluxo de execução de um sistema que está alicerçado no valor. seja ele verdadeira ou falso, quanto a uma expressão que segue determinada lógica. Basta adicionar uma **Annotation Spring Validation**, como @Length, que serve para validar o número máximo ou mínimo de uma caracter permitidos. (O que é muito bom e diminui a verbosidade DE FATO!!).

Por último, para que as validações inseridas sejam reconhecidas e executadas, você deve adicionar *@Valid*. Feito isso, todas as anotações trabalhadas da classe vão ser validadas e implementadas.
![[ValidationImagem.png]]
Assim como na imagem acima.

Há diversos tipos de anotações que podem ser acrescentadas no código. Elas são:
- **@NotEmpty** -> valida quando o campo está vazio;
- **@NotNull** -> valida quando o campo é considerado nulo;
- **@NotBlank** -> valida quando o campo se encontra vazio ou nulo;
- **@Future** -> valida a data atual ou outra posterior;
- **@Past** -> valida a data atual ou outra anterior;
- **@Length** -> valida o tamanho máximo ou mínimo que um campo deve ter;
- **@Min** -> valida um tamanho mínimo que um campo deve ter;
- **@Max** -> valida um tamanho máximo que um campo deve ter;