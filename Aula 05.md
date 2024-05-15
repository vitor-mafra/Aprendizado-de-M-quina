[[2024-03-25]]

Recapitulação dos conceitos introduzidos na última aula:
n -> tamanho da amostra
épsilon -> o quão bom quero que o modelo seja/quão tolerante ao erro se é
erro empírico -> erro que pode ser medido -> erro na amostra
erro esperado -> não pode ser medido, apenas estimado

Exemplo do reconhecimento de dígitos escritos à mão:
- Imagens de dígitos escritos à mão com 16x16 pixels
- X = vetorização de todos os pixels, vetor de tamanho 256
- Isso cria um problema, já que temos 256 parâmetros. Será que todos eles são necessários?
- **Como representar os dados é muito importante**
- Feature engeneering! Intensidade e simetria dos números podem ser escolhidos como features para ajudar nessa tarefa de diferenciação de dígitos

#### Pocket Perceptron -> Minimização de erro empírico
Escolher sempre o perceptron com o menor erro empírico, ou seja, ao longo do treino manter sempre o perceptron que minimiza o erro na amostra. 
Erro empírico geralmente é uma aproximação para a complexidade do modelo. Uma função que tem um erro empírico menor do que outra é sempre mais complexa.

SVM implementa um conceito de margem, que é responsável por penalizar a complexidade em um modelo.
