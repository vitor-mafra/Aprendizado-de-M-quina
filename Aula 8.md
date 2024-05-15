[[2024-04-10]]

Capacidade de um perceptron é baixa. Ou seja, dificilmente overfita, mas tem grande erro de viés. 

Classificador de regressão logística -> parecido com perceptron mas com a saída dada por uma função sigmoide. Essa conversão de saída acaba reforçando um tom probabilístico pela saída estar entre 0 e 1. A sigmoide transforma uma entrada em probabilidade.

Um perceptron encontra pesos que parecem ser pesos bons.
A regressão logística encontra pesos de forma que a saída reproduzida está próxima da saída esperada.

Um perceptron tende a ser ruim para problemas não-convexos, o que não tende a acontecer com a regressão logística, que lida melhor com esse tipo de problema com vários mínimos locais.

fish-chips-ketchup example.

$$

∇WL=∑[σ(W^TX^i)−y^i]σ′(W^TX^i)X^i   (chainrule)
$$
		            		Erro                     Confiança do modelo

Algoritmo de descida do gradiente:
1) inicializa os pesos (W) aleatoriamente
2) calcula o gradiente da função de perda dados os pesos  ∇W L
$$
3) W←W−r×(∇WL)=∑Error(i)×σ′(WTX(i))×X(i)

$$
4) Repita os passos 2 e 3
You should plot L(W ) after each iteration:

If L(W ) is converging = learning rate is ok  
If L(W ) is diverging = learning rate is too large

If the learning rate is too small = slow to converge

A entrada precisa estar normalizada para que o algoritmo entre em convergência.