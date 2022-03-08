# **PROGRAMANDO COBOL COM LINUX**

Estava buscando outras linguagens para estudo e me deparei com o COBOL.
Então pensei, como posso desenvolver COBOL no Linux(Ubuntu).
E assim nasceu esse repositório.

## Passo 1 - Instalação no linux

O desafio aqui vou encontrar fontes adequadas de informação e fazer o negócio rodar.Após algumas tentativas e erros, esse foi o caminho que funcionou para mim.

No terminal rodei os seguintes comandos para a instalação.

```
sudo apt update
```

```
sudo apt install -y gnucobol
```

```
sudo apt install -y open-cobol
```

Em minha home criei um diretório cobol e abri no vscode. Deste ponto em diante foi bem simples, apenas estudar e codificar...

## Passo 2 - Como compilar e executar COBOl Program

No vscode procurei extensões para debugger cobol.
Mas utilizei o terminal para fazer tal função.
Dentro do diretório do projeto, ṕor exemplo:

>program01
>>hello.cob

Abrir o terminal e rodar o seguinte comando para compilar.

```
cobc -x hello.cob
```

Para executar o programa o seguinte comando.

```
./hello
```

-----------------