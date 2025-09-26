## Regra de Hebb
- Ajuste excitatório: se a saída produzida pela rede está coindidente com a saída esperada, os pesos sinápticos serão estão incrementados proporcionalmente aos valores dos sinais de entrada.
- Ajuste inibitório: Se a saída produzida pela rede é diferente da saída esperada, os pesos sinápticos serão então decrementados proporcionalmente aos valores dos sinais de entrada.
$$
\bar{\omega i} = \bar{\omega} i-1 + \eta \cdot (y - \dot{y}) \cdot \bar{xi}
$$
- wi-1 = O vetor de pesos da época anterior (indicada por i-1);
- eta = A taxa de aprendizagem que determina a velocidade e qualidade da convergência do erro;
- (y - y') = 𝚫, erro, tolerância: a diferença entre o valor esperado y e o valor previsto y';
- xi = O vetor com os valores de entrada na época atual i.

**Curva de convergência de erro:** mecanismo para verificar se a rede está realmente otimizando o problema.
## Fases de treinamento

Fase *forward*:
$$
u = \sum_{i=1} Wi \cdot Xi - \theta
$$
$$
y = g(u)
$$
Fase *backward*:
$$
\bar{\omega i} = \bar{\omega} i-1 + \eta \cdot (y - \dot{y}) \cdot \bar{xi}
$$
