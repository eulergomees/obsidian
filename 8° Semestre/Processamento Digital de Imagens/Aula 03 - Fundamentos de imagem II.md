**Tipos de vizinhança**
- Vizinhança-4: Um pixel f(x,y) possui 4 vizinhos, 2 horizontais e 2 verticais.
![[viz-4.png]]
- Vizinhança-8: Um pixel f(x,y) possui 8 vizinhos, os 4 mencionados acima e mais 4 nas suas diagonais.
![[viz-8.png]]

**Adjacência**
Dois elementos são adjacentes se forem conexos em pelo menos um elemento.

- Caminho: é uma sequência de pixels, onde cada pixel é adjacente ao proximo (seja por vizinhança 4 ou 8). O número de elementos (o número de pixels representa o comprimento do caminho);
- Região conectada: qualquer região que exxiste pelo menos um caminho entre quaisquer pares de pixels;
- Foreground: Conjunto de todos os elementos conectados da imagem;
- Background: O complemento dos conjuntos conectados (o que sobrou);

**Operações aritméticas**
Funciona como em qualquer matriz. 
Possui soma, subtração, multiplicação e divisão.

Cada imagem possui um intervalo de bits fixo, essas operações são passiveis de estourar esse valor maximo ou minimo (overflow).
		Ex: 
		$$
		L = {2}^k = {2}³ = 8
		$$

Intervalo de 8 pixels, ou seja de 0 até 7.

Para evitar esse tipo de comportamento há algumas técnicas.
- Truncamento: limita os valores ao valor maximo do conjunto de valores possíveis.
$$
g(x,y) = min(g(x,y), L - 1)
$$
- Normalização:  mapeia um intervalo de valores de brilho para outro segundo uma tabela pré-definida.
$$
g = \frac{L - 1}{gmax - gmin} (g - gmin)
$$
- Wrap-around: em vez de simplesmente limitar a um valor máximo, continuamos a contar dependendo do valor resultate, se o resultado foi 9 e na escala o máximo é 7, começamos a contar novamente.
$$
g(x,y) > L - 1 ? g(x,y) - L: g(x,y)
$$
- Valor absoluto: na subtração, se obtvermos um valor negativo podemos simplesmente utilizar o valor positivo respectivo.
$$
g(x,y) = |g(x,y)|
$$
- Mascaramento: na multiplicação, utilizamos uma matriz que possui somente valores 1 e 0, como resultado obtemos somente a matriz com os elementos principais que a matriz mascara possui.

**Operações lógicas**
Possuindo duas matrizes A e B, temos as seguintes operações lógicas: 
- NOT A: resulta no inverso da matriz A;
- A AND B: resulta no espaço comum entre as duas matrizes;
- A OR B: resulta na soma dos espaços das matrizes;
- A XOR B: resulta na soma dos espaços das matrizes, porem excluindo seus pontos em comum.
