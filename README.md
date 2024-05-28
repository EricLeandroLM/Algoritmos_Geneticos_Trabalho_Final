# Equipe
*DreamCoders* - Samuel Soares de Araújo e Eric Leandro Lima Mendoça.

# INTRODUÇÃO
Repositório do Projeto Final de Algoritmos Genéticos da disciplina de *Redes Neurais e Algoritmos Genéticos*. A disciplina faz parte da grade curricular do 3º semestre da ILUM - Escola de Ciência, sendo administrada pelo Professor Daniel Cassar. 

O repositório está dividido em duas partes:
- O "notebook oficial", contendo a contextualização dos datasets e dos objetivos do presente trabalho, além do tratamento dos datasets. Ademais, há a criação, desenvolvimento e resultado das populações produzidas pelo algoritmo genético junto a uma comparação com os dados originais do dataset considerando as pontuações da função objetivo e a distância de Manhattan da população final em relação as features/propriedades reais.
  
- A *lore* criada funciona como uma história baseada na cultura geek, em especial, em RPGs de fantasia medieval. Toda a lore foi desenvolvida pensando em inspirar o leitor ou pesquisador a se envolver com o problema, permitindo o fácil entendimento para uma situação hipotética. [ Esperamos que gostem, fizemos com muito carinho :) ]

## Objetivo
O projeto consiste na aplicação de um algoritmo genético para criação de possíveis ligas metálicas com alta *resistência* e baixa densidade. Para isso, foi criado uma função objetivo que levasse em conta as propriedades ligadas a *resistência* e a densidade para pontuar o quão bom é o material. Com o intuito de validar se o materiais da população final possuem propriedades semelhantes, por meio do cálculo dad istância de Manhattan, aos materiais reais do dataset base.
Vale ressaltar que não faz parte do escopo do projeto se aprofundar nos aspectos técnicos, sendo necessário, para isso, a leitura das referências bibliográficas.

# Metodologia
Para alcançar o objetivo do trabalho de forma plena, foi realizado uma série de etapas: 

- Primeiro, a manipulação dos dados partindo da transformação dos dados de csv para o formato dataframe seguido do tratamento desses dataframes a partir da exploração dos mesmos, permitindo, assim, filtrar as features relevantes para a função objetivo;
- Depois, foi criada uma função objetivo com as features relevantes e os pesos dela foram determinados de forma arbitrária com base na influência de cada propriedade;
- Ainda em relação as definições, definimos o tamanho da população, número de gerações, taxa de cruzamento e taxa de mutação;
- Após a criação da função objetivo, foi criada uma população inicial artificial, levando em conta os máximos e minímos de cada propriedade nas ligas do dataset e com um filtro para não criação de indivíduos com uma pontuação melhor que a melhor liga metálica do dataset original, assim, evitando materiais instáveis;
- No uso dos operadores, foram feitas alterações na mutação sucessiva e no cruzamento para que não houvesse a criação de indivíduos com uma pontuação na função objetivo melhor que a melhor das ligas metálicas do dataset base, dessa forma, evitando a criação de "super ligas" inviáveis;
- Após a criação do algoritmo, aplicamos ele para a criação de uma população com possíveis candidatos a ligas ótimas estáveis.
- Por fim, para filtrar as ligas realmente viáveis, foi calculado a distância Manhattan entre cada indivíduo da população final em relação as ligas reais do dataset base.

# Tecnologias/Técnicas
## Linguagem
- Python
## Biblitecas
- Statistics
- Pandas
- Random
## Plataforma de computação
- Jupyter Notebook

# Organização
O Repositório está dividido em 4 partes:

- Readme -> Guia do projeto. Incluindo a motivação, origem, fontes e organização do github;
- Datasets -> Pasta com o arquivo referente ao dataset base com as ligas reais, o arquivo está disponibilizado no formato *.csv*;
- Notebooks -> Essa pasta consiste em dois arquivos com a extensão *.ipynb*. Incluindo o notebook com o desenvolvimento da *lore*. Além do notebook com a aplicação do algoritmo genético para suposição de ligas ótimas junto ao detalhamento do processo de raciocínio e explicação dos códigos passo a passo;
- Imagens -> Pasta com as imagens utilizadas para ilustração da narrativa do notebook referente a lore;

## Lore
O notebook da lore foi desenvolvido com muita atenção para uma imersão semelhante a uma novel de fantasia medieval com anões e magia. Todas as imagens utilizadas para ilustração foram feitas por IA, permitindo o uso irrestrito das ilustrações. Em relação a história, o desenvolvimento por inteiro é original e se encaixa de maneira suave aos tópicos apresentados no notebook do código e das explicações em si. É recomendado que a leitura da lore seja feita antes da leitura do outro notebook, porém a leitura da lore não é obrigatória para o entendimento do desenvolvimento da exploração dos datasets e do algoritmo genético.

## Código
O notebook com o código possui a estrutura inspirada em publicações científicas, unindo formalidade com uma leitura fluída e de fácil entendimento(assim esperamos). É de suma importância que os textos sejam lidos na ordem e ao decorrer da elaboração dos códigos e dos resultados para que haja um entendimento correto e completo da proposta, do raciocínio e dos resultados. No conteúdo em si, há a introdução aos principais tópicos em relação as ligas metálica junto as suas features e ao conceito de resistência(definido pelos autores), além dos códigos com as explicações necessárias, e, por fim, os resultados das ligas criadas e as conclusões dos autores. 

Caso ocorra dúvidas ou haja o desejo de aprofundamento, todas as referências utilizadas estão presentes aqui no Readme e ao fim do notebook.

# Datasets

*Features*
- Número de elétrons
- Número de elétrons de valência
- Número atômico
- Eletronegativa de Pauling
- Eletronegatividade do estado de oxidação mais comum
- Raios atômicos covalentes
- Raio de Vander Waals
- Energia de ionização do neutro
- Média de todos os elétrons
- Densidade média
- Peso atômico
  
Entretanto, o dataset de teste possui duas colunas a mais. A primeira corresponde a fórmula molecular do mineral e a segunda ao tipo de estrutura ceistalina.
  
# Referências
## Datasets
[1] Dumlao, J. (2024). Prediction of Mohs Hardness with Machine Learning. Kaggle. Retirado de https://www.kaggle.com/datasets/jocelyndumlao/prediction-of-mohs-hardness-with-machine-learning/data

[2] Garnett, J. C. (2022). Dataset for Mohs Hardness Prediction. Mendeley Data. DOI: 10.17632/jm79zfps6b.1. retirado de https://data.mendeley.com/datasets/jm79zfps6b/1

## Literatura 
[1] TABOR, David. Mohs's hardness scale-a physical interpretation. Proceedings of the Physical Society. Section B, v. 67, n. 3, p. 249, 1954.

[2] Cassar, Daniel(2024). ATP-303 NN 1.1 - Introdução.pdf. Retirado do repositório da matéria Redes Neurais e Algoritimos Genéticos da ILUM - Escola de Ciência.

[3] Cassar, Daniel(2024). ATP-303 NN 1.2 - Redes neurais.pdf. Retirado do repositório da matéria Redes Neurais e Algoritimos Genéticos da ILUM - Escola de Ciência.

[4] Cassar, Daniel(2024). ATP-303 NN 1.3 - Regra da cadeia.pdf. Retirado do repositório da matéria Redes Neurais e Algoritimos Genéticos da ILUM - Escola de Ciência.

[5] Cassar, Daniel(2024). ATP-303 NN 1.4 - Backpropagation.pdf. Retirado do repositório da matéria Redes Neurais e Algoritimos Genéticos da ILUM - Escola de Ciência.

[6] Cassar, Daniel(2024). ATP-303 NN 3.2 - Notebook Autograd.ipynb. Retirado do repositório da matéria Redes Neurais e Algoritimos Genéticos da ILUM - Escola de Ciência.

[7] Cassar, Daniel(2024). ATP-303 NN 4.2 - Notebook MLP.ipynb. Retirado do repositório da matéria Redes Neurais e Algoritimos Genéticos da ILUM - Escola de Ciência.

[8] Cassar, Daniel(2024). ATP-303 NN 5.2 - Notebook PyTorch.ipynb. Retirado do repositório da matéria Redes Neurais e Algoritimos Genéticos da ILUM - Escola de Ciência.

## Bibliotecas
[1] PyTorch. (2024). PyTorch: Tensors and Dynamic neural networks in Python with strong GPU acceleration. Retirado de https://pytorch.org/.

[2] PyTorch. (2024). torch.nn - PyTorch v1.10.1 documentation. Retirado de https://pytorch.org/docs/1.10.1/nn.html.

[3] PyTorch. (2024). torch.optim - PyTorch v1.10.1 documentation. Retirado de https://pytorch.org/docs/1.10.1/optim.html.

[4] Pandas. (2010). pandas documentation. Retirado de https://pandas.pydata.org/docs/.

[5] Scikit-learn. (2011). scikit-learn preprocessing module documentation. Retirado de https://scikit-learn.org/stable/modules/classes.html#module-sklearn.preprocessing.

[6] Scikit-learn. (2011). scikit-learn metrics module documentation. Retirado de https://scikit-learn.org/stable/modules/classes.html#module-sklearn.metrics.

[7] Matplotlib. (2007). matplotlib.pyplot documentation. Retirado de https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.html.

[8] NumPy. (2020). NumPy v1.22.0 documentation. Retirado de https://numpy.org/doc/stable/.






