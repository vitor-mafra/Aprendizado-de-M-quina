[[2024-05-15]]

#### Naive Bayes

Faz parte de uma classe de algoritmos chamada de não-paramétrica. Perceptron, SVM, MLP: todos são algoritmos paramétricos que dependem da alteração de pesos para aprender. Naive Bayes aprende através do dado, mas não faz isso através de parâmetros. Apesar de árvores de decisão não tenha pesos, ela é materializada com uma forma determinada - mas também faz parte da classe de algoritmos não paramétricos.

Naive Bayes consiste em duas principais etapas:
1) Estimar uma distribuição
2) Inferência

##### A parte Bayes
Naive Bayes baseia-se no Teorema de Bayes, que fornece uma maneira de atualizar as probabilidades de uma hipótese à medida que novas evidências são apresentadas. O teorema é expresso pela seguinte fórmula:

𝑃(𝑦∣𝑋)=𝑃(𝑋∣𝑦)⋅𝑃(𝑦)𝑃(𝑋)P(y∣X)=P(X)P(X∣y)⋅P(y)​

Onde:

- 𝑃(𝑦∣𝑋)P(y∣X) é a probabilidade posterior da classe 𝑦y dado o vetor de features 𝑋X.
- 𝑃(𝑋∣𝑦)P(X∣y) é a probabilidade de observar o vetor de features 𝑋X dado que a classe é 𝑦y.
- 𝑃(𝑦)P(y) é a probabilidade prévia da classe 𝑦y.
- 𝑃(𝑋)P(X) é a probabilidade de observar o vetor de features 𝑋X.

##### A parte Naive

Assumiremos aqui a independência condicional - isto é, que fixando um y, teríamos independência das features (todo o vetor X). Isso facilita bastante os cálculos do cálculo das probabilidades para estimar uma hipótese. As features, neste caso, seriam, então, independentes entre si: teriam apenas uma relação com y.

p(xi | y, xj) = p(xi | y)
p(xi | y, xj, xk) = p(xi | y) 
p(xi | y, xj, xk, xl) = p(xi | y)

Essa suposição de independência é o que torna o algoritmo "ingênuo" (naive). Embora na prática as features muitas vezes não sejam completamente independentes, o Naive Bayes pode ainda assim ter um desempenho surpreendentemente bom em muitos problemas de classificação devido à sua simplicidade e eficiência computacional.

--- 

Naive Bayes é interessante quando queremos um modelo que seja muito rápido - seja por limitação de tempo ou de poder computacional. Além disso, esse algoritmo se comporta bem mesmo com pouquíssimos dados. Geralmente não se fala de *overfitting* quando o assunto é Naive Bayes.

Naive Bayes não é, de fato, um algoritmo lazy. O termo "lazy" refere-se a um tipo específico de algoritmo de aprendizado, conhecido como "lazy learning" ou "aprendizado preguiçoso", onde a generalização do modelo é adiada até que uma nova amostra precise ser classificada. Exemplos típicos de algoritmos lazy são o k-NN (k-Nearest Neighbors), que não constroem um modelo explícito durante a fase de treinamento, mas simplesmente armazenam os dados de treinamento e realizam a generalização na hora da classificação. Naive Bayes, por outro lado, é considerado um algoritmo "eager" ou "aprendizado ansioso". Isso significa que ele constrói um modelo de classificação durante a fase de treinamento, antes de receber novos dados para serem classificados.