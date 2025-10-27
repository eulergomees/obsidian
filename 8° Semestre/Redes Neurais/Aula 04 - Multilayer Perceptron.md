A **perceptron** multicamadas (MLP) é uma rede neural semelhante à **perceptron**, mas com mais de uma camada de neurônios em alimentação direta. Tal tipo de rede é composta por camadas de neurônios ligadas entre si por sinapses com pesos.
## Esquema

![[mlp.png]]

# Fase Foward

Fase de leitura das entradas, e primeiros calculos com os pesos iniciados de forma aleatoria. 

### Camada 1 (c =1)

$I^{1}_{J}=\sum_{i = 0}^{n1}W^{1}_{ji}\cdot{X_{i}}$ => $Y^{1}_{j}=g(I^{1}_{j})$
$I^{1}_{j}=W_{10}^{1}\cdot X_{0}+W^{1}_{11}\cdot X_{1}+\dots+W_{1n}^{1}\cdot X_{n}$

### Camada 2 (c =2)

$I^{2}_{J}=\sum_{i = 0}^{n_{2}}W^{2}_{ji}\cdot{Y^{1}_{i}}$ => $Y^{2}_{j}=g(I^{2}_{j})$

### Camada 3 (c =3)

$I^{3}_{J}=\sum_{i = 0}^{n_{3}}W^{3}_{ji}\cdot{Y^{2}_{i}}$ => $Y^{3}_{j}=g(I^{3}_{j})$

### Generalizando

$I^{3}_{j}=\sum^{n}_{i=0} W^{C}_{ji}\cdot X_{i}$

## Cálculo de erro

Considerando que K é o indice da amostra

$P(k)=\frac{1}{2}\sum^{n3}_{j=i}(d_{j}(k)-Y^{3}_{j}(k))^{2}$

Em termos de EQM (Erro Quadratico Médio):

$EQM=\frac{1}{P}\sum^{p}_{k=1}e(k)$

# Fase Backward (backpropagation)

Fase de volta da rede neural, onde o erro obtido é então usado para ajustar os pesos de cada aresta.

**Nosso interesse é calcular o gradiente dos erros**

## Primeira volta (arestas de saída)

