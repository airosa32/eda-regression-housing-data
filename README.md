# 🏠 Análise Exploratória e Regressão Linear em Dados Imobiliários

## 📂 Introdução aos Dados  
O dataset utilizado é um conjunto de dados de imóveis dos Estados Unidos, com 5.000 registros e 7 colunas, incluindo características como a renda média da área, idade média das casas, número médio de quartos e banheiros, população da área e o preço das propriedades. A coluna de endereços foi removida, pois não é uma variável numérica relevante para a modelagem de regressão linear.

## 📊 Análise Estatística Básica  
Para entender melhor os dados, foram realizadas análises descritivas básicas:

- **📌 Distribuição das Variáveis**: Utilizou-se o método `.describe()` do Pandas para obter estatísticas como média, desvio padrão, valores mínimo e máximo. Por exemplo, o preço médio das propriedades é aproximadamente **1.232.073 dólares**, com desvio padrão de **353.117 dólares**, indicando variação considerável.
- **📈 Visualizações Iniciais**: Gráficos de caixa (box plots) foram gerados para as variáveis **Avg. Area Income** e **Price**, com o objetivo de observar a dispersão e identificar possíveis outliers.

## 🧹 Preparação dos Dados  
- **📝 Renomeação de Colunas**: Foram substituídos espaços por sublinhados e removidos pontos dos nomes das colunas para facilitar a manipulação.
- **🗑️ Remoção de Colunas Irrelevantes**: A coluna "Address" foi removida, pois não agrega valor à análise preditiva.

## 🔗 Análise de Correlação  
- **📉 Correlação entre Variáveis**: A matriz de correlação, gerada com o método `.corr()` do Pandas e visualizada com um heatmap, indicou que a variável **Avg. Area Income** tem uma correlação positiva significativa com o preço das propriedades (**0.6397**), sugerindo que uma maior renda média na área está associada a preços mais altos.

## 📌 Visualização dos Dados  
- **🔍 Pair Plots**: Gráficos de dispersão (pair plots) foram usados para examinar a relação entre as variáveis independentes e o preço.
- **💰 Distribuição dos Preços**: Um histograma foi criado para mostrar a distribuição dos preços, com a maioria concentrada ao redor da média.

## 🧠 Modelagem de Regressão Linear  
- **📤 Preparação para Modelagem**: Os dados foram divididos em conjuntos de treino (70%) e teste (30%).
- **⚙️ Treinamento do Modelo**: Foi treinado um modelo de **regressão linear**, que ajusta uma relação entre as variáveis explicativas e o preço.
- **📏 Avaliação**: A performance foi medida pelo coeficiente de determinação **R²**, com valor aproximado de **0.915**, indicando que o modelo explica **91,5% da variabilidade** nos preços — um excelente resultado.

## 🔍 Comparação dos Resultados Reais e Previstas  
- Foi criado um gráfico para comparar os preços reais das propriedades com os preços previstos. A boa correspondência entre ambos valida a eficácia do modelo de regressão.

## ✅ Conclusão  
A análise e modelagem confirmam que a regressão linear é uma técnica eficaz para prever os preços de propriedades residenciais com base em variáveis como renda média da área, número de quartos e idade das casas. O valor elevado de **R²** destaca o bom desempenho do modelo e sua aplicabilidade em análises preditivas do mercado imobiliário.
