---
layout: post
title: Shell Scripting
date: 2023-06-21
categories: [programming, bash]
tags: [bash, coding, shell, programming]
---
---

> Artigo ainda em construção, releve os erros. Talves algumas informações estejam incompletas
{: .prompt-warning }

## VARIÁVEIS

Exemplos:

ENV
PATH
HOME
USERNAME
TERM
RANDOM



### Array de ambiente

```bash
testearray=(laranja maça morango)
```

```sh
echo ${testearray[n]}
```


## Funções
```
nome() {
	(...)
}
```


## Arquivo de configuração

![[Pasted image 20230619094814.png]]



### Cálculos matemáticos

```sh
var=$[ operação ]
```

```sh
var1=$[ 3 + 6 ]

echo $var1 # output: 9
```

* bc


### Condicional

```bash
if comando
then
	comandos
fi

#ou

if comando; then
	comandos
else
	comandos
fi



if comando1; then
	comandos
elif comando2
then
	comandos processameto
elif comando3; then
	comandos processamento
fi



```


### Test
```zsh
if test CONDIÇÃO
then
	comandos
fi

# ou

if [CONDIÇÃO]
then
	comandos
fi
```


![[Pasted image 20230620091847.png]]


* _test_ não suporta numeros float

Exemplo

```zsh

#!/bin/bash

n1=10
n2=12

if [ $n1 -eq $n2 ]
then
     echo "$n1 = $n2"
elif [ $n1 -gt $n2 ]
then
	echo "$n1 > $n2"
elif [ $n1 -lt $n2 ]
then
    echo "$n1 < $n2"
else
    echo "erro"
fi
```


![[Pasted image 20230620092940.png]]



### Comparação de arquivos no comando teste

![[Pasted image 20230620093504.png]]



![[Pasted image 20230620094047.png]]


```bash
#!/bin/bash

file=$HOME/.bashrc
if [ $USER = daniel ] && [ -w file ]
then
	echo "$USER tem permição para alterar aquivo $file"
else
	echo "$USER não pode alterar $file"
fi
```

### Comando case

```bash
#!/bin/bash

case <variavel> in
	valor)
		comando1;;
	valor2)
		comandos2;;
	*)
		comandos-padrão;;
esac
```


## Estrutura de repetição

for, while, until

```bash
for valor in lista
do
	comandos
done
```

exemplo
```bash
 #!/bin/zsh

lista=("Laranja" Maçã mamão morango "leite condensado")
n=1

for item in $lista
do
    echo $n " - " $item
    n=$[ $n + 1 ] #ou n=$(($n+1))
done
```




## Parâmetros de linha de comando

./ex.sh param1 param2 ....
$0      $1           $2

$# - numero de parametros


#### Shift

reduz ou passa o parametro para uma variável anterior, ex, valor de $3 passa para => $2

##### Comando read

```bash
read nome -p "nome: "
echo $nome
```


<span><h2>whiptail</h2> caixa de dialogo</span>


``` bash
whiptail --title "Caixa" --msgbox "caixa" --fb 10 50
```


## funções

```bash
function nome_função {
	comandos
}

#ou

nome_funcao(){
	comandos
}

```
## VARIÁVEIS

Exemplos:

ENV
PATH
HOME
USERNAME
TERM
RANDOM



### Array de ambiente

```bash
testearray=(laranja maça morango)
```

```sh
echo ${testearray[n]}
```


## Funções
```
nome() {
	(...)
}
```


## Arquivo de configuração

![[Pasted image 20230619094814.png]]



### Cálculos matemáticos

```sh
var=$[ operação ]
```

```sh
var1=$[ 3 + 6 ]

echo $var1 # output: 9
```

* bc


### Condicional

```bash
if comando
then
	comandos
fi

#ou

if comando; then
	comandos
else
	comandos
fi



if comando1; then
	comandos
elif comando2
then
	comandos processameto
elif comando3; then
	comandos processamento
fi



```


### Test
```zsh
if test CONDIÇÃO
then
	comandos
fi

# ou

if [CONDIÇÃO]
then
	comandos
fi
```


![[Pasted image 20230620091847.png]]


* _test_ não suporta numeros float

Exemplo

```zsh

#!/bin/bash

n1=10
n2=12

if [ $n1 -eq $n2 ]
then
     echo "$n1 = $n2"
elif [ $n1 -gt $n2 ]
then
	echo "$n1 > $n2"
elif [ $n1 -lt $n2 ]
then
    echo "$n1 < $n2"
else
    echo "erro"
fi
```


![[Pasted image 20230620092940.png]]



### Comparação de arquivos no comando teste

![[Pasted image 20230620093504.png]]



![[Pasted image 20230620094047.png]]


```bash
#!/bin/bash

file=$HOME/.bashrc
if [ $USER = daniel ] && [ -w file ]
then
	echo "$USER tem permição para alterar aquivo $file"
else
	echo "$USER não pode alterar $file"
fi
```

### Comando case

```bash
#!/bin/bash

case <variavel> in
	valor)
		comando1;;
	valor2)
		comandos2;;
	*)
		comandos-padrão;;
esac
```


## Estrutura de repetição

for, while, until

```bash
for valor in lista
do
	comandos
done
```

exemplo
```bash
 #!/bin/zsh

lista=("Laranja" Maçã mamão morango "leite condensado")
n=1

for item in $lista
do
    echo $n " - " $item
    n=$[ $n + 1 ] #ou n=$(($n+1))
done
```




## Parâmetros de linha de comando

./ex.sh param1 param2 ....
$0      $1           $2

$# - numero de parametros


#### Shift

reduz ou passa o parametro para uma variável anterior, ex, valor de $3 passa para => $2

##### Comando read

```bash
read nome -p "nome: "
echo $nome
```


<span><h2>whiptail</h2> caixa de dialogo</span>


``` bash
whiptail --title "Caixa" --msgbox "caixa" --fb 10 50
```


## funções

```bash
function nome_função {
	comandos
}

#ou

nome_funcao(){
	comandos
}

```


