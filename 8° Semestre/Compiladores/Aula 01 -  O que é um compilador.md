
Composição básica do compilador: Analisador Léxico, Analisador Sintático, Analisador Semantico, Gerador de Código Intermediário, Otimizador de Código e Geradador de Código Fonte.

**Função de cada parte:**
- Léxico: Separa as instruções em simbolos (lexemas).
- Sintático Analisa as sentenças para garantir que façam sentido gramaticalmente.
- Semântico: Valida o significado e o sentido logico do código, verifica a coerência e compatibilidades de tipos.
- Gerador de Código intermediário: Representação explícita intermediária de um código de baixo nivel (fica entre a liguagem de programação e o Assembly).
- Otimizador de Código: Converte ações redundantes de código, gerando uma versão mais "leve" que não altera seu significado. 
- Gerador de Código Fonte: Mapeia e transforma a interpretação intermediária do código em uma sequência de instruções que realizam a tarefa descrita pela linguagem de alto nível.

**Contexto Hístorico**

Inicialmente todos os programas eram escritos em linguagem de máquina (Assembly).
Final dos anos 50/60 surgiram as linguagens mnemônicas.
	Ex: MOV X,2

Criação das linguagens de alto nível nos anos sequentes (70/80), elas transformam instruções da linguagem (C++ por exemplo) em linguagem de máquina (Assembly) utilizando o seu compilador (MinGW).

Geralmente são mais lentas que linguagens de baixo nível.
Linguagens de baixo nível dão maior controle ao programador quando comparadas as linguagens de alto nível.

Década de 80/90 houve uma predominância das linguagens C,C++ e Java.
Com os novos recursos das linguagens incentivou novas pesquisas sobre otimização de compiladores.

Em 1967, a Programação Orientada a Objeto foi inicialmente introduzida na linguagem Simula, posteriormente incorporada nas linguagens Smalltalk, Java e C++.

**Fundamentos da linguagem de programação**

Estático: ocorre durante a instanciação do código.
	Ex: *public static int* x
	Torna x uma variável de classe e diz que existe apenas uma única cópia de x.
Dinâmico: ocorre durante a execução do codigo.
	Ex: val x
	Torna x uma variável mutavel em Kotlin.
	
Escopo: corpo do programa, determina onde cada variavel e ação pode ser chamada e executada, é delimitado por diferentes formas como chaves para Java ou identação para Python.
Linguagens modernas tem controle explicito de escopo, como public, private e protected.


