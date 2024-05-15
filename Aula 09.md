[[2024-04-15]]

Recapitulação das capacidades de um neurônio: não é possível resolver problemas não-lineares.

Uma rede com muitas camadas é capaz de linearizar os dados de modo a tirar a influência dessa limitação inerente ao perceptron

dimensão extra no índice 0 sempre ligada a 1? -> relembrar isso

As redes neurais combinam perceptrons de modo a aumentar a capacidade do modelo e permitir mais soluções, o que diminui também o overfitting.

#### Backpropagation
Perturbar os pesos sem uma estratégia bem definida obviamente não é uma boa estratégia para determinar bons pesos para uma rede. O algoritmo que melhora a definição dos pesos de uma rede neural é conhecido como backpropagation. A etapa foward estima de acordo com a entrada X, a saída Y. Na etapa backwards, a rede neural corrige os pesos de acordo com a saída Y prevista. A rede neural prevê para depois corrigir para calcular o erro de modo a permitir melhores ajustes dos pesos. Note que a cada iteração o erro é calculado e os pesos são atualizados.

Algoritmo:
`Randomly initialize the weights`    
`For each example (x(i), y(i))`
	`Calculate the error (forward pass)` 
	`Calculate local gradients for each node` 
	`Update the weights (backward pass)`

O gradiente é a derivada da sigmoide (função de ativação) multiplicado pelo peso.

Momentum é uma heurística utilizada na atualização dos pesos para sair facilmente de mínimos locais - ou seja, em mínimos locais complexos, o momentum ajuda menos a superação do gradiente nesses pontos.

Problemas: diminishing gradient -> pesos na parte baixa da rede tendem a ser aleatórios.