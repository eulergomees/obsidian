Utlização de conjuntos matematicos para funções de identificação de objetos na cena.

## Especificação de conjunto
O conjunto de valores da matriz com valores negativos.

## Reflexão
Se A é o conjunto de pixels que representam um objeto, Então A é o conjunto de 

## Elementos estruturantes
Conjuntp de pequenos ou sub-imagem usados para examinar uma imagem buscando propriedades de interesse.

- Fit: Todos os pixels 1 no elemento estruturante cobrem uma área na imagem também com valores 1.
- Hit: Qualquer pixel 1 o elemento estruturante cobre um elemento 1 da imagem.

O * indica o centro do elemento estruturante, se está omitido então é o centro.

## Erosão
A erosão de um conjunto A sob um conjunto estruturante B.

O elemento estruturante B é sobreposto na imagem de conjunto A, onde ele se movimenta por toda a imagem utilizando seu centro, onde quando ocorre um *fit* dos elementos, o centro é substituido por 1. 

Usada por exemplo para identificação de textos.

Normalmente não usada sozinha, pode ser usada com outras funções para segmentação.

## Dilatação
Reflexão de B em torno de sua origem.
Ao contrario da Erosão que remove informação da imagem, a dilatação aumenta a informação do conjunto.

A dilatação utiliza o *hit* para fazer a verificação.

**Dilatação não é o oposto de erosão!!**

## Abertura
Suaviza o contorno da imagem, quebra, istmos estreitos e elimina protuções finas.
Ela faz uma erosão de A por B seguido da dilatação do resultado por B.

## Fechamento
Suaviza o contorno da imagem, funde as quebras em golfos finos, elimina pequenos buracos e preenche fendar em um contorno.
Ela faz uma dilatação de A por B seguido da erosão do resultado por B.

## Transformada Hit-or-Miss
A transformada hit-or-miss é uma ferramena básica para a detecção de formas: Utiliza dois elementos estruturantes para especificar o padrão a ser detectado na imagem.

