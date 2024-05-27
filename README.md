# Algoritmos Geneticos
Repositorio da matéria Rede Neurais e Algoritmos genéticos do 3° Semestre do Bacharelado em Ciência e Tecnologia - ILUM

## Redes Neurais

### MN2
Para realizar esta tarefa, foram criadas duas classes principais em Python: Elemento e Molecula. A classe Elemento representa um elemento químico, contendo atributos como o símbolo do elemento, seu número atômico, categoria, ano de descoberta e seu peso atômico. Já a classe Molecula recebe uma relação de elementos químicos e suas quantidades, sendo capaz de exibir o peso atômico da molécula criada, o "circulo magico" da molecula, o ano do atomo mais antigo e gerar uma fórmula química para a mesma.

- **Grimorio_dos_elementos_obscuros.jpg:** Imagem ilustrativa do monstro presente no notebook.
- **MN2.jpg:** Imagem de capa do notebook.
- **Monstrinho 2.ipynb:** Notebook com o codigo e a historia.

### MN3
Resumo

### MN4
O objetivo deste código é criar classes em Python para representar diferentes personagens de um jogo, como Mago, Tank, Guerreiro e Curandeiro, cada um com habilidades especiais únicas. Além disso, é implementada a classe Item para representar os itens que os personagens podem possuir. 

Foram utilizados métodos dunder (double underscore methods, ou métodos especiais) para realizar operações especiais em objetos dessas classes, como comparação, adição e subtração de itens, iteração sobre o inventário de um personagem e definição de comportamento de entrada e saída de um contexto.

Dentre os métodos dunder utilizados, destacam-se `__init__` para inicialização de objetos, `__str__` e `__repr__` para representação em string e formal dos objetos, `__eq__` para comparação de igualdade entre objetos, `__lt__` para comparação de ordem, `__add__` e `__sub__` para adição e subtração de valores, `__contains__` para verificação de presença de itens, `__iter__` e `__next__` para iteração sobre o inventário, e `__enter__` e `__exit__` para definição de comportamento de entrada e saída de um contexto.

Como exemplo, a classe `Personagem` representa um personagem genérico do jogo, com métodos para entrada e saída do campo de batalha, adição e subtração de pontos de vida, e iteração sobre o inventário. Cada classe de personagem específica, como `Mago`, `Tank`, `Guerreiro`, `Curandeiro`, possui uma habilidade especial que pode ser utilizada durante o jogo.

Uma classe adicional, `Guerreiro_sem_alma`, foi criada como uma variação do Guerreiro, com uma habilidade especial única.

- **Guerreiro_sem_alma.jpg:** Imagem ilustrativa do monstro presente no notebook.
- **MN4.jpg:** Imagem de capa do notebook.
- **Monstrinho 4.ipynb:** Notebook com o codigo e a historia.

### MN5
O objetivo deste código é implementar um regularizador Dropout em uma rede neural simples utilizando Python puro. A classe `NeuralNetwork` representa a rede neural, que possui uma camada oculta e uma camada de saída.

O método `forward` realiza a propagação direta dos dados pela rede, aplicando a função de ativação sigmoid na camada oculta e na camada de saída. Durante o treinamento, o Dropout é aplicado à camada oculta para evitar o overfitting. O método `backward` realiza a retropropagação para ajustar os pesos da rede com base no erro calculado.

A função `train` é responsável por treinar a rede neural usando os dados fornecidos, realizando várias épocas de treinamento e ajustando os pesos com base na taxa de aprendizagem especificada. Por fim, o método `predict` é utilizado para realizar previsões com base nos dados de entrada.

A implementação do Dropout na camada oculta é realizada através da aplicação de uma máscara binomial durante o treinamento, onde os neurônios são "desligados" com uma probabilidade especificada, ajudando a evitar o overfitting e melhorando a generalização do modelo.

- **General_Zumbi.jpg:** Imagem ilustrativa do monstro presente no notebook.
- **MN5.jpg:** Imagem de capa do notebook.
- **Monstrinho 5.ipynb:** Notebook com o codigo e a historia.

### MN6
O objetivo deste código é implementar três novas funções de ativação em uma rede neural feita em Python puro, além da função sigmoidal já implementada. As novas funções de ativação são: ReLU (Rectified Linear Unit), Tangente Hiperbólica (Tanh), Swish, ELU (Exponential Linear Unit) e Softplus.

A função ReLU é uma função de ativação muito comum em redes neurais profundas devido à sua simplicidade e eficácia. Ela mapeia os valores de entrada para zero quando são negativos e mantém os valores positivos inalterados. A Tangente Hiperbólica (Tanh) é uma função de ativação que mapeia os valores de entrada para o intervalo entre -1 e 1, proporcionando uma alternativa à função sigmoidal que apresenta um gradiente mais forte. Já a Softplus é uma função de ativação que produz uma saída suave e contínua, aproximando-se da identidade para entradas positivas e se aproximando de zero para entradas negativas.

A função Swish é uma função de ativação proposta recentemente que usa a função sigmoidal em uma forma modulada. Ela é considerada uma alternativa à ReLU, apresentando uma saída mais suave e contínua.

Já a função ELU é outra função de ativação que, assim como a ReLU, é uma alternativa à função sigmoidal. ELU é uma função definida para valores positivos e negativos e é mais suave do que a ReLU, permitindo treinamento mais rápido de redes neurais profundas e uma melhor generalização.

Cada função de ativação implementada possui também o método para calcular a derivada da função, que é essencial para a retropropagação do erro durante o treinamento da rede neural. Essas funções de ativação oferecem diferentes comportamentos não-lineares que podem ser úteis em diferentes tipos de problemas e arquiteturas de rede neural.

Essas funções de ativação adicionais proporcionam uma variedade de opções para a construção de arquiteturas de rede neural e podem ser exploradas de acordo com as necessidades específicas de cada aplicação.

- **Golem_de_carne.jpg:** Imagem ilustrativa do monstro presente no notebook.
- **MN6.jpg:** Imagem de capa do notebook.
- **Monstrinho 6.ipynb:** Notebook com o codigo e a historia.

### MN7
Neste código, a classe `NeuralNetwork`, usada nos notebooks anteriores, foi modificada para funcionar como um classificador multiclasse em vez de uma rede neural classificadora binaria. As principais alterações incluem:

1. **Função de Ativação Softmax:** Em vez de usar a função de ativação sigmoid para a camada de saída, foi implementada a função de ativação softmax, que é mais adequada para problemas de classificação multiclasse. A função softmax converte as saídas da rede em uma distribuição de probabilidade sobre as classes.

2. **Função de Perda Cross-Entropy:** Para problemas de classificação multiclasse, a função de perda mais comumente usada é a entropia cruzada (cross-entropy loss), que é mais apropriada do que a função de perda baseada em resíduos quadrados usada em problemas de regressão.

3. **Ajustes na Retropropagação:** Na retropropagação, a forma como o erro é propagado de volta para a camada oculta foi ajustada para se adequar à função de ativação softmax na camada de saída.

4. **Saída de Predição:** A saída da função `forward` foi modificada para retornar as probabilidades previstas para cada classe em vez dos valores reais.

Essas alterações permitem que a rede neural seja treinada e usada para classificar dados em várias classes. Para treinar a rede, os rótulos esperados (`y`) devem ser codificados no formato one-hot, onde cada classe é representada como um vetor binário com um valor de 1 na posição correspondente à classe e valores de 0 em todas as outras posições.

- **Mumia_da_Tempestade.jpg:** Imagem ilustrativa do monstro presente no notebook.
- **MN7.jpg:** Imagem de capa do notebook.
- **Monstrinho 7.ipynb:** Notebook com o codigo e a historia.

### MN8
Resumo

### MN9
Nesse notebook está a implementação da função `mc_dropout_prediction` para calcular a incerteza de previsão usando a estratégia de Monte Carlo Dropout. Essa função realiza várias previsões com a rede neural usando o dropout durante o teste e retorna a média e o desvio padrão das previsões para cada classe.

A ideia por trás do Monte Carlo Dropout é que, durante o teste, o dropout é aplicado à rede neural várias vezes, gerando diferentes previsões para os mesmos dados de entrada. Em seguida, a média dessas previsões é calculada como a previsão final, e o desvio padrão é usado como uma medida de incerteza.

Essa abordagem permite que a rede neural forneça não apenas uma previsão única, mas também uma estimativa de quão confiante ela está em sua previsão. Isso é útil em situações em que é importante conhecer a incerteza associada à previsão, como em sistemas de tomada de decisão automatizados ou em tarefas de classificação onde as classes são desbalanceadas.

- **Ceifador_de_almas.jpg:** Imagem ilustrativa do monstro presente no notebook.
- **MN9.jpg:** Imagem de capa do notebook.
- **Monstrinho 9.ipynb:** Notebook com o codigo e a historia.

### MN10
Nesse notebook está a implementação de uma rede neural com uma camada oculta e otimizador de Descida do Gradiente com Momento. O otimizador de Descida do Gradiente com Momento ajuda a acelerar o processo de aprendizado, permitindo que o modelo se mova mais rapidamente na direção certa e reduzindo oscilações desnecessárias.

Este otimizador utiliza o conceito de momento, que é uma média móvel exponencial dos gradientes anteriores. Isso permite que o otimizador acumule momento na direção consistente do gradiente, o que ajuda a "suavizar" o processo de atualização dos pesos.

Durante o treinamento, os momentos para os pesos e vieses são atualizados a cada passo de retropropagação, e os pesos e vieses são atualizados usando esses momentos.

Essa implementação permite treinar a rede neural usando o otimizador de Descida do Gradiente com Momento, o que pode resultar em um aprendizado mais rápido e estável.

- **Drake_Zumbi.jpg:** Imagem ilustrativa do monstro presente no notebook.
- **MN10.jpg:** Imagem de capa do notebook.
- **Monstrinho 10.ipynb:** Notebook com o codigo e a historia.

### MN11
Resumo

## Algoritmos Genéticos
