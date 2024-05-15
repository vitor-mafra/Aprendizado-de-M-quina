[[2024-04-24]]

Recapitulação de modelos lineares vistos e o problema da seleção de modelos. A metodologia de avaliação de modelos retorna uma previsão para o erro esperado de modo a auxiliar na escolha de decisão de qual modelo usar. Mesmo depois da escolha de um modelo, existem parâmetros e hiper-parâmetros que ainda podem ser escolhidos e ajustados.

Essa metodologia parte do princípio da escolha de complexidade de um modelo a partir da distribuição dos dados. Priorizar a minimização do erro implica, por exemplo, em escolher modelos mais complexos. Usar o erro esperado como estimativa do erro empírico enviesa essa estimativa. Como então encontrar uma estimativa menos enviesada?

1) Separamos o modelo em duas partes: T e V
2) T é usado para treinar o modelo e V é usado para avaliar a perfomance do modelo
3) A estimativa do erro que temos é chamada de erro de validação

 O erro de validação resultante é a melhor estimativa para o erro esperado.

Dilema: queremos um modelo que erre pouco e queremos uma estimativa acurada do erro desse modelo. Aumentar a quantidade de dados de treino, reduz a acurácia do erro de validação e, por sua vez, aumentar a quantidade de dados para validação (em um conjunto de dados finito) reduz a acurácia do modelo, que terá sido treinado em menos dados e estará mais sujeito a variância. Justamente por isso, existem algumas estratégias para fazer essa escolha:
##### Leave-on-out
Para cada treino do modelo, retira um dos dados da amostra para validação. Utiliza n-1 dados para o conjunto T e deixa um dado para V. Repete isso para todos os dados de modo que todos eles sejam utilizados como validação, computando o erro a cada iteração. Problema: mesmo com uma amostra pequena, treinar n modelos para gerar uma estimativa de erro ainda é bastante caro. Em teoria, esta é a melhor solução para estimar o erro - no entanto, seu custo é muito elevado.
##### Validação cruzada
Intercalar os conjuntos de T e V é o que chamamos de *cross validation* . O leave-on-out é uma validação cruzada com o tamanho de V fixo em 1. O erro de validação cruzada não é enviesado para o dado de treino e, com isso, ele consegue gerar uma estimativa bem mais fiel e realista do erro esperado. Para isso, a validação divide a amostra em *k* partições com *n/k* exemplos cada. A divisão mais comum é usar 5 partições nos dados. Isto é o que chamamos de *k-fold cross validation*. Existem alguns estudos mostrando que para *k<=10* tende a ser o ideal para particionar os dados. 
