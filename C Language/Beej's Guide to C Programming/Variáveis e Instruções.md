#capitulo 
# A memória e suas casas

A memória é como um array de bytes, isto é, um conjunto sequencial de bytes indexado. O índice que usamos para acessar tal memória também é chamado de **endereço**, **local** ou ***pointer*** (ponteiro).

# Variáveis

**Variáveis** são endereços de memória que são capazes de:
1. Armazenar valores.
2. Serem referenciados por um nome, também chamado de **identificador**.

Os nomes de variáveis podem usar quaisquer caracteres de `0-9`, `A-Z`, `a-z` e `_`:
1. Começar com dígitos `0-9`.
2. Começar com dois `_`
3. Começar com `_`, seguido por `A-Z`

De forma geral, caracteres Unicode não tem nenhuma restrição e você pode usá-los sem problemas como identificadores de variáveis.

## Tipos Primitivos

Os tipos primitivos de C são os principais tipos presentes na linguagem, que nos permitem realizar as instruções mais básicas sem tem como os dados, que são **numéricos** devem ser interpretados.

| **Tipo em alto nível**                      | **Exemplo**         | **Tipo em C** |
| ------------------------------------------- | ------------------- | ------------- |
| Inteiro                                     | `67`                | `int`         |
| Número de ponto flutuante                   | `3.14159f`          | `float`       |
| Número de ponto flutuante de dupla precisão | `3.141592653589793` | `double`      |
| Caractere                                   | `'A'`               | `char`        |
| String (array de Caractere)                 | `"Hello, world!"`   | `char *`      |
| Booleano                                    | `false`, `true`     | `bool`        |
| Vazio (diferente de nulo)                   | `void`              | `void`        |

A linguagem C realiza a conversão automática entre tipos se eles forem minimamente compatíveis. Apesar disso, há tipagem forte, ou seja, uma variável, uma vez declarada, não pode ter seu tipo alterado.

### `bool`

O tipo `bool` em C não existe, pelo menos não da forma que esperamos. `0` corresponde à `false` e qualquer número que seja diferente de `0`, como `52`, corresponde à `true`.

## Declarando e inicializando variáveis

O seguinte código:

```C
#include <stdio.h>

int main(void) {
	int i;
	float f;
	
	return 0;
}
```

Ambas as variáveis `i` e `f` não foram inicializadas, o que significa que, dentro delas, há um valor indeterminado armazenado, já que a linguagem considera isso comportamento inesperado.

Sendo assim, é sempre recomendado que variáveis sejam inicializadas. Assim, sempre podemos atribuir valores nas declaração usando [[Operadores e expressões#Aritméticas|`=`]] seguido de algum valor, constituindo uma **inicialização**.

