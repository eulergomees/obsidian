
Valor de intensidade de pixels.

**Histograma:** mostra os niveis de intensidade de brilho de uma imagem.
	Ex: contar quantos pixeis de intensidade 50 de uma imagem.

Com o histograma podemos distinguir diferentes objetos.
Um baixo contraste, pouca diferença de intensidade é ruim para diferenciação de objetos em uma imagem.

**Transformação de intensidade**

Metodos:
- Contrast stretching function: método de aprimoramento de imagem que tenta melhorar uma imagem ampliando o intervalo de valores de intensidade;
- Thresholding function: transforma a imagem RGB em uma imagem binaria (preto e branco);
- Negative function: inverte o histograma da imagem(usadas em campo médico como mamografia).

**Equalização de histograma**

É uma técnica de processamento de imagem utilizada para melhorar o contraste de uma imagem, utilizada para imagens onde seu histograma está alocado muiti para um dos lados.

Função de equalização (transformada de intensidade):
$$
Sk = T(rk) = (L - 1)\sum_{j=0}^k Pr(rj)
$$
