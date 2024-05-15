[[2024-03-11]]

Definição de aprendizado: Aprendizado é uma adaptação causada pelo acúmulo de experiência
- Quase todos os seres vivos com sistema nervoso central são capazes de aprender (até mesmo os mais simples!)

Perguntas centrais em aprendizagem de máquina:
1)  O que significa uma máquina aprender?
2)  Por quê é importante que uma máquina aprenda?
3) Como fazer isso?

Na prática, escrevemos programas parametrizados e deixamos a máquina encontrar a melhor configuração de parâmetros de modo a otimizar o comportamento esperado. Fazemos isso apresentando exemplos de entrada e saída de modo a melhorar essa otimização de escolha dos parâmetros. Por isso falamos em aprender: estamos aprendendo com exemplos que já aconteceram para prever comportamentos que ainda vão acontecer.

"A computer program is said to learn **from experience E with respect to some class of tasks T and performance measure P, if its performance at tasks in T, as measured by P, improves with experience E**" - Tom Mitchell, 1997

Como vários problemas são muito difíceis de escrever proceduralmente um passo-a-passo que ensine a máquina a realizar uma dada tarefa, a abordagem que tomamos aqui é fornecer à máquina exemplos, isto é, conjuntos de entradas e saídas já conhecidos. O programa, então, aprende à partir desses casos e consegue generalizar para novas entradas suas previsões de saídas.

Motivos do sucesso recente de aprendizado de máquina:
1) Acesso a computação mais amplo
2) Aquisição de dados muito ampliada <- extremamente importante
3) Avanço dos algoritmos de machine learning

Diferentes tipos de aprendizado de máquina:
- **Aprendizado supervisionado**: dado um conjunto de dados de exemplo com entradas e saídas, produz uma predição para um novo dado.
- **Aprendizado por reforço**: baseado em recompensas e agentes. Entrega uma estratégia, e não uma predição. Um conjunto de passos no tempo que otimiza caminhos futuros, não coisas que já aconteceram.
- **Aprendizado não-supervisionado**: dado um conjunto da dados não rotulados, encontra padrões que agrupa os dados em subconjuntos.

Tipos de aprendizado supervisionado
- Regressão
	 Tenta encontrar uma função que estima uma saída, dada uma entrada.
- Classificação
	 Tenta encontrar uma função para separar conjuntos de dados, de modo a agrupar populações diferentes em um dado grupo.

Tipos de aprendizado não-supervisionado
- Agrupamento/Clusterização
- Embedding/n-fold


**Pontuação**
2 provas de 20 pontos cada
- primeira prova no meio do semestre (até aprendizado estatístico)
- segunda prova no fim do semestre (com conteúdo de deep learning também)

2 trabalhos práticos de 10 pontos cada
- primeiro tp próximo a prova 1, com um mês de tempo de entrega
- segundo tp logo depois do tp1

1 projeto de 40 pontos
- sem especificação, aberto a qualquer problema que possa ser resolvido no tempo do semestre. Sem entrega intermediária, apenas o resultado final e um vídeo de 5 minutos