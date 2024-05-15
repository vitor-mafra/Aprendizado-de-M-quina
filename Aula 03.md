#### Retomando alguns conceitos relativos ao Perceptron

O Perceptron é um modelo linear - a função é dada por uma combinação linear entre os pesos dos atributos. Todos os modelos que se baseiam no perceptron contém **taxa de aprendizado** - a taxa de atualização dos pesos de um perceptron. É interessante adaptar essa taxa de aprendizado ao longo do treinamento (normalmente a taxa de aprendizado começa bem alta e vai decaindo ao longo das iterações - isto é conhecido como aprendizado adaptativo). 

#### Época
Época é quando um modelo visita, ao longo do treinamento, todas as entradas disponíveis. A quantidade de épocas também costuma ser um hiperparâmetro.

Padrão de atualização dos pesos de um perceptron
Slides (link aqui)

#### Capacidade
O Perceptron tem um problema de capacidade - ela é muito baixa. A capacidade tem a ver com o conjunto de hipóteses. Se suas hipóteses estão descoladas das soluções reais de um dado problema, a capacidade deste dado modelo é baixa.