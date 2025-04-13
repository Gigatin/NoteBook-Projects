# Previsão de Preços de Imóveis

## Esse projeto é baseado em um desafio do Kaggle!

Link para o desafio: kaggle.com/competitions/house-prices-advanced-regression-techniques/overview


## Objetivo do Projeto
O principal objetivo deste projeto é desenvolver modelos preditivos para estimar o valor de venda de imóveis (variável `SalePrice`). Para isso, foi criado um pipeline que realiza:
- O pré-processamento completo dos dados;
- O tratamento de valores ausentes e a codificação de variáveis categóricas;
- A separação dos dados em conjuntos de treinamento e teste;
- O treinamento e comparação de diversos modelos de regressão (como Regressão Linear, XGBoost e Random Forest);
- A geração do arquivo final de submissão das predições.

## Origem dos Dados
O projeto utiliza o dataset "House Prices", que é composto por dois arquivos principais:
- **train.csv**: contém os dados de treinamento com a variável alvo `SalePrice`.
- **test.csv**: contém os dados de teste, nos quais as predições serão realizadas.

Além destes, o dataset inclui documentação detalhada (no arquivo `data_description.txt`) e um exemplo de submissão (`sample_submission.csv`).

## Etapas Realizadas

### 1. Carregamento e Integração dos Dados
- Os arquivos de treinamento e teste foram lidos utilizando a biblioteca *Pandas*.
- Foi realizada a padronização entre os conjuntos (como a criação da coluna `SalePrice` no conjunto de teste, se necessário) e, em seguida, ambos os datasets foram concatenados para um tratamento unificado.

### 2. Tratamento de Dados Ausentes e Codificação
- Identificação das colunas com valores faltantes.
- Remoção de colunas com muitos valores ausentes.
- Preenchimento dos valores nulos:
  - Em variáveis categóricas, os nulos foram substituídos pela string `"null"`.
  - Em variáveis numéricas, foi aplicada a imputação por moda (para atributos discretos) ou média (para atributos contínuos).
- Aplicação do One-Hot Encoding para transformar as variáveis categóricas em dados numéricos.
- Eliminação das colunas originais do tipo *object*, mantendo apenas os dados tratados.

### 3. Separação dos Dados para Treinamento e Teste
- A partir do DataFrame final, os dados foram divididos em duas partes:
  - **Treinamento**: contendo as amostras de `train.csv` com a variável `SalePrice`.
  - **Teste**: contendo as amostras de `test.csv` (com a coluna `SalePrice` removida) para as quais serão feitas as predições.

### 4. Modelagem e Avaliação
Foram comparados três modelos de regressão:
- **Regressão Linear**: Utilizada como baseline.
- **XGBoost Regressor**: Apresentou o melhor desempenho, capturando relações não lineares nos dados.
- **Random Forest Regressor**: Embora robusto, apresentou desempenho inferior ao XGBoost no conjunto testado.
  
A performance de cada modelo foi avaliada com base no *Mean Squared Error (MSE)*, comparando os valores reais com as predições.

### 5. Geração do Arquivo Final de Submissão
- Utilizando o modelo com melhor desempenho (XGBoost), foram geradas as predições para os dados de teste.
- Um DataFrame final foi criado contendo o `Id` (mantido dos dados originais) e a predição de `SalePrice` para cada amostra.
- Esse DataFrame foi exportado para um arquivo `output.csv`, pronto para submissão.

## Conclusão
O pipeline desenvolvido demonstra um fluxo completo, desde o pré-processamento dos dados até a geração do arquivo final de submissão. A abordagem de comparar diferentes modelos permitiu identificar que o **XGBoost Regressor** foi o mais eficiente na redução do erro das predições. Este projeto está estruturado para facilitar futuras otimizações, tanto na seleção e engenharia de features quanto no ajuste fino dos hiperparâmetros dos modelos.

Sinta-se à vontade para explorar, modificar e aprimorar este projeto. Em caso de dúvidas ou sugestões, por favor, abra uma *issue* ou entre em contato!
