[[2024-05-22]]

### Boosting
A ideia por trás do Boosting é combinar vários modelos simples (ou fracos) de modo a criar um modelo forte. Essa ideia se mostrou muito potente ao longo da história de aprendizado de máquina e é uma das ferramentas mais usadas em modelos atualmente. O princípio por trás disso tudo é evitar o overfitting. 

Um modelo fraco é um modelo que tem um desempenho ligeiramente melhor que o acaso - ou seja, um modelo que tenha precisão melhor que 50% em tarefas de classificação binária, por exemplo. Note que esses modelos tendem a ser simples, rápidos e menos propensos ao *overfitting* (isso será muito importante para o resultado final que estamos buscando com o *Boosting*).

O objetivo final, em Boosting, é descorrelacionar o erro.

#### AdaBoost
O AdaBoost, que significa Adaptive Boosting, é um dos algoritmos de boosting mais conhecidos e amplamente utilizados em machine learning. Foi introduzido por Yoav Freund e Robert Schapire em 1996. A principal ideia por trás do AdaBoost é melhorar a precisão dos modelos fracos (*weak learners*) combinando-os em uma sequência adaptativa de modelos, onde cada modelo é treinado para corrigir os erros cometidos pelos modelos anteriores.

##### Funcionamento Básico do AdaBoost

1. **Inicialização**:
   - Começa com a atribuição de pesos iguais a todas as observações do conjunto de treinamento. Se houver \( N \) observações, cada uma recebe um peso $$( w_i = \frac{1}{N}\)$$
2. **Treinamento Iterativo**:
   - Em cada iteração \( t \):
     - Um modelo fraco \( h_t(x) \) é treinado usando o conjunto de treinamento ponderado.
     - O erro do modelo \( h_t \) é calculado em relação aos pesos das observações.
     - A partir do erro, calcula-se a importância do modelo \( \alpha_t \), que mede o quanto o modelo merece ser considerado na combinação final.
     - Os pesos das observações são então atualizados: as observações classificadas incorretamente pelo modelo recebem mais peso, enquanto as observações classificadas corretamente têm seu peso reduzido. Isso faz com que os próximos modelos foquem nas observações mais difíceis.

3. **Combinação dos Modelos**:
   - Os modelos fracos são combinados para formar uma forte predição final. A predição combinada é uma média ponderada das predições dos modelos fracos, ponderada pela importância \( \alpha_t \) de cada modelo.

##### Fórmulas Chave

- **Erro do modelo (h_t)**:

$$
  \epsilon_t = \sum_{i=1}^{N} w_i \cdot I(y_i \neq h_t(x_i))
  
$$
  onde \( I \) é uma função indicadora que é 1 se a predição estiver errada e 0 se estiver correta.

- **Importância do modelo \( \alpha_t \)**:
  
$$
  \alpha_t = \frac{1}{2} \ln \left( \frac{1 - \epsilon_t}{\epsilon_t} \right)
$$
  

- **Atualização dos pesos**:
  
$$
  w_i \leftarrow w_i \cdot \exp(\alpha_t \cdot I(y_i \neq h_t(x_i)))
$$
  
  Importante notar que aqui os pesos são então normalizados para que sua soma seja 1.


**Sensibilidade a *Outliers***: Como o algoritmo dá mais peso às observações difíceis, ele pode ser sensível a *outliers*, que podem distorcer o aprendizado.