# Equipe
*DreamCoders* - Samuel Soares de Araújo e Eric Leandro Lima Mendoça.

# INTRODUÇÃO
Repositório do Projeto Final de Redes Neurais da disciplina de *Redes Neurais e Algoritimos Genéticos*. A disciplina faz parte da grade curricular do 3º semestre da ILUM - Escola de Ciência, sendo administrada pelo Professor Daniel Cassar. 

O repositório está dividido em duas partes:
- O "notebook oficial", contendo a contextualização dos datasets e dos objetivos do presente trabalho, além do tratamento dos datasets. Ademais, há o desenvolvimento e otimização de uma rede neural para previsão da dureza de materiais dado as informações das features junto aos resultados da aplicação da rede neural no dataset de teste e as conclusões deduzidas a partir desses resultados.
  
- A *lore* criada funciona como uma história baseada na cultura geek, em especial, em RPGs de fantasia medieval. Toda a lore foi desenvolvida pensando em inspirar o leitor ou pesquisador a se envolver com o problema, permitindo a fácil aplicação da rede neural para uma situação hipotética. [ Esperamos que gostem, fizemos com muito carinho :) ]

## Objetivo
O projeto consiste na aplicação e na otimização de hiperparâmetros de uma rede neural do tipo MLP para prever a dureza, na escala de Mohs, de minerais a partir de 11 features inerentes a cada material. A partir dos resultados da predição, analisar a eficácia de redes neurais MLP para predição de dureza de minerais com estruturas cristalinas distintas e explorar as variações para cada tipo de estrutura cristalina, considerando as amostragens utilizadas.
Vale ressaltar que não faz parte do escopo do projeto se aprofundar nos aspectos técnicos, sendo necessário, para isso, a leitura das referências bibliográficas.

# Metodologia
Para alcançar o objetivo do trabalho de forma plena, foi realizado uma série de etapas: 

- Primeiro, a manipulação dos dados partindo da transformação dos dados de csv para o formato dataframe de tratamento para os datasets junto ao tratamento dos datasets a partir da exploração dos mesmos, permitindo, assim, filtrar as features necessária e relevantes para previsão da dureza, depois, foi feita a segmentação dos dois datasets em treino e teste junto a normalização de dados. 
- Após a etapa de manipulação, foi construída uma rede neural MLP do tipo regressora, logo depois, fez-se a otimização dos hiperparâmetros usando SGD do próprio PyTorch, ademais, foi feito o treinamento aprimorando a perda através da aplicação de 100 arquiteturas de rede distintas. 
- Por fim, aplicou-se a rede neural treinada no dataset de teste e computou-se diversas métricas de erros para análise da precisão da rede neural para os diferentes tipos de estrutura cristalina.

# Tecnologias/Técnicas
## Linguagem
- Python
## Biblitecas
- Pytorch
- Numpy
- Matplotlib
- Pandas
- ScikitLearn
## Plataforma de computação
- Jupyter Notebook

# Organização
O Repositório está dividido em 4 partes:

- Readme -> Guia do projeto. Incluindo a motivação, origem, fontes e organização do github.
- Datasets -> Pasta com os dois arquivos referentes ao dataset de treino e de validação, os arquivos estão disponibilizados no formato *.csv*
- Notebooks -> Essa pasta consiste em dois arquivos com a extensão *.ipynb*. Incluindo o notebook com o desenvolvimento da *lore*. Além do notebook com a aplicação da rede neural otmizada para predição junto ao detalhamento do processo de raciocínio e explicação dos códigos passo a passo em norma culta científica.
- Imagens -> Pasta com as imagens utilizadas para ilustração da narrativa do notebook referente a lore.

## Lore
O notebook da lore foi desenvolvido com muita atenção para uma imersão semelhante a uma novel de fantasia medieval com dragões e magia. Todas as imagens utilizadas para ilustração foram feitas por IA, permitindo o uso irrestrito das ilustrações, em relação a história, o desenvolvimento por inteiro é original e se encaixa de maneira suave aos tópicos apresentados no notebook do código e das explicações em si. É recomendado que a leitura da lore seja feita antes da leitura do outro notebook, porém a leitura da lore não é obrigatória para o entendimento do desenvolvimento da exploração dos datasets e da predição pela rede neural.

## Código
O notebook com o código possui a estrutura inspirada em publicações científicas, unindo formalidade com uma leitura fluída e de fácil entendimento(assim esperamos). É de suma importância que os textos sejam lidos na ordem e ao decorrer da elaboração dos códigos e dos resultados para que haja um entendimento correto e completo da proposta, do raciocínio e dos resultados. No conteúdo em si, há a introdução aos principais tópicos em relação aos minerais junto as suas features e ao conceito de dureza(alvo principal da predição), além dos códicos com as explicações necessárias, e, por fim, os resultados das predições e as conclusões dos autores. Caso ocorra dúvidas ou haja o desejo de aprofundamento, todas as referências utilizadas estão presentes aqui no Readme e ao fim do notebook.

# Datasets
Os dados extraídos consiste em dois databases de minerais, uma para treino com 622 minerais e outro para teste com 51 minerais. Ambos os dataset possuem um total de 11 descrições atômicas de cada mineral, ou seja, 11 features e a dureza como target.
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

## Dataset de Treino
O Dataset de treino é composto por 622 minerais com composições únicas obtidos por permutações composicionais de uma base de dados com 369 minerais únicos retirados do *Physical and Optical Properties of Minerals CRC Handbook of Chemestry and Physics* e da *American Mineralogist Crystal Structure Database* . Os minerais presentes do dataset possuem estruturas critalinas diversas como já foi mencionado, sendo: 

- 210 de estrutura monoclínica;
- 96 de estrutura romboédrica;
- 89 de estrutura hexagonal;
- 80 de estrutura tetragonal;
- 73 de estrutura cúbica;
- 50 de estrutura ortorrômbica;
- 22 de estrutura triclínica;
- 1 de estrutura trigonal;
- 1 de estrutura amorfa.

## Dataset de Teste
O dataset de teste é composto por 51 cristais sintéticos singulares retirados da literatura, sendo a distribuição das estruturas cristalinas:

- 15 de estrutura monoclínica;
- 7 de estrutura tetragonal;
- 7 de estrutura hexagonal;
- 6 de estrutura ortorrômbicas;
- 4 de estrutura cúbica;
- 3 de estrutura romboédrica.
  
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






