Etapas para o treinamento de uma rede neural artificial:
- Coleta de Dados: Montagem da base de dados baseado no experimento escolhido.
- Tratamento de Dados:
	- Verficação de integriade: remoção de dados problematicos/faltantes e interpolação (criação de dados artificiais utilizando técnicas especificas).
	- Indentificação de pontos atípicos(outlier): algum(ns) possível(is) dado(s) coletado(s) de forma errada ou com problema, que distorce os dados da amostra. Intervalo Entre Quartis (IQR) é a técnica utilizada para remover esses pontos atípicos, depois usado a interpolação para "cobrir" o espaço gerado.
	- Scaler (colocar em escala): Colocar os dados em uma escala de 0 à 1. Transforma todos os valores do conjunto de dados para dentro da escala.
	Formula da escala:$$
\frac{Xi - Xmin}{Xmax - Xmin}
$$
- Divisão de conjuntos: com 60% do conjunto de amostras são entregues ao modelo para ele inferir o plano de separação (dados de treino), outros 30% são usados para validação do treinamento da rede (dados de validação), os 10% restantes são usados para teste do modelo (dados de teste cego).
- Dataset de treino: 60% do conjunto de dados tratado.
- Mix: Mistura de todos os dados do conjuto de forma aleatoria.
- Treinamento: Entraga de valores presentes no conjunto de dados para o modelo, onde o resultado gerado pela rede são comparados com o resultado real, se ocorrer erros de resultados eles sao armazenados e somados. Passa os dados, soma os erros, devolve o erro pra rede, ela recalcula os pesos, e continua até o final das épocas.
Formula dos erros:
$$
\frac{\sqrt{ \sum_{}{E²} }}{n}
$$
**O neurônio**

![[neuronio.png]]

Formula:
$$
u = \sum_{i=1}{Wi \cdot Xi - \Theta}
$$
$$
y = g(u)
$$
Legenda:
- Xi = Sinais de entrada (valores do dataset)
- Wi = Peso (vetor de pesos)
- θ = Bias
- g(x) = Função de ativação
- u = Saída da rede

**A rede sempre atualiza somente os pesos!!!**

## Funções de ativação

### Parcialmente diferenciaveis:
Possuem pontos onde as derivadas se primeira ordem não existem.
- Degrau
- Degrau bipolar
- Rampa simétrica
- ReLU (Rectified Linear Uniti)

### Totalmente diferenciáveis:
Derivadas conhecidas em todos os pontos da função.
- Sigmoides
	- Logística
	- Tangente hiperbólica
- Gaussiana


