# Projeto de Análise de Vendas e Sistema de Recomendação - Meu Projeto

Neste projeto, vou compartilhar como criei um sistema de análise de vendas e um sistema de recomendação de produtos personalizado. A seguir, descrevo as etapas que segui para alcançar esse objetivo.

## Etapa 1: Geração Simulada de Banco de Dados

Primeiro, criei um banco de dados simulado com informações fictícias sobre clientes, produtos e transações. Isso envolveu a geração de dados aleatórios usando Python e a biblioteca Pandas.

- Gerei 100 clientes fictícios com nomes e e-mails fictícios.
- Criei 50 produtos fictícios com IDs, nomes e preços fictícios.
- Simulei 500 transações fictícias, associando clientes a produtos com detalhes como quantidade comprada e data da transação.
- Salvei os dados em arquivos CSV para uso posterior.

## Etapa 2: Carregamento e Visualização de Dados

Na segunda etapa, carreguei os dados gerados anteriormente e exibi as primeiras linhas de cada DataFrame para verificar a qualidade dos dados.

- Utilizei a biblioteca Pandas para carregar os arquivos CSV em DataFrames.
- Exibi as primeiras linhas dos DataFrames de clientes, produtos e transações para inspeção.

## Etapa 3: Tratamento de Dados

Para garantir que os dados estivessem prontos para análise, fiz algumas operações de tratamento de dados:

- Removi linhas com valores ausentes dos dados de clientes.
- Eliminei duplicatas em dados de clientes, produtos e transações.
- Tratei valores inválidos, garantindo que os preços dos produtos fossem não negativos.
- Converti a coluna de datas para o tipo DateTime.

## Etapa 4: Análise Descritiva e Métricas

Realizei análises descritivas dos dados e criei métricas para entender melhor as transações e os clientes:

- Calculei a receita total para cada transação multiplicando a quantidade de produtos pelo preço.
- Determinei a receita média por cliente.
- Calculei a taxa de conversão.
- Identifiquei os produtos mais populares.
- Realizei estatísticas gerais das transações.
- Calculei a média, mediana e moda dos preços dos produtos.

## Etapa 5: Análise de Comportamento do Cliente

Na quinta etapa, utilizei técnicas de aprendizado de máquina para segmentar os clientes com base na receita total. A segmentação foi feita usando o algoritmo K-Means.

- Calculei a receita total por cliente.
- Normalizei os dados para prepará-los para o K-Means.
- Apliquei o algoritmo K-Means para segmentação.
- Visualizei a segmentação em um gráfico de dispersão.

## Etapa 6: Previsão de Vendas

Nesta parte, criei um modelo de previsão de vendas usando regressão linear para prever vendas futuras com base em dados históricos.

- Calculei a receita total diária.
- Criei um modelo de regressão linear.
- Dividi os dados em conjuntos de treinamento e teste.
- Treinei o modelo e fiz previsões.
- Visualizei os resultados em um gráfico de dispersão.

## Etapa 7: Sistema de Recomendação de Produtos

Na sétima etapa, implementei um sistema de recomendação de produtos personalizado com base no histórico de compras dos clientes.

- Criei uma coluna fictícia de classificação chamada "Rating" para os dados de transações.
- Utilizei a biblioteca Surprise para carregar os dados e treinar um modelo de filtragem colaborativa.
- Gerei recomendações para um cliente específico e exibi as principais recomendações.
- Adicionei a coluna "Estimation" ao DataFrame de transações com as estimativas de classificação.

Este projeto foi criado para fins de demonstração e aprendizado, e os dados e algoritmos utilizados são fictícios. No entanto, ele serve como um exemplo de como abordar a análise de vendas e a criação de sistemas de recomendação.

## Observações das Análises

Durante a análise dos dados e a criação do sistema de recomendação, observei os seguintes pontos:

### Dados de Vendas

- A análise dos dados de vendas revelou uma grande variação nos preços dos produtos, com preços que variam de $10 a $1000. Isso pode indicar uma ampla gama de produtos disponíveis para os clientes.

- O cálculo da taxa de conversão, que mostrou que apenas uma porcentagem das visitas dos clientes resulta em transações, é uma métrica importante para entender o desempenho do negócio.

- A identificação dos produtos mais populares destacou quais produtos atraem mais clientes, o que pode ser útil para estratégias de marketing e estoque.

### Comportamento do Cliente

- A segmentação de clientes com base na receita total revelou três grupos distintos, o que sugere que os clientes podem ser categorizados em diferentes níveis de engajamento.

### Previsão de Vendas

- O modelo de regressão linear aplicado para prever as vendas futuras com base nas tendências históricas produziu resultados interessantes. No entanto, a previsão de vendas futuras pode ser afetada por vários fatores não considerados neste modelo, como sazonalidade.

### Sistema de Recomendação

- O sistema de recomendação implementado com sucesso usa um modelo de filtragem colaborativa para fornecer recomendações personalizadas com base no histórico de compras do cliente.

- A adição da coluna "Estimation" aos dados de transações permite que os clientes vejam as classificações estimadas dos produtos que ainda não compraram.

Essas observações refletem o processo de análise dos dados de vendas e a criação do sistema de recomendação. Este projeto serve como uma base para análises mais aprofundadas e aprimoramentos futuros no sistema de recomendação.
