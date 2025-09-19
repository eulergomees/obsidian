Etapas para o treinamento de uma rede neural artificial:
- Coleta de Dados: Montagem da base de dados baseado no experimento escolhido.
- Tratamento de Dados:
	- Verficação de integriade: remoção de dados problematicos/faltantes e interpolação (criação de dados artificiais utilizando técnicas especificas).
	- Indentificação de pontos atípicos(outlier): algum(ns) possível(is) dado(s) coletado(s) de forma errada ou com problema, que distorce os dados da amostra. Intervalo Entre Quartis (IQR) é a técnica utilizada para remover esses pontos atípicos, depois usado a interpolação para "cobrir" o espaço gerado.
	- Scaler (colocar em escala): Colocar os dados em uma escala de 0 à 1. Transforma todos os valores do conjunto de dados para dentro da escala.
		$$
\frac{Xi - Xmin}{Xmax - Xmin}
$$
