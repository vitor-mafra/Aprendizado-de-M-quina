[[2024-04-08]]

Uma árvore é capaz de encontrar uma aproximação para qualquer tipos de função - desde que existam dados de qualidade em abundância. É uma aproximadora universal, diferentemente de um Perceptron, por exemplo, que só consegue aproximar retas.

#### Distinção do Erro
##### Viés
É um erro que acontece quando seu algoritmo não é capaz de produzir um modelo com a capacidade que deveria ter. O modelo que gera a função de aproximação não tem capacidade. Ex: perceptron só é capaz de gerar modelos lineares - portanto não é capaz de aproximar curvas, por exemplo.
##### Variância
É uma propriedade que depende do dado. Acontece quando seu modelo funciona bem nos dados de treino, mas falha com os dados de teste. Há uma relação entre complexidade e variância.

Quando diminuímos o erro de viés, aumentamos o erro de variância - e vice-versa. Existe uma forte relação entre os dois, justamente na complexidade do modelo. Um modelo mais complexo tende a ter pouco erro de viés, no entanto, tende a ter maiores erros de variância. Essa relação inversa tem um lugar ótimo, que minimiza esses dois erros (note que encontrar isso de forma objetiva, na prática, é impossível).

#### Regularização
Minimizar o erro de treino -> reduzir o viés (desde que isso signifique ter uma boa aproximação do erro de teste/erro esperado, isto é, errar pouco devido a variância). Modelos simples, que cometem muito erro devido a viés, conseguem dar uma boa aproximação do erro de teste. Modelos complexos oferecem um erro empírico baixo, mas a aproximação do erro de teste não é boa.

##### Navalha de Occam
Entre duas opções igualmente boas, fique com a mais simples.

Se a capacidade de um modelo é fixa, quanto maior for o treino, m
Mantendo um modelo fixo, a medida que se aumenta a quantidade de dados de treino, o erro esperado tende a cair.

Com dados suficientes, uma árvore de decisão tem erro empírico zero.

Regularização é aplicada para todos os algoritmos de aprendizado de máquina. Ela minimiza uma função de perda (erro empírico) ao mesmo tempo que penaliza modelos complexos.

Quanto maior for o tamanho da sua amostra, mais complexo seu modelo pode ser.

#### Princípios de indução:
1) Minimização de erro empírico
2) Minimização de risco estrutural: minimizar o erro empírico com uma regularização -> minimizar a complexidade de um modelo