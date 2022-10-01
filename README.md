# Projeto de Insights: House Rocket

Todo contexto de negócio envolvendo este projeto é fictício. A base de dados foi extratida do [Kaggle](https://www.kaggle.com/datasets/harlfoxem/housesalesprediction) e desenvolvida com a ajuda da [Comunidade DS](https://www.comunidadedatascience.com/).

## 1. Negócio

A House Rocket é uma plataforma digital que tem como modelo de negócio, a compra e a venda de imóveis usando tecnologia.

Sua principal estratégia é comprar boas casas em ótimas localizações com preços baixos e depois revendê-las posteriormente à preços mais altos. Quanto maior a diferença entre a compra e a venda, maior o lucro da empresa e portanto maior sua receita.

### 1.1. Questões de negócio

O CEO da House Rocket trouxe três dúvidas principais para sanar suas dores:

1. Quais casas a House Rocket deveria comprar e por qual preço de compra?
2. Uma vez a casa em posse da empresa, qual o melhor momento para vendê-las e qual seria o preço da venda?
3. A House Rocket deveria fazer uma reforma para aumentar o preço da venda? Quais seriam as sugestões de mudanças? Qual o incremento no preço dado por cada opção de reforma?

### 1.2. Base de dados

As variáveis do dataset original são:

Feature | Description
------------ | -------------
|id | Identificador de cada propriedade.|
|date | Data em que a propriedade ficou disponível.|
|price | O preço de cada imóvel, considerado como preço de compra.|
|bedrooms | Número de quartos.|
|bathrooms | O número de banheiros, o valor 0,5 indica um quarto com banheiro, mas sem chuveiro. O valor 0,75 ou 3/4 banheiro representa um banheiro que contém uma pia, um vaso sanitário e um chuveiro ou banheira.|
|sqft_living | Pés quadrados do interior das casas.|
|sqft_lot | Pés quadrados do terreno das casas.|
|floors | Número de andares.|
|waterfront | Uma variável fictícia para saber se a casa tinha vista para o mar ou não, '1' se a propriedade tem vista para o mar, '0' se não.|
|view | Vista, Um índice de 0 a 4 de quão boa era a visualização da propriedade.|
|condition | Um índice de 1 a 5 sobre o estado das moradias, 1 indica propriedade degradada e 5 excelente.|
|grade | Uma nota geral é dada à unidade habitacional com base no sistema de classificação de King County. O índice de 1 a 13, onde 1-3 fica aquém da construção e design do edifício, 7 tem um nível médio de construção e design e 11-13 tem um nível de construção e design de alta qualidade.|
|sqft_above | Os pés quadrados do espaço habitacional interior acima do nível do solo.|
|sqft_basement | Os pés quadrados do espaço habitacional interior abaixo do nível do solo.|
|yr_built | Ano de construção da propriedade.|
|yr_renovated | Representa o ano em que o imóvel foi reformado. Considera o número ‘0’ para descrever as propriedades nunca renovadas.|
|zipcode | Um código de cinco dígitos para indicar a área onde se encontra a propriedade.|
|lat | Latitude.|
|long | Longitude.|
|sqft_living15 | O tamanho médio em pés quadrados do espaço interno de habitação para as 15 casas mais próximas.|
|sqft_lot15 | Tamanho médio dos terrenos em metros quadrados para as 15 casas mais próximas.|


## 2. Planejamento da Solução

### 2.1 Produto Final
O que será entregue?

- Um link para acessar o dashboard com a visibilidade de cada apartamento do seu portfólio.

### 2.2 Ferramentas

- Python 3.8.3
- Streamlit
- Geopandas
- LunarVim
- Jupyter Notebook ( Análise e prototipagens )

### 2.3 Processo (Passo a passo)

#### 2.3.1 - Filtro dos imóveis por um ou várias regiões

Objetivo: Visualizar imóveis por código postal<br>
Ação do Usuário: Digitar um ou mais códigos desejados<br>
A visualização: Uma tabela com todos os atributos e filtrada por código postal

#### 2.3.2 - Escolher uma ou mais variáveis para visualizar

Objetivo: Visualizar as características do imóveis<br>
Ação do Usuário: Digita as características desejadas<br>
A visualização: Uma tabela com todos os atributos selecionados

#### 2.3.3 - Observar o número total de imóveis, a média de preço, a média da sala de estar e também a média do preço por metro quadrado em cada um dos códigos postais

Objetivo: Visualizar as médias de algumas métricas por região<br>
Ação do Usuário: Digita as métricas desejadas<br>
A visualização: Uma tabela com todos os atributos selecionados

#### 2.3.4 - Analisar cada uma das colunas de um modo mais descritivo

Objetivo: Visualizar métricas descritivas de cada atributo escolhido<br>
Ação do Usuário: Digita as métricas desejadas<br>
A visualização: Uma tabela com métricas por atributo

#### 2.3.5 - Um mapa com a densidade de portfolio por região e tamém densidade de preço

Objetivo: Visualizar a densidade de portfólio no mapa (número de imóveis por região)<br>
Ação do Usuário: Nenhuma ação<br>
A visualização: Um mapa com a densidade de imóveis por região

#### 2.3.6 - Checar a variação anual de preço

Objetivo: Observar variações anuais de preços<br>
Ação do Usuário: Filtra os dados pelo ano<br>
A visualização: Um gráfico de linha com os anos em X e preços médios em Y

#### 2.3.7 - Checar a variação diária de preço

Objetivo: Observar variações diárias de preços<br>
Ação do Usuário: Filtra os dados por dia<br>
A visualização: Um gráfico de linha com os dias em X e preços médios em Y<br>

#### 2.3.8 - Conferir a distribuição dos imóveis por:
- Preço
- Número de quartos
- Número de banheiros
- Número de andares
- Vista para a água ou não

Objetivo: Observar a concentração dos imóveis por preço, quartos, banheiros e andares<br>
Ação do Usuário: Filtra de preço, quartos, banheiros e andares<br>
A visualização: Um histograma com cada atributo definido
	
## 3. Resultado das análises

1. Quais imóveis a House Rocket deveria comprar ?
R: Preferência de casas que contém de 2 a 3 quartos e vista para o mar.

2. A House Rocket deveria fazer uma reforma para aumentar o preço da venda? Quais seriam as sugestões de mudanças? Qual o incremento no preço dado por cada opção de reforma?
R: As reformas tem gerado um aumento de 17% no preço dos imóveis.

## 4. Conclusão

O objetivo do projeto foi alcançado com sucesso para que o CEO esteja melhor preparado para tomar suas decisões na compra e venda dos imóveis do seu portfólio.

## 5. Próximos Passos

- Implementar um modelo de machine learning com o objetivo de apresentar quantos % um imóvel pode valorizar na região após uma reforma.
- Aprimorar o dashboard com objetivo de facilitar mais insigths.
