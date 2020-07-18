### Comparação de modelos e transformação de dados para análise de crédito (Give Me Some Credit Kaggle)

O objetivo deste foi comparar quatro abordagens distintas para modelagem de informações de crédito, considerando bases balanceados, desbalanceadas e preditoras trsnformadas por WOE, bem como em sua escala originais. No processo de modelagem foram utilizados os algoritmos de Random Forest, Redes Neurais, AdaBoost, Gradient Boosting e Regressão Logística, em cada um destes casos foram realizadas permutações nos hiperparâmetros dos modelos(tuning), com o intuito de selecionar o melhor modelo para cada um dos quatro cenários.

A base utilizada no estudo pode ser obtida em Kaggle: https://www.kaggle.com/c/GiveMeSomeCredit

<img align="center" width="600" height="400"  src="https://github.com/WOLFurriell/BehaviorScorePython/blob/master/plots/donut3.png">

Como é possível verificar a distribuição da variável target é relativamente desbalanceada, deste modo, foi realizada um undersampling na base, para balancear a amostra. 
Tal método equaliza a informação desbalanceada diminuindo de forma aleatória o conjunto com a classificação majoritária. Pare este estudo realizou-se um balanceamento 66/33.

<img align="center" width="800" height="350"  src="https://github.com/WOLFurriell/BehaviorScorePython/blob/master/plots/balanc2.png">

No gráfico acima pode-se observar os resultados da variável target para a base balanceada e desbalanceada.

<img align="center" width="800" height="500"  src="https://github.com/WOLFurriell/BehaviorScorePython/blob/master/plots/hist3.png">

Antes de iniciar a modelagem dos dados, foi realizada uma breve análise univariada das variáveis preditoras, tendo por objetivo avaliar a amplitide e a existência de outliers nas informações. Com isto, constatou-se que a variávei RazaoGastos, possuia valores desviantes a partir do percentil 99, desse modo, foi realizada uma substituição das informações acima desta medida pelo próprio P99 e aplicado o logaritmo natural para suavizar a distribuição da informação. 

<img align="center" width="800" height="500"  src="https://github.com/WOLFurriell/BehaviorScorePython/blob/master/plots/Box3.png">

No gráfico acima é possível verificar as preditoras segundo a variável target, em que é possível avaliar que individualmente nota-se disatinções entre as médias das informaões quando verifica-se os indivíduos bons e maus.

<img align="center" width="600" height="400"  src="https://github.com/WOLFurriell/BehaviorScorePython/blob/master/plots/cor1.png">

Para encerrar a parte descritiva, tem-se o gráfico de correlação das preditoras em que não obteve-se valores que repretaram qualquer indicio de multicolinearidades para os modelos de regressão. Ressalta-se que a correlação foi obtida por Pearson para informações contínuas e Spearman para as discretas.

<img align="center" width="800" height="1300"  src="https://github.com/WOLFurriell/BehaviorScorePython/blob/master/plots/WOE2.png">



<img align="center" width="800" height="700"  src="https://github.com/WOLFurriell/BehaviorScorePython/blob/master/plots/ordena.png">

<img align="center" width="800" height="1900"  src="https://github.com/WOLFurriell/BehaviorScorePython/blob/master/plots/ranks.png">

<img align="center" width="800" height="400"  src="https://github.com/WOLFurriell/BehaviorScorePython/blob/master/plots/compara.png">

