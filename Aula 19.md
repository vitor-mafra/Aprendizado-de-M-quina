[[2024-06-10]]

### Aprendizado não supervisionado

Aprendizado supervisionado foi anteriormente definido como um problema de aproximador de uma função. No aprendizado supervisionado, tratamos de problemas bem definidos, com erros conhecidos e facilmente calculáveis.

Aprendizado não supervisionado contém problemas menos bem estabelecidos que os problemas do aprendizado supervisionado. Descrever um dado é uma tarefa muito mais subjetiva do que uma mera aproximação de função. Aqui, trataremos de problemas com dados que possuem apenas uma entrada (sem uma saída que vamos usar para treinar o modelo). Portanto, o que buscaremos aqui é encontrar padrões nos dados de modo a conseguir criar um modelo que o descreva bem. Por conta de tudo isso, falamos também de problemas que vão lidar com quantidades muito maiores de dados para encontrar os padrões nesses problemas. 

Aprendizado não supervisionado e agrupamentos não são sinônimos. No entanto, os exemplos mais comuns de aprendizado não supervisionado normalmente envolvem agrupamentos (*clustering*). 

#### *Hierarchical agglomerative clustering*:
Define a distance function between clusters. 
- Initialize:
	Every example is a cluster. 
- Iterate:
	Compute distance between all pairs of clusters. Merge the two closest clusters.
This forms a [dendogram](https://en.wikipedia.org/wiki/Dendrogram).

Uma vez formado o dendograma, diferentes agrupamentos podem ser configurados facilmente a partir dessa estrutura.

Diferentes algoritmos para calcular as distâncias no agrupamento levam a resultados completamente diferentes. Existem, portanto, medidas de distâncias que são boas para determinados tipos de problemas (ou resultados buscados). 

#### *K-Means*
Iterate between:  
- Updating the assignment of points to clusters.
- Updating the clusters.
Assume k clusters.

Sempre vai convergir para uma solução única (para um dado *k*) já que quando os centróides pararem de se mover, os dados não vão mudar de grupos e o resultado estará dado. Se o *k* for muito pequeno, qualquer ponto será colocado num mesmo grupo. Já se *k* for muito grande, qualquer ponto será um grupo. A questão crítica aqui é, portanto, escolher bem o valor de *k*. Uma solução é penalizar pela complexidade:
More clusters increase the loss, if they do not help ”enough” 
*Bayesian Information Criterion:*

$C=log(1/n×d ∑||xi−μi||^2)+ k × log n/n$

Normalmente *k-means* é um modelo testado inicialmente para qualquer problema de agrupamento - apesar de enfrentar um problema com quantidades massivas de dados, já que todas as distâncias precisam ser calculadas.