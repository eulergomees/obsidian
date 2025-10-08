
Segmentação: como é definido o que é o objeto de interesse na cena? 
Se divie as técnicas de segmentação em:
- Segmentação de Descontinuidade
- Segmentação por Similaridade

Segmentar e rotular as partes da imagem/objeto
### Segmentação por Descontinuidade

Operação clássica: Gradiente

- Sobel
- Prewitt
- Scharr

**Pode gerar bordas mais grossas...**

#### Detecção de bordas
Modelos de bordas: 
- Degrau
- Rampa
- Telhado

Toda tarefa que tentamos segmentar algum objeto, é preciso suavizar a imagem antes, para diminuir a quantidade de ruído.

#### Prática
Algoritmo de Canny e comparação com filtro de Sobel

- Primeiro reduz o ruído, logo em seguida é aplicado um filtro passa-alta
- Supressão não-máxima (remoção de pontos que não fazem parte da borda)
- Limiarização