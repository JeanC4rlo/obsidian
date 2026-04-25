```C
#include <stdio.h>

int main(void) {
    printf("Hello World!");
    return 0;
}
```

Todo programa C inicia com instruções de processamento, iniciadas com um #, isso é: `#include` e `#define`. Elas indicam, respectivamente: inclusões de headers e definições de valores.

As instruções iniciam sequencialmente a partir da função `main()` e finalizam em seu fechamento de chaves.

A instrução `printf` não existe por padrão em C e é incluída através da instrução de preprocessador `#include <stdio.h>`. Ela *printa* a informação nos parâmetros de maneira formatada.

Por fim, `return 0` encerra a função `main()`, ou seja, o programa com código de saída `0`.