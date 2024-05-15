[[2024-03-13]]

Conjunto de treino é pressuposto em aprendizado supervisionado. O conjunto de treino é um *set* que combina entradas e saídas-alvo. As saídas não precisam necessariamente ser binárias, mas, normalmente, por conveniência e simplificação, tomaremos aqui as possíveis saídas *y* como binárias. O vetor de entradas, por sua vez, pode ser n-dimensional a depender da modelagem das *features* contidas em *X*. A escolha das features de *X* é crucial para a boa solução de um problema. O objetivo é determinar uma função - que chamaremos aqui de modelo (seja ela estimadora ou separadora) - de forma a modelar o problema para predizer corretamente as saídas *y* em novos valores possíveis de vetores *X*.

Esse procedimento geralmente é dividido em duas etapas bem estabelecidas:
1) Escolher um algoritmo (difícil!)
	Depende muito da experiência e não existe uma metodologia bem definida, muito menos um algoritmo que seja uma bala de prata
2) Otimizar parâmetros (geralmente é mais fácil que o primeiro passo)
	 No geral, consiste em minimizar a função de perda. É como sintonizar um rádio: após descobrir um caminho, basta refinar as escolhas de modo a minimizar o erro e aumentar o sinal em relação ao ruído.
	 **previsão - verdade == erro**

---
#### Aprendizado Neural (*Deep Learning*) *vs* Aprendizado Estatístico (*Machine Learning*)

Aprendizado Neural:
- Busca-se muito inspiração no funcionamento do sistema nervoso
- Normalmente os algoritmos são criados através da inspiração para depois a teoria surgir explicando o que acontece ali
- Ex: *perceptron*/*covnets*

Aprendizado Estatístico:
- Baseado na modelagem estatística
- Geralmente a teoria precede o algoritmo
- Ex: SVM e árvore de decisão

--- 
Aprendizado não é memorização! Memorização é importante, mas o que buscamos quando falamos em aprendizado de máquina é **generalização**. Queremos sair de exemplos já conhecidos e conseguir encontrar respostas para novas entradas antes desconhecidas. O problema é que fazer essa generalização costuma ser bastante difícil: como conseguir uma boa generalização a partir de um número limitado de exemplos? 

https://pt.wikipedia.org/wiki/Navalha_de_Ockham

Como encontrar a função-alvo?
- Ela é desconhecida, apesar de que possamos assumir que ela existe
- Pode ser muito complexa
Provavelmente não econtraremos a função-alvo *f*, mas podemos encontrar uma outra função *g* que aproxime bem a função-alvo. O problema é justamente esse: queremos aproximar uma função de uma função-alvo desconhecida - tendo apenas uma amostra pequena do fenômeno em mãos.

Os algoritmos se diferem no conjunto de funções *g* que eles podem criar. Alguns podem produzir qualquer coisa, outros podem produzir apenas funções lineares, por exemplo.

O treino normalmente é uma pequena amostra do fenômeno em questão. Não se pode ver *f*, mas podemos enxergar essa pequena amostra de exemplos que pertencem a *f* - uma pequena dica.

--- 
#### Perceptron

Baseado em um neurônio - consiste em múltiplos *inputs* e um único *output*. Cada *input* tem um peso *w* que multiplica o valor do *input*. O neurônio, então, combina esses pesos aos *inputs* de modo a determinar um *output* de acordo com uma função de ativação. Os dendritos de um neurônio, nesse caso, são analogias para os pesos *w* para cada um dos atributos. 