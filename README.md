# Equipe
*DreamCoders* - Samuel Soares de Araújo e Eric Leandro Lima Mendoça.

# INTRODUÇÃO
Repositório do Projeto Final de Algoritmos Genéticos da disciplina de *Redes Neurais e Algoritmos Genéticos*. A disciplina faz parte da grade curricular do 3º semestre da ILUM - Escola de Ciência, sendo administrada pelo Professor Daniel Cassar. 

O repositório está dividido em duas partes:
- O "notebook oficial", contendo a contextualização dos datasets e dos objetivos do presente trabalho, além do tratamento dos datasets. Ademais, há a criação, desenvolvimento e resultado das populações produzidas pelo algoritmo genético junto a uma comparação com os dados originais do dataset considerando as pontuações da função objetivo e a distância de Manhattan da população final em relação as features/propriedades reais.
  
- A *lore* criada funciona como uma história baseada na cultura geek, em especial, em RPGs de fantasia medieval. Toda a lore foi desenvolvida pensando em inspirar o leitor ou pesquisador a se envolver com o problema, permitindo o fácil entendimento para uma situação hipotética. [ Esperamos que gostem, fizemos com muito carinho :) ]

## Objetivo
O projeto consiste na aplicação de um algoritmo genético para criação de possíveis materiais com alta *resistência* e baixa densidade. Para isso, foi criado uma função objetivo que levasse em conta as propriedades ligadas a *resistência* e a densidade para pontuar o quão bom é o material. Com o intuito de validar se os materiais da população final possuem propriedades semelhantes, por meio do cálculo da distância de Manhattan, aos materiais reais do dataset base.
Vale ressaltar que não faz parte do escopo do projeto se aprofundar nos aspectos técnicos, sendo necessário, para isso, a leitura das referências bibliográficas.

# Metodologia
Para alcançar o objetivo do trabalho de forma plena, foi realizado uma série de etapas: 

- Primeiro, a manipulação dos dados partindo da transformação dos dados de csv para o formato dataframe seguido do tratamento desses dataframes a partir da exploração dos mesmos, permitindo, assim, filtrar as features relevantes para a função objetivo;
- Depois, foi criada uma função objetivo com as features relevantes e os pesos dela foram determinados de forma arbitrária com base na influência de cada propriedade;
- Ainda em relação às definições, definimos o tamanho da população, número de gerações, taxa de cruzamento e taxa de mutação;
- Após a criação da função objetivo, foi criada uma população inicial artificial, levando em conta os máximos e mínimos de cada propriedade dos materiais do dataset e com um filtro para não criação de indivíduos com uma pontuação melhor que a melhor material do dataset original, assim, evitando materiais instáveis;
- No uso dos operadores, foram feitas alterações na mutação sucessiva e no cruzamento para que não houvesse a criação de indivíduos com uma pontuação na função objetivo melhor que o melhor material do dataset base, dessa forma, evitando a criação de "super materiais" inviáveis;
- Após a criação do algoritmo, aplicamos ele para a criação de uma população com possíveis candidatos a materiais ótimos estáveis.
- Por fim, para filtrar os materiais realmente viáveis, foi calculado a distância Manhattan entre cada indivíduo da população final em relação aos materiais reais do dataset base.

# Tecnologias/Técnicas
## Linguagem
- Python
## Bibliotecas e Módulos
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
O notebook da lore foi desenvolvido com muita atenção para uma imersão semelhante a uma novela de fantasia medieval com anões e magia. Todas as imagens utilizadas para ilustração foram feitas por IA, permitindo o uso irrestrito das ilustrações. Em relação a história, o desenvolvimento por inteiro é original e se encaixa de maneira suave aos tópicos apresentados no notebook do código e das explicações em si. É recomendado que a leitura da lore seja feita antes da leitura do outro notebook, porém a leitura da lore não é obrigatória para o entendimento do desenvolvimento da exploração dos datasets e do algoritmo genético.

## Código
O notebook com o código possui a estrutura inspirada em publicações científicas, unindo formalidade com uma leitura fluida e de fácil entendimento(assim esperamos). É de suma importância que os textos sejam lidos na ordem e ao decorrer da elaboração dos códigos e dos resultados para que haja um entendimento correto e completo da proposta, do raciocínio e dos resultados. No conteúdo em si, há a introdução aos principais tópicos em relação aos materiais junto às suas features e ao conceito de resistência(definido pelos autores), além dos códigos com as explicações necessárias, e, por fim, os resultados das ligas criadas e as conclusões dos autores. 

Caso ocorra dúvidas ou haja o desejo de aprofundamento, todas as referências utilizadas estão presentes aqui no Readme e ao fim do notebook.

# Dataset
O Dataset base contém 1.552 materiais com as suas propriedades mecânicas, totalizando 15 propriedades relacionadas. No entanto, por conta de algumas linhas possuírem valores NaN, foi optado por considerar apenas as colunas completamente preenchidas e que não possuíam strings, sendo elas:

- Ultimate Tensile Strength/Su (MPa) 
- Yield Strength/Sy (MPa)
- Elastic Modulus/E (MPa)
- Shear Modulus/S (MPa)
- Density/Ro (MPa)

# Referências
## Datasets
[1]NAWALE, Purushottam. Materials and their Mechanical Properties. 2023. Disponível em: https://www.kaggle.com/datasets/purushottamnawale/materials. Acesso em: 28 maio 2024.

## Literatura 
[1] LOURENÇO, Hévila. Aprendizado de Máquinas - Algoritmos Genéticos. 2023. Disponível em: https://www.youtube.com/watch?v=tfPYwaNkI7o. Acesso em: 28 maio 2024.

[2] Cassar, Daniel(2024). ATP-303 GA 2.3 - Notebook algoritmo genético.ipynb. Retirado do repositório da matéria Redes Neurais e Algoritimos Genéticos da ILUM - Escola de Ciência.

[3] Cassar, Daniel(2024). ATP-303 GA 3.3 - Notebook caixas não-binárias.ipynb. Retirado do repositório da matéria Redes Neurais e Algoritimos Genéticos da ILUM - Escola de Ciência..


## Bibliotecas e Módulos
[1] PYTHON Software Foundation. Statistics — Mathematical statistics functions. Python 3.12.3 documentation, 2023. Disponível em: https://docs.python.org/3/library/statistics.html. Acesso em: 28 maio 2024.

[2] PYDATA. pandas — Python Data Analysis Library. pandas.pydata.org, 2024. Disponível em: https://pandas.pydata.org/. Acesso em: 28 maio 2024.

[3] PYTHON Software Foundation. random — Generate pseudo-random numbers. Python 3.12.3 documentation, 2023. Disponível em: https://docs.python.org/3/library/random.html. Acesso em: 28 maio 2024.









