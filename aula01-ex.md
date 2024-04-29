# Exercícios da aula 1

**1. Analise as afirmações abaixo e determine quais delas são falsas:**

1. O shell só é capaz de executar seus comandos internos.
2. O shell é um interpretador de comandos programável.
3. Sem a linha do interpretador de comandos, o script será executado pelo shell **não interativo** padrão.
4. No modo **interativo**, o shell só recebe comandos pela entrada padrão.
5. O shell `sh` sempre será encontrado no diretório `/bin` no GNU/Linux.

**Resposta:** F V V V F

**Justificativas:**
1. O shell tem a capacidade de executar programas.
5. Pode ser encontrado em /usr/bin/sh.

**2. Utilizando o `help` e o `man bash`, descubra quais são as opções do *builtin* `compgen` para imprimir listas de...**

Comandos internos do Bash:

```
:~$ compgen 
```

Palavras reservadas do Bash:

```
:~$ compgen
```

Tópicos de ajuda do comando intermo `help`:

```
:~$ compgen
```

**3. Pesquise e descubra uma forma de exibir o nome do dispositivo de terminal em uso:**

```
:~$
```

**4. Pesquise e elabore comandos que demonstrem as seguintes afirmações:**

*"Imprimir/exibir no terminal"* é o mesmo que escrever no arquivo dispositivo de terminal:

```
:~$ 
```

Quando recebe um comando como argumento da opção `-c`, o Bash é executado no modo **não interativo**:

```
:~$
```

Em um redirecionamento de leitura, o link simbólico com o dispositivo do terminal é substituído pela ligação com um arquivo:

```
:~$ 
```

**5. Com base nas ajudas do *builtin* `help`, descreva as diferenças entre os comandos `echo` e `printf`:**

**Resposta:**

**6. Com base nas diferenças encontradas, reescreva o script `salve.sh` ([da aposila](aula01.md#o-script-final)) usando `printf`:**

Arquivo `salve.sh`:

```
#!/bin/bash


```

**7. Ainda com o script `salve.sh`, faça com que ele escreva a mensagem abaixo com *apenas uma* invocação do comando `echo`.**

```
:~$ ./salve.sh
Salve, simpatia!
Qual é a sua graça?
```

**8. Pensando na portabilidade, eu utilizei a seguinte *hashbang* no meu script:**

Arquivo do script:

```
#!/usr/bin/env sh
```

**Perguntas:**

- Essa *hashbang* é válida?

**Resposta (com justificativa):**

- Se for válida, ela é necessária para o meu propósito?

**Resposta (com justificativa):**

- Se não for válida ou necessária, qual seria a forma correta?

```

```

**Justifique:**

**9. Qual é o significado da extensão `.sh` no nome do arquivo `salve.sh`?**

**Resposta:**




