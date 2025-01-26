
1. Declaração de Array 
- `int [] numeros` -> Aqui estamos declarando uma varável chamada *numeros*, que será um array de inteiros (**int**).
- O uso de `[]` indica que essa varável armazenará múltiplos valores do tipo **int**.

2. Intanciaçao do Array
- `new int [3]` -> Estamos criando um novo array do tipo `int` **com tamanho 3**
- o 3 define o tamanho do array, ou seja, quantos elementos ele pode armazenar.

## Como funciona na Memória? 

Quando executamos um código com array de inteiros com 3 posições (ou mais) é criado na memória. Como não atribuimos valores iniciais, cada posição do array será preenchido com o valor padrão de *int*, que é 0.

| índice | Valor |
| ------ | ----- |
| 0      | 0     |
| 1      | 0     |
| 2      | 0     |

## Resumindo: 

Casos de Uso: 
- Se já souber os valores, prefira => `{1, 2, 3}`
- Se precisar inicializar primeiro e preencher depois, use `new int [3] (ou quantos você quiser`.

