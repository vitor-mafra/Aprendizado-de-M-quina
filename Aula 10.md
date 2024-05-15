[[2024-04-17]]

Support Vector Machine - traz uma regularização muito melhor que as outras técnicas existentes anteriormente. Tem a capacidade de um modelo linear - justamente porque ele também é um.

Introdução ao conceito de margem para tentar determinar qual separação feita por um perceptron é a melhor. Ter uma margem maior é melhor. Uma intuição que ajuda a entender isso é que com a introdução de variância nos dados um separador com margem maior tende a ter um erro empírico menor. Um perceptron de margem máxima é a melhor separação linear em dados linearmente separáveis. Um separador mais robusto a variância - e, portanto, erro de overfitting - é também o separador com margem máxima.

Os pontos dos dados que são responsáveis por definir a margem máxima são os pontos que vão criar o vetor de suporte - o SVM só precisa desses dados! 

#### Despedaçar e Dimensão VC

A separabilidade dos dados aumenta com o aumento do número de dimensões. Isso aumenta também as dimensões de separação - no entanto também aumenta a complexidade dela. Em 2 dimensões, um perceptron é capaz de despedaçar apenas 3 pontos. Em 3 dimensões, o perceptron é capaz de despedaçar até 4 pontos - mas não 5. É possível despedaçar tantos pontos quanto for a dimensão - 1.

**A margem depende da escala dos pontos**. A menor esfera n-dimensional que engloba todos os dados determina o mundo em que os dados estão. A margem relativa é o tamanho da margem dividido pelo tamanho da esfera que engloba todos os dados.

**A dimensão VC de um separador h é limitada pelo mínimo da dimensão do dado e o teto do   quadrado do inverso da margem relativa.**

Com um separador de margem suficientemente grande a dimensionalidade do dado não importa!

#### O algoritmo do SVM

É preciso separar os dados com uma linha. Mas qual? Queremos buscar um separador que maximiza a margem.

Suponha que existe um vetor (dado pelos pesos do SVM), que sai da origem e tem uma direção perpendicular a um certo separador.

**O SVM enxerga os dados como restrições!**

