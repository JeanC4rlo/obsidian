#comando
# Resumo

O comando `gcc` (GNU C Compiler), padrão Unix para o comando `cc` (C Compiler), é utilizado para a compilação e linkagem de arquivos C, a fim de gerar um executável passível de ser utilizado.

O comando mais simples é:

```bash
gcc -o <executavel> <fonte>.c`
```

Onde `<executavel>` é o nome do arquivo executável e `<fonte>` é o *filename* do arquivo de código fonte.

Também é possível compilar múltiplos arquivos de uma vez:

```bash
gcc -o <executavel> <fonte1>.c <fonte2>.c (...) <fonteN>.c
```

Nesse caso, o `gcc` compila todos os arquivos e faz a linkagem automaticamente.

# Flags

As *flags* mais comuns são:

- `-o <executable>`
	- define o nome do executável.
- `-Wall`  
	- Ativa a maioria dos avisos (_warnings_). Muito importante pra evitar bugs.
- `-Wextra`  
	- Ativa avisos adicionais mais rigorosos.
- `-g`  
	- Inclui informações de debug (usado com `gdb`).
- `-O1`, `-O2`, `-O3`  
	- Níveis de otimização (quanto maior, mais otimizado, mas pode dificultar debug).
- `-c`  
	- Compila o arquivo, mas **não faz a linkagem** (gera `.o`).
	- ```bash
	  gcc -c arquivo.c
	  ```
- `-I<diretorio>`  
	- Adiciona um diretório para busca de headers (`.h`).
- `-L<diretorio>`  
	- Adiciona um diretório para busca de bibliotecas.
- `-l<nome>`  
	- Linka uma biblioteca (ex: `-lm` para matemática).
- `-std=`
	- Permite definir a versão que será compilada.
- `-pedantic`
	- Pede para o compilador ser pedante com a documentação da versão de C requisitada.