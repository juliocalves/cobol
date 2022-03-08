# **ESTRUTURA DO PROGRAMA**

Um programa cobol possuí a seguinte estrutura:
>PROGRAMA
>>DIVISÕES
>>>SEÇÕES
>>>>PARAGRAFOS
>>>>>FRASE
>>>>>>COMANDOS

## DIVISION E SECTION

Dentro de um programa há quatro divisões.

- IDENTITIFICATION DIVISION

É a divisão onde o programador e o compilador identificam o programa. Em outras palavras informações de documentação do programa.
Ela não possuí seções entretanto possuí os seguinte parágrafós:

1. PROGRAM-ID.

1. AUTHOR.

1. INSTALLATION.

1. DATE-WRITTEN.

1. DATE-COMPILED.

1. SECURITY.

1. REMARKS.

Essa divisão é obrigatória dentro de um programa, e deve conter no mínimo o parágrafo PROGRAM-ID, o restante dos parágrafos são opcionais, de acordo com a especificação de cada programa.

- ENVIROMENT DIVISION

A divisão de ambiente descreve equipamento e arquivos utilizados para rodar o programa. Ela possuí duas seções:

1. CONFIGURATION SECTION
1. INPUT-OUTPUT SECTION

Cada seção possí os seus parágrafos.

A primeira seção é onde definimos as configurações de equipamentos.
>CONFIGURATION SECTION
>>SOURCE-COMPUTER (Opcional)
>>>OBJECT-COMPUTER (Opcional)
>>>>SPECIAL-NAMES (Relaciona nomes internos a equipamentos)

A segunda seção define opções de entrada e saída.
>INPUT-OUTPUT SECTION
>>FILE-CONTROL (Nomeia e associa arquivos a periféricos)
>>>I-O-CONTROL (Opcional, Define técnicas de controle)

- DATA DIVISION

Define a origem e a definição dos dados. Variáveis e constantes são declaradas aqui. Essa divisão possuí quatro seções.

A file section é onde os arquivos são descritos com seus respectivos arquivos.
>FILE SECTION.

Define todas as aŕeas auxiliares de processamento do programa, ou seja, as variáveis.
>WORKING-STORAGE SECTION

Define comunicação com outros programas. E as variáveis de link. É uma seção opcinal.
>LINKAGE SECTION

Define as telas. Opcional.
>SCREEN SECTION

- PROCEDURE DIVION
E finalmente a divisão da parte lógica do programa.
As sections são feitas pelas rotinas. Importante lembrar que cobol é uma linguagem procedural.

## **REGRAS DE CODIFICAÇÃO COBOL**

### COLUNAS

As colunas de 1 a 6 não podem ser usadas para escrever código.
A coluna 7 ativa a função comentário com um *.
A 7 também pode indicar a continuação de uma linha anterior, indicado por um -.
A partir da coluna 8 temos a área A, onde é definido as divisões, seções, parágrafos e alguns níveis de variáveis.
Da coluna 12 até a coluna 72 é a área B, onde é definidos os parâmetros e comandos cobol.
Da coluna 73 a 80 deixamos em branco pois elas não são interpretadas pelo cobol. Servem para identificação dos comandos do programa.

### VARIÁVEIS

Variáveis em cobol possuem a seguinte estrutura: nível de variável, identificação de variável, o tipo de variável e por último o tamanho da váriavél.

### NÍVEIS

O número de nível é usado para especificar dados em um registro. Define se os itens são elementares ou itens de grupo. Itens elementares podem ser agrupados para criar itens de grupo.

|NÚMERO NÍVEL | DESCRIÇÃO|
|-------------|----------|
|01|Descreve registro de entrada|
|02 a 49| Grupo de itens|
|66|Renomea itens cláusula|
|77|Itens que não podem ser subdivididos|
|88|Nome condição entrada|

### NOME DE VARIÁVEIS

1. Tamanho máximo de 30 caracteres;
1. Não pode conter espaços ou brancos;
1. Pode conter letras, números ou hifens (hifens para serparar);
1. Não pode ser uma palavra reservada cobol;
1. Não pode conter caracteres especiais;
1. Deve conter no minímo um caractere do alfabeto;
1. Sempre uppercase;(na realidade todo o código é feito em uppercase)

### TIPOS

Para definir o tipo de váriavel utilizamo a cláusula PIC (picture) junto com o símbolo de seu tipo. Sua sintaxe de implementação é a seguinte:

``` 
77 NOME-VARIAVEL PIC TIPO-DE-DADOS(TAMANHO)
```
Os simbolos usados na cláusula são os seguintes:

|SÍMBOLO| DESCRIÇÃO|
|-------|----------|
|9|Os valores numérico|
|A|Ordem Alfabética|
|X|Caracteres alfanuméricos|
|V|Decimal implícita|
|S|Sinais|
|P|Casas decimais|
