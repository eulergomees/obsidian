Uma grande variedade de filtros para suavizar ou deixar em evidencia mudanças de frequência.

Duas caracteristicas principais:
- Correlação: 
$$
g(x,y) = \sum_{s=-a}\sum_{t=-b}w(s,t)f(x+s,y+t)
$$
- Convolução:
$$
g(x,y) = \sum_{s=-a}\sum_{t=-b}w(s,t)f(x-s,y-t)
$$

Para pixels de borda, sem laterais utilizamos o *padding*, pixels de valor 0 (*default*) na borda externa da imagem para realizar as operações.


### Filtros de suavização

Filtro gaussiano: Utiliza uma função gaussiana para suavizar imagens e sinais, reduzindo  o ruído e desfoques indesejados.
Filtros de mediana: Trata-se de um filtro não linear
Passa baixa: bloquear as frequências altas, no intuito de suavizar a imagem, mais borrada.
Passa alta: deixar mais evidente a transição de frequência de uma imagem.