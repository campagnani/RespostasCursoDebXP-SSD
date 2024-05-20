# Exercícios da aula 1

### **1. Analise as afirmações abaixo e determine quais delas são falsas:**

1. O shell só é capaz de executar seus comandos internos.
2. O shell é um interpretador de comandos programável.
3. Sem a linha do interpretador de comandos, o script será executado pelo shell **não interativo** padrão.
4. No modo **interativo**, o shell só recebe comandos pela entrada padrão.
5. O shell `sh` sempre será encontrado no diretório `/bin` no GNU/Linux.

**Respostas:**
1. Falso. O shell tem a capacidade de executar outros programas.
2. Verdadeiro. Nós podemos criar shell scrips.
3. Falso. Sem o #! o script será executado pelo shell em execução
4. Falso. Nós podemos usar o source para executar comandos 
5. Verdadeiro caso o link simbólico /bin exista, caso contrário pode ser encontrado em /usr/bin/sh.

### **2. Utilizando o `help` e o `man bash`, descubra quais são as opções do *builtin* `compgen` para imprimir listas de...**

Comandos internos do Bash:

```
:~$ compgen -b
```

Palavras reservadas do Bash:

```
:~$ compgen -k
```

Tópicos de ajuda do comando interno `help`:

```
:~$ help help
```

### **3. Pesquise e descubra uma forma de exibir o nome do dispositivo de terminal em uso:**

```
:~$ ls -l /proc/self/fd
```

### **4. Pesquise e elabore comandos que demonstrem as seguintes afirmações:**

*"Imprimir/exibir no terminal"* é o mesmo que escrever no arquivo dispositivo de terminal:

```
:~$ echo oi
oi
:~$ echo oi > /dev/pts/1
oi
```

Quando recebe um comando como argumento da opção `-c`, o Bash é executado no modo **não interativo**:

```
:~$ echo $-
himBHs
:~$ bash -c 'echo $-'
hBc
#Não tem a letra i, logo não é interativo.
```

Em um redirecionamento de leitura, o link simbólico com o dispositivo do terminal é substituído pela ligação com um arquivo:

```
:~$ echo "ls /proc/self/fd -l" > teste
:~$ bash < teste
total 0
lr-x------ 1 thalles thalles 64 mai 19 23:01 0 -> /home/thalles/teste
lrwx------ 1 thalles thalles 64 mai 19 23:01 1 -> /dev/pts/1
lrwx------ 1 thalles thalles 64 mai 19 23:01 2 -> /dev/pts/1
lr-x------ 1 thalles thalles 64 mai 19 23:01 3 -> /proc/31117/fd
```

### **5. Com base nas ajudas do *builtin* `help`, descreva as diferenças entre os comandos `echo` e `printf`:**

**Resposta:** Ambos passam os argumentos para a saída padrão, mas printf permite especificar o formato do argumento. 

### **6. Com base nas diferenças encontradas, reescreva o script `salve.sh` ([da aposila](aula01.md#o-script-final)) usando `printf`:**

Arquivo `salve.sh`:

```
#!/bin/bash
printf 'Salve, simpatia!\n'
```

### **7. Ainda com o script `salve.sh`, faça com que ele escreva a mensagem abaixo com *apenas uma* invocação do comando `echo`.**

```
:~$ ./salve.sh
Salve, simpatia!
Qual é a sua graça?
```

Arquivo `salve.sh`:

```
#!/bin/bash
echo -e 'Salve, simpatia! \nQual é a sua graça?'
```

### **8. Pensando na portabilidade, eu utilizei a seguinte *hashbang* no meu script:**

Arquivo do script:

```
#!/usr/bin/env sh
```

**Perguntas:**

- Essa *hashbang* é válida?

**Resposta (com justificativa):** Sim, o sistema operacional vai procurar por sh no PATH, e vai encontrar.

- Se for válida, ela é necessária para o meu propósito?

**Resposta (com justificativa):** Não, pq o sh é um link simbólico que vai estar sempre disponível no /bin/sh no GNU/Linux. Além disso, a pasta /bin também está disponível nos BSD's e no MacOS, contendo o link sh dentro. Logo poderiamos usar #!/bin/sh, apesar de #!/usr/bin/env sh ser válido.

**Justifique:**

### **9. Qual é o significado da extensão `.sh` no nome do arquivo `salve.sh`?**

**Resposta:** .sh indica que é um arquivo de script shell.




