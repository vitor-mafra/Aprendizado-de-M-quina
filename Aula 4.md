[[2024-03-20]]

épsilon -> tolerância ao erro 
ni -> frequência de erro

https://en.wikipedia.org/wiki/Hoeffding%27s_inequality
https://en.wikipedia.org/wiki/Chernoff_bound

P.A.C. -> pesquisar mais sobre

Uma tolerância baixa ao erro implica que para evitar um evento ruim é necessário garantir uma amostra maior. Portanto, com uma quantidade pequena de amostra de treino, o erro esperado aumenta. Um n pequeno implica em um epsilon grande. Certas deficiências nos dados implicam em resultados ruins - mesmo com técnicas e algoritmos avançados em aprendizado de máquina. 

Não é possível garantir *ni* baixo sem saber o quão boa é a sua função preditora comparada a função real. Apenas por meio de comparações é possível dizer que sua função preditora é provavelmente boa - ou o contrário.

*ni* -> error in sample 

Se o erro na amostra é baixo, não é possível garantir que a função *h* é boa - mas um erro na amostra baixo permite essa possibilidade. Um erro na amostra alto, por sua vez, a função *h* provavelmente é ruim.

mi -> erro fora da amostra, erro esperado

*mi* não pode ser calculado, mas se ele for dado e for baixo, *h* é com certeza uma ótima função preditora.

M se refere a quantidade de funções preditoras testadas ao longo do treinamento. Essa busca não é feita aleatoriamente, afinal, todo processo de otimização implica em melhorar a qualidade de *h* ao longo das iterações - M. Se você precisa de muitas iterações para buscar essa melhoria, isso provavelmente não é um bom sinal (***overfitting***).