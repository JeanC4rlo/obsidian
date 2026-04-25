#capitulo 

# Operadores

Operadores são caracteres especiais que realizam operações entre valores e/ou [[Variáveis e Instruções#Variáveis|variáveis]].

**Expressões** são instruções que utilizam de operadores.

## Aritméticas

Operadores aritméticos são aqueles que realizam operações matemáticas comuns:

| **Nome**                     | **Operação** | **Descrição**                                                                      |
| ---------------------------- | ------------ | ---------------------------------------------------------------------------------- |
| Atribuição                   | `=`          | Atribui um valor ou expressão solucionável à uma variável.                         |
| Soma                         | `+`          | Soma dois valores                                                                  |
| Subtração                    | `-`          | Subtrai dois valores                                                               |
| Multiplicação                | `*`          | Multiplica dois valores                                                            |
| Divisão                      | `/`          | Divide dois valores, quando os dois são do tipo `int`, ocorre uma divisão inteira. |
| Módulo (ou resto da divisão) | `%`          | Gera o resto da divisão inteira de dois valores.                                   |

Operadores de atribuição compostos combinam uma operação aritmética com a atribuição, atualizando o valor da variável.

### Incremento e decremento

A linguagem C contém operadores de incremento (`++`) e decremento (`--`), eles são equivalentes à `+= 1` e `-= 1` e, portanto, devem ser utilizados apenas com variáveis.

Se o operador vir antes da variável, a operação é realizada antes de qualquer comparação ou resolução de expressão. Já quando ele vem depois da variável, a operação é realizada após qualquer comparação ou resolução de expressão.

## Condicionais

Operadores condicionais são aqueles utilizados em comparações:

| Nome                | Operação | Descrição                                                                 |
| ------------------- | -------- | ------------------------------------------------------------------------- |
| É equivalente?      | ==       | Retorna `true` se a expressão na esquerda é equivalente à da direita.     |
| Não é equivalente?  | !=       | Retorna `true` se a expressão na esquerda não é equivalente à da direita. |
| É menor que?        | <        | Retorna `true` se a expressão na esquerda é menor que a da direita.       |
| É maior que?        | >        | Retorna `true` se a expressão na esquerda é maior que a da direita.       |
| É menor ou igual a? | <=       | Retorna `true` se a expressão na esquerda é menor ou igual à da direita.  |
| É maior ou igual a? | >=       | Retorna `true` se a expressão na esquerda é maior ou igual à da direita.  |

### Operador ternário (`?`)

É usado para avaliar expressões simples, normalmente, dicotomias. Veja sua estrutura:

```C
<expressao_condicional> ? <resultado_se_true> : <resultado_se_false>
```

E um exemplo:

```C
printf("O resultado é: %s", 3 % 2 == 0 ? "Par!" : "Ímpar!");

// SAÍDA
// O resultado é: Ímpar!
```

### Operadores booleanos

Operadores utilizados em conjunto com operadores condicionais, a fim de fazer operações lógicas comuns, como "E", "OU" e "NÃO/NEGAÇÃO". São eles:

| Nome | Operador    |
| ---- | ----------- |
| &&   | E           |
| \|\| | OU          |
| !    | NÃO/NEGAÇÃO |

Eles possuem uma otimização chamada de **curto circuito**, isto é, se alguma avaliação for conclusiva para o restante da expressão, o compilador é capaz de inferir o resultado final, evitando o cálculo redundante de expressões e economizando tempo.

## Especiais

Operadores especiais são aqueles que não correspondem à nenhum dos operadores acima.

### Operador vírgula (`,`)

Avalia expressões, da esquerda para à direita e, por fim, retorna o valor da última operação realizada. Veja exemplos:

```C
x = (1, 2, 3) // x == 3
```

```C
int a = 1, b = 2; // a == 1, b == 2
y = (a += 1, b += 3, a + b)  // y == 7
```

### Operador de tamanho (`sizeof`)

Devolve o tamanho, em bytes, que uma variável, expressão ou tipo utilizam em memória. É utilizado como:

```C
sizeof(<variavel_expressao_ou_tipo>)
```