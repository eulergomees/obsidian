**O Olho Humano:**
- Estrutura: Córnea, Cristalino, Vítreo, Íris, Esclera, Coróide, Mácula, Retina e Nervo Óptico.
- Converte raios de luz em imagem na retina.
- Ponto Cego: Área sem fotorreceptores.
- Adaptação ao brilho: O olho se ajusta à intensidade da luz.

**A Imagem Digital:**
- Representação: Uma função da intensidade da luz, f(x,y), onde (x,y) são coordenadas espaciais e f é o brilho.
    - f(x,y) = i(x,y) * r(x,y) (i=iluminação, r=reflectância).
- Tipos: Imagens de intensidades (níveis de cinza) e Imagens coloridas (RGB).
- Pixel: Menor unidade de uma imagem digital.
- RGB: Representação de cores com canais Vermelho (R), Verde (G) e Azul (B).
    - 8 bits por canal = 256 níveis de intensidade por cor.
    - 24 bits = 16.777.216 cores.

**Como Câmeras Digitais Funcionam:**
- Processo: Luz é capturada pela lente, focada no sensor de imagem.
- Sensor: "Photosites" medem o brilho.
- Filtro Bayer: Mosaico de filtros (vermelho, verde, azul) para capturar informação de cor. Mais filtros verdes para imagem mais nítida.
- Conversão A/D: Sinal elétrico analógico convertido em dados digitais.
- Processamento Digital de Imagem: Converte dados brutos em imagem colorida.

**Aquisição de Imagens:**
- Processo de conversão de uma cena real tridimensional em imagem analógica.
- Sensores:
    - **CCD (Charge-Coupled Device):** Fotodiodos geram carga elétrica proporcional à luz, que é transferida e amplificada.
    - **CMOS (Complementary Metal-Oxide Semiconductor):** Cada pixel possui seu próprio amplificador e conversor A/D.

**Amostragem e Quantificação:**
- **Amostragem:** Digitalização das coordenadas (posição) da imagem, criando uma matriz de pixels.
    - Valores de (x,y) são discretos (inteiros e positivos).
- **Quantificação:** Digitalização dos valores de intensidade de luz (brilho) de cada pixel.
    - Valores de f(x,y) são discretos (reais e positivos).

**Resolução da Escala de Cinza:**
- Definida pelo número de bits (n) para codificar cada pixel.
- Escala de variação: 0 <= f(x,y) <= W.
- Ex: n=8 bits/pixel = 256 níveis de cinza (0 a 255).

**Resolução Espacial:**
- Expressa em pixels por unidade de medida (ex: PPI - pixels por polegada).
- Maior número de pixels em uma área = maior resolução espacial = mais detalhes.
- Cálculo de Pixels: Tamanho em polegadas * PPI.

**Efeitos da Resolução:**
- **Baixa resolução espacial:** Efeito de pixelização.
- **Baixa resolução de escala de cinza:** Efeito de falsos contornos.

**Armazenamento:**
- Espaço em bytes (1 byte = 8 bits).
- Quantidade de níveis de cinza (L) é geralmente potência de 2.
- Ex: Imagem com L=256 (8 bits/pixel) ocupa 1 byte por pixel.
- Cálculo: (Largura * Altura * Profundidade em bits) / 8.
    - Ex: Imagem de 640x480 com 4 bits de profundidade = 153.600 bytes = 150 KB.