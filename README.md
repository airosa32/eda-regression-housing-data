# Data Science - Case 03

# Análise Exploratória e Modelagem de Regressão Linear para Preços de Imóveis
## 1. Introdução aos Dados
O dataset utilizado é um conjunto de dados de imóveis dos Estados Unidos, com 5000 registros e 7 colunas, incluindo características como a renda média da área, idade média das casas, número médio de quartos e quartos, população da área, e o preço das propriedades. A coluna de endereços foi removida, pois não é uma variável numérica relevante para a modelagem de regressão linear.

## 2. Análise Estatística Básica
Para entender melhor os dados, foram realizadas análises descritivas básicas:
- Distribuição das Variáveis: Utilizamos o método .describe() do pandas para obter estatísticas resumidas, como a média, desvio padrão, valores mínimo e máximo. Por exemplo, o preço médio das propriedades é aproximadamente 1.232.073 dólares, com um desvio padrão de 353.117 dólares, indicando uma variação considerável nos preços.
- Visualizações Iniciais: Foram criados gráficos de caixa (box plots) para as variáveis "Avg. Area Income" e "Price" para observar a distribuição e identificar possíveis outliers. A renda média da área e o preço das propriedades foram analisados para entender sua dispersão.

## 3. Preparação dos Dados
- Renomeação de Colunas: As colunas foram renomeadas para substituir espaços por sublinhados e remover pontos, a fim de facilitar a manipulação dos dados.
- Remoção de Colunas Irrelevantes: A coluna "Address" foi removida, pois não é uma variável numérica que contribui para a modelagem de regressão.

## 4. Análise de Correlação
- Correlação entre Variáveis: Calculou-se a correlação entre as variáveis usando o método .corr() do pandas e visualizou-se a matriz de correlação com um heatmap. Observou-se que a variável "Avg. Area Income" tem uma correlação positiva significativa com o preço das propriedades (0.6397), indicando que uma maior renda média na área está associada a preços mais altos.

## 5. Visualização dos Dados
- Pair Plots: Foram utilizados gráficos de dispersão (pair plots) para examinar a relação entre as variáveis explicativas e o preço. Esses gráficos ajudam a visualizar a linearidade e a relação entre as variáveis.
- Distribuição dos Preços: Um histograma foi gerado para mostrar a distribuição dos preços das propriedades, evidenciando que a maioria dos preços se concentra em torno da média.

## 6. Modelagem de Regressão Linear
- Preparação dos Dados para Modelagem: Os dados foram divididos em conjuntos de treino e teste, com 70% dos dados usados para treinamento e 30% para teste.
- Treinamento do Modelo: Foi treinado um modelo de regressão linear usando o conjunto de treinamento. O modelo ajusta a relação linear entre as variáveis explicativas e o preço das propriedades.
- Avaliação do Modelo: A performance do modelo foi avaliada usando o coeficiente de determinação **R²**, que mede a proporção da variabilidade dos preços explicada pelas variáveis independentes. O valor **R²** obtido foi aproximadamente 0.915, indicando que o modelo explica 91.5% da variabilidade nos preços, o que é um excelente resultado.

## 7. Comparação dos Resultados Reais e Previstas
- Visualização dos Resultados: Foi criado um gráfico para comparar os preços reais das propriedades com os preços previstos pelo modelo. A comparação revelou uma boa correspondência entre os valores reais e previstos, confirmando a eficácia do modelo.

## 8. Conclusão
A análise e modelagem indicam que o modelo de regressão linear é eficaz para prever os preços das propriedades com base nas variáveis explicativas selecionadas. O elevado valor do **R²** sugere que as variáveis independentes escolhidas têm um impacto significativo sobre o preço das propriedades, e o modelo fornece previsões robustas.
