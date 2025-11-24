Senóide é uma função cujo gráfico é identico ao do seno gerado.

## Por que usar ?
É interessante saber quão frequente ocorre alguma intensidade, ou quanto por cento está acima de um certo valor

## Equação da Transformada de Fourier

$$f(t)= \int_{-\infty}^{\infty} f(t)e^{-j_{2}\pi \phi t} dt \to F(\phi) = \int_{-\int_{-\infty}^{\infty} f(t)e^{-j_{2}\pi \phi t}dt }$$

Como não é possivel calcular a transformada em Python, será usada a equação **DISCRETA** de Fourier.

## Transformada discreta

$$
F(u) = \sum _{x=0}^{M - 1}f(x)e^{-j_{2}\pi ux/M}, u=0,1,2,\dots,M - 1$$


