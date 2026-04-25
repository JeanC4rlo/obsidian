#capitulo

```C
// hello.c
#include <stdio.h>

int main(void) {
    printf("Hello World!\n");
    return 0;
}
```

Todo programa C inicia com instruções de processamento, iniciadas com um #, isso é: `#include` e `#define`. Elas indicam, respectivamente: inclusões de *headers* e definições de valores.

As instruções iniciam sequencialmente a partir da função `main()` e finalizam em seu fechamento de chaves.

A instrução `printf` não existe por padrão em C e é incluída através da instrução de preprocessador `#include <stdio.h>`. Ela *printa* a informação nos parâmetros de maneira formatada - o que significa que `\n` se tornou um caractere de nova linha.

Por fim, `return 0` encerra a função `main()`, ou seja, o programa com código de saída `0`.

Dessa forma, podemos compilar e *linkar* o programa, em Unix, utilizando o [[gcc |`cc`ou `gcc`]]via o comando:

```bash
gcc -o hello hello.c
```

Assim, é gerado um executável de nome `hello`, assim, basta executá-lo com o comando:

```bash
./hello
```

A saída gerada é a seguinte:

```bash
Hello, World!
```
