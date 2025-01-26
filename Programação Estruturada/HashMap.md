	## O que é um HashMap?

**HashMap** é uma implementação da INTERFACE **Map** em Java que armazena pares de  chaves-valor (key, value). Ele não garante a ORDEM das inserção dos elementos e permite a associação rápida de valores a chaves **ÚNICAS**. Isso faz com que seja eficiente para buscar e recuperar valores com base em uma **CHAVE(KEY)** .

## Exemplo de Uso do HashMap:
O básico que eu mesmo fiz, consiste em nome de pacientes e a idade deles.

```java
package study;  
  
import java.util.HashMap;  
import java.util.Map;  
  
public class Aula21HashMapNovamente {  
    public static void main(String[] args) {  
  
        Map<String, Integer> pacientes = new HashMap<>();  
        pacientes.put("Mariana", 23);  
        pacientes.put("Mateus", 22);  
        pacientes.put("Beggy", 4);  
  
for(Map.Entry<String, Integer> entry: pacientes.entrySet()){
	String key = entry.getKey();
	Integer value = entry.getValue();

	System.out.println("O paciente: " + key);
	System.out.println("Idade: " + value); 
        }  
  
    }  
}
```

### Explicação do código:
- Criação do HashMap
```java
Map<String, Integer> pacientes = new HashMap<>();
```
- O **paciente** é um **HashMap** que mapeia Strings (nome dos pacientes) para Integers (idade dos pacientes).

### Adição dos Elementos ao HashMap:
```java
pacientes.put("Mariana", 23);
pacientes.put("Mateus", 22);
pacientes.put("Beggy", 4);
```
- Adicionando pares chaves-valores ao **HashMap**.

### Iteração sobre Chaves e Valores:
```java
for(Map.Entry<String, Integer> entry: pacientes.entrySet()){
	String key = entry.getKey();
	Integer value = entry.getValue();

	System.out.println("O paciente: " + key);
	System.out.println("Idade: " + value);
}
```
- Itera sobre TODAS as entradas no **HashMap** (chave e valor).

### Caso precise fazer uma remoção de elementos:
```java
pacientes.remove("Mateus");
```
- Remove o par chave-valor associado à chave "Mateus";

### Verifica se o HashMap está vazio:
```java
if(pacientes.isEmpty()){
	System.out.println("Paciente não compareceu);
} else {
	System.outprintln("Paciente compareceu");
}
```

- Verifica se o **HashMap** está vazio.