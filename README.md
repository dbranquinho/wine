## Prefácio

Há duas estratégias principais nesse trabalho, uma está no nodebook [LopesBin.ipynb](https://github.com/dbranquinho/wine/blob/master/LopesBin.ipynb) o outro [lopes.ipynb](https://github.com/dbranquinho/wine/blob/master/lopes.ipynb)

## Introdução
O presente problema se refere aos dados de vinhos portugueses "Vinho Verde", que possuem variantes de vinho branco e tinto. Devido a questões de privacidade, apenas variáveis físico-químicas (input) e sensoriais (output) estão disponíveis (por exemplo, não há dados sobre tipo de uva, marca do vinho, preço de venda, etc).

### Objetivo

Criar um modelo para estimar a qualidade do vinho.

## Questões a serem respondidas

a. Como foi a definição da sua estratégia de modelagem?
* R: Foram usadas duas estratégias básicas para a modelagem, todas usando as distribuições de Poisson e Bernoulli, discreta com várias classes e Binomial com apenas duas classes (boa ou ruim) respectivamente.   
1. AutoML: Automatic Machine Learning
2. DRF (incluindo os modelos Random Forest e Extremely Randomized Trees (XRT)
3. GLM - Generalized linear model
4. XGBoost (XGBoost GBM)
5. SVM - um classificador linear binário não probabilístico
 

b. Como foi definida a função de custo utilizada?
* R: De uma forma geral, a escolha da função de custo depende se o problema. Usamos algumas para o modelo multiclasses:
1. Erro quadrático médio (Mean squared error – MSE)
2. Erro Quadrático Médio (RMSE)
3. AUC - area under the curve (ROC)
4. Acurácia = Taxa de acertos

* Para o modelo binomial:
1. Acurácia
2. F1 - Essa métrica combina precisão e recall de modo a trazer um número único que indique a qualidade geral do seu modelo e trabalha bem até com conjuntos de dados que possuem classes desproporcionais.
3. AUCPR - Para um alvo binário desequilibrado, recomendamos AUCPR em detrimento de AUC

c. Qual foi o critério utilizado na seleção do modelo final?
* R: As metricas apresentadas acima

d. Qual foi o critério utilizado para validação do modelo? Por que escolheu utilizar este método?
* R: Alguns métodos foram usados:
1. Validação cruzada usando k-fold com k=3, usamos k=5, mas o número de observações é pequeno para um k maior do que 3.
2. Dividindo o dataset em treino, validação e teste, o segundo para o modelo validar e entregar as métricas de desempenho do modelo, o último, teste, para evitar o overfiting, testando novamente o desempenho.

e. Quais evidências você possui de que seu modelo é suficientemente bom?
* R: Vários modelos sendo comparados entre sí com várias técnicas e métricas com relatório final.
