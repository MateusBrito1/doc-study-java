Os métodos Getters e Setters são usadas para poder modificar e acessar os atributos (variáveis de instância) de uma classe de maneira controlada.

1. Getters (Método de Acesso):
- Os métodos getters são usados para obter o valor de um atributo de uma classe.
- Eles geralmente seguem uma convenção de nomenclatura, começando com "get" seguido pelo nome do atributo com a primeira letra em maiúscula
- Eles **NÃO** alteram o estado do objeto, apenas fornecem acesso ao valor do atributo.

2. Setters (Método de Modificação):
- Os métodos setters são os métodos de modificação, são usados para definir o valor de um atributo de uma classe.
- Eles podem te dar a permissão de que você defina um *novo* valor para um atributo, aplicando lógica ou validações, se necessário.
- Um exemplo simples de um método setter para um atributo chamado "idade" seria assim:
```Java
public void setIdade (int novaIdade) {
//Podemos adicionar validação aqui, se necessário.
idade = novaIdade;
}
```