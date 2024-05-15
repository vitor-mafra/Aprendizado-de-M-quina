[[2024-04-01]]

Recapitulação de minimização de erro empírico (e seus problemas). Árvores de decisão e overfitting.

Cada nó da árvore de decisão representa uma pergunta - com suas respectivas decisões de acordo com as respostas. **Encontrar a melhor árvore de decisão é um problema NP-completo!** Entropia: função em termos de uma distribuição entre positivos e negativos -> o quão caótico é o conjunto em termos da distribuição de seus diferentes subconjuntos. A entropia máxima é alcançada com cada um dos subconjuntos com ocorrência de 50% (em um exemplo com dois subconjuntos). Entropia esperada é calculada como a média ponderada da entropia dos subconjuntos resultantes de uma divisão, levando em consideração a proporção de instâncias em cada subconjunto. **Um nó com uma entropia esperada menor é considerado melhor para fazer uma divisão**, pois isso indica que a divisão resultará em subconjuntos mais homogêneos em termos de classes de destino. Para-se quando todas as decisões te levam a grupos puros.

O primeiro atributo escolhido é aquele que leve ao maior ganho de informação.
A entropia caiu com a escolha de um dado atributo -> houve, então, ganho de informação.

Buscar a minimização de erro empírico implica em overfitting. 
Erro empírico não é uma boa aproximação do erro esperado.
Para evitar overfitting não basta minimizar o erro empírico, mas sim, reduzir o erro empírico "sem passar do ponto" -> REGULARIZAÇÃO.

Parada precoce é uma política em árvores de decisão para evitar overfitting. Não aplicamos uma nova pergunta, isto é, um novo nó se este não for gerar um resultado bastante significativo. Esse critério de parada, no entanto, não é capaz de olhar para o futuro - é possível que logo após um early stopping, a nova política fosse aumentar a pureza da separação. 
Outra política possível é post pruning: fazer com que a árvore de decisão tenha overfitting e, a partir dessa árvore viciada busca um ponto anterior em que a separação é melhor feita. Um problema dessa estratégia é que o algoritmo fica extremamente lento.

O que queremos é uma boa acurácia em dados inéditos. Na prática, o que fazemos é separar a amostra em dados de treino e dados de teste. A acurácia de um modelo é medida usando uma função de perda que sumariza o erro produzido pelo modelo. Se avaliarmos o modelo nos dados de treino, temos o erro de treino - ou erro empírico. O erro de teste é normalmente chamado de risco esperado. O risco esperado é uma aproximação do erro esperado. O número de exemplos para o qual o erro empírico e o erro no teste (ou risco esperado) converge é o que chamamos de capacidade do modelo. Com poucos dados de treino, é fácil ter um erro empírico baixo. Se, para esse mesmo modelo, eu aumentar o número de exemplos de treino, o erro empírico tende a subir.

Underfitting -> capacidade baixa
Overfitting -> capacidade alta -> modelos muito complexos com muitos dados

Quando falamos de overfitting não estamos falando apenas de complexidade. Estamos falando também quanto a quantidade de dados de treino. Há uma relação entre a quantidade de dados de treino e sua capacidade.