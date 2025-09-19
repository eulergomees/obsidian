É a primeira fase de um compilador.

A tarefa principal do analisador léxico é ler os objetos e agrupa-los em " objetos do tipo token".
Trata as construções de multiplos caracteres como identificadores.
Os **identificadores** são sequências de caracteres.
	Ex: *cont* + 1
	o identificador *cont* é tratado como uma unidade.

Um token é um par consistido em um nome e um valor de atributo opcional.

Lexema: é uma sequencia de caracteres no possui um padrão léxico dentro da linguagem.

Os tokes podem ser divididos em dois grupos:
- Simples: palavras reservadas, que não tem um valor associado.
- Com argumento: possuem um valor associado e corresponde a elementos da linguagem definidos pelo programador.

Identificadores: palavras para nomear entidades do programa.
	Ex: var, func
Literais: sequencia de caractesres que representa uma constante.
	Ex: um número inteiro, um número float
Palavras-chave: palavras usadas para representar estruturas de linguagem.
	Ex: while, if, else.
Sinais de pontuação: sinais que auxiliam na escrita de programas.
	Ex: ponto e virgula, chaves

O analisador léxico ignora espaços em branco.
Trata todos os números.
Comentarios são ignorados.

As quebras de linhas são contabilizadas (conta a quantidade de \n), utilizadas posteriormente para indicar possiveis erros em partes especificas dos código.

### **Atributos de tokes**

O analisador léxico deve fornecer às fases subsequentes do compilador informações adicionais sobre qual foi o lexema em particular casado.

Cada token deve ter seu padrão muito bem definido para não gerar ambiguidade.

### **Reconhecendo palavras-chave**

Palavras-chave são reservadas pela linguagem, ou seja são únicas dentro da linguagem.
É necessario um mecanismo para decidir quando um lexema forma uma palavra-chave.
Uma sequência de caracteres forma um identificador apenas se não for uma palavra-chave.

Representação única.

Ex: *int* var1
O compilador lê o var1 e o procura na tabela de simbolos, como não o encontra ele o insere na tabela, atribuindo um valor e um id para ele no formato: <var1, id>

As palavras reservadas já estão identificadas na linguagem, ela é inicializada previamente, não sendo necessário os passos anteriores.

Uma tabela de sequências de caracteres pode ser implementada como uma tabela hash. 

Qual a sequência de tokens? 

*while* indice < 10 do:
	indice:= total + indice;

Resposta: <while, >, <indice, id>, <<, >, <10, number>, <do, >, <indice, id>, < :=, >, <total, id>, <+,>, <indice, id>, <;, >.

### Tabela de simbolos

Estruturas de dados que contém informações sobre as contruções do programa fonte.
A informações são coletadas de modo incremental pelas fases de análise de um compilador.

As entradas da tabela são criadas e utilizadas conforme a utilização do código.
Quando o analisador léxico descobre um lexema que é um identificador ele o insere na tabela de simbolos.

### Erros léxicos

É dificil para um analisador léxico saber que existe um erro no código fonte.
	Ex: fi (a = f(x)) ...
	
Explicação: if é uma palavra reservada para uma função condicional, quando encontrado **fi** pelo analisador léxico ele o identifica de forma correta, pois **fi** está correto como um identificador novo, mas não como a palavra reservada da estrutura condicional.

O compilador seria como uma peneira de coleta de erros que vão se afunilando com a passagem dos analisadores.

### Abordagens de implementação

Software: lex;

