[[2024-06-05]]

Recapitulação de *Deep Learning* das últimas aulas - aprendizado de características de forma não supervisionada. Autoencoders e svms. 

Arquiteturas específicas para visão computacional e NLP e o porquê disso ser necessário.
### Visão Computacional
Seres humanos são tão bons em reconhecer padrões e objetos que é difícil compreender o desafio que é treinar um computador para fazer o mesmo. Alguns dos diversos problemas que podem aparecer: 
- Parte do objeto pode estar coberta ou incompleta
- Um mesmo objeto pode ter diversas formas
- Uma imagem é uma representação 2D de um objeto tridimensional - há perda de informação
- Diferentes pontos de vista de uma mesma coisa podem trazer representações completamente diferentes de um mesmo objeto
##### Arquitetura Convolucional
A arquitetura convolucional, ou Redes Neurais Convolucionais (CNNs), é uma classe de redes neurais especialmente eficaz para tarefas de visão computacional. Elas são projetadas para processar dados que têm uma estrutura em grade, como imagens, de maneira que possam capturar padrões espaciais e hierárquicos com eficiência.

CNNs eliminam a necessidade de engenharia manual de características, que era um passo trabalhoso e específico de domínio em técnicas de visão computacional tradicionais. A rede aprende automaticamente as características relevantes diretamente a partir dos dados brutos.

1) **Camadas Convolucionais**:
    - Estas camadas utilizam filtros (ou kernels) que percorrem a imagem de entrada para extrair características locais, como bordas, texturas e padrões específicos. Isso permite que a rede aprenda a detectar características importantes de maneira local.
    
2) **Camadas de Pooling**:
    - Camadas de pooling reduzem a dimensionalidade das representações intermediárias, mantendo as informações mais importantes. Isso não só ajuda a reduzir a complexidade computacional, mas também torna a rede mais robusta a pequenas variações e deslocamentos na imagem.
    
3) **Camadas de Ativação**:
    - Introduzem não-linearidades na rede, permitindo que ela aprenda representações mais complexas. A função ReLU (Rectified Linear Unit) é a mais comum, ativando apenas as partes relevantes do sinal.