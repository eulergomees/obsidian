Obter gramáticas livres de contexto que gerem cada uma das seguintes linguagens:
1. {ai bi | i ≥ 0};
	S -> aSb
	S -> vazio

2. {ai bi | i ≥ 1};
	S -> aCb
	C -> aCb
	C -> vazio
	
3. {ai bj | i ≤ j};
	S -> aCb
	C -> aCb | Cb | vazio
	
4. {ai bj |  i < j};
	S -> Cb
	C -> aCb | Cb | vazio

Considere a gramática livre de contexto A-> AA+ | AA* | a
a) Mostre como a cadeia aa+a* pode ser gerada por essa
gramática.
A = AA*
AA* = AA+ A*
AA+ A* = aa+ a*

b) Construa uma árvore de derivação para essa cadeia.
	  A
	   |
	  AA*
	  /  \
   AA+     a
   /  \
a      a

c) Que linguagem essa gramática gera? 
Consiste em um número qualquer de "a, + e *"

Que linguagem é gerada pelas gramáticas a seguir? Em cada caso, justifique sua resposta. Dê um exemplo de derivação de cada gramática.
a) S→ 0S1 | 01 com a cadeia 000111
	0S1 = 00S11
	00S11 = 000111
	A linguagem gerada é 0i 1i | i >= 1
	
b) S→ +SS | * SS | a com a cadeia + * aaa
	+SS = +* SSS
	+* SSS = + * aaa
	A linguagem gerada é + ou * com no minimo de 2 a
	
c) S→ S(S)S | 𝜖 com a cadeia (()())
	S(S)S = S(S(S)S)S
	S(S(S)S)S = S(S(S)S(S)S)S
	Com s = 𝜖, temos: (()())