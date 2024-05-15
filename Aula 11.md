[[2024-04-22]]

Recapitulação de SVM. Sabendo qual é o vetor suporte é possível determinar qual é o hiperplano que separa linearmente os dados. 

Como maximizar a margem?
- maximizar 1/norma de w
- minimizar a norma de w

O regularizador de uma rede neural com camadas ocultas é a norma dos pesos.

SVM, assim como perceptron, tem a premissa de que o dado é linearmente separável - o que é uma premissa ruim, já que os dados no mundo real dificilmente são assim (e, se são, o problema que eles representam não é interessante). SVM busca sempre a maior margem possível, coisa que pode não ser o ideal para algumas distribuições de dados no mundo real, já que aumentar a margem pode implicar em aumentar também o erro empírico. 

#### SVM aproximado ou regularizável
Uma das técnicas que usamos para contornar isso é punir a complexidade e o erro empírico para buscar esse melhor balanço. A "margem suave" (*soft margin*) introduz o conceito de "variáveis de folga" (*slack variables*). A margem suave permite que algumas das amostras de treinamento sejam classificadas incorretamente ou estejam dentro da margem de decisão, em vez de exigir que todas as amostras de treinamento sejam corretamente classificadas e fora da margem. Isso é útil para este caso em que os dados não são linearmente separáveis, permitindo uma certa quantidade de erro para melhor generalização do modelo.

#### Kernels
No entanto, existem padrões de dados que não são linearmente separáveis e que a punição dessas complexidades não faz nenhum sentido. Nesse caso, podemos aumentar a dimensionalidade dos dados de modo a criar um novo espaço em que os dados possam ser linearmente separáveis. Esse processo é chamado de Kernel - existe uma função que faz isso e essa função possui algumas propriedades. Quanto mais dimensões você aumenta, mais fácil é a encontrar uma separação linear dos dados - no entanto, isso implica em encontrar uma separação muito mais complexa quando traduzido de volta à dimensão original.

Hot take da aula: Tudo o que é simples em uma dimensão é mais complexo ao ser reduzido para uma dimensão menor