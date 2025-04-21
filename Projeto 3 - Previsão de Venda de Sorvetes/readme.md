# Previsão de Vendas de Sorvete com XGBoost

##  Objetivo
Desenvolver um modelo de machine learning que permita prever a quantidade de vendas de sorvete com base na temperatura do dia. O objetivo é otimizar a produção, evitar desperdícios e garantir estoque suficiente, antecipando a demanda conforme variações de temperatura.

---

##  Etapas do Projeto

### 1. Geração de Dados

Criamos um conjunto de dados sintético com 100 registros contendo:
- `Data` (data do registro)
- `Temperatura (°C)` (temperatura do dia)
- `Vendas de Sorvete` (quantidade vendida, ajustada proporcionalmente à temperatura com elementos de variabilidade aleatória)

A lógica assume que quanto maior a temperatura, maior tende a ser o volume de vendas de sorvete.

---

### 2. Pré-processamento

- Os dados foram carregados em um `DataFrame` pandas.
- A coluna `Data` foi removida, uma vez que não possui influência direta sobre as vendas no modelo atual.
- As variáveis foram separadas:
  - `X`: Temperatura
  - `y`: Vendas

Os dados foram divididos em **treinamento** (80%) e **teste** (20%) usando `train_test_split` para validação do modelo.

---

### 3. Criação e Treinamento do Modelo

Foi utilizado o algoritmo **XGBoost (XGBRegressor)**, uma das técnicas mais robustas de aprendizado supervisionado para tarefas de regressão e classificação.

O modelo foi treinado com os seguintes parâmetros:
- `n_estimators=100`
- `learning_rate=0.1`
- `random_state=42`

O XGBoost foi escolhido pela sua alta capacidade de generalização e excelente performance em conjuntos de dados com relação não linear.

---

### 4. Avaliação do Modelo

Utilizamos métricas de **regressão** para avaliar o modelo:

- `MAE` (Mean Absolute Error): erro absoluto médio.
- `RMSE` (Root Mean Squared Error): raiz do erro quadrático médio.
- `R²` (R-squared): mede o quão bem o modelo explica a variabilidade dos dados (quanto mais próximo de 1, melhor).

Essas métricas foram calculadas comparando as previsões geradas pelo modelo (`y_pred`) com os dados reais de teste (`y_test`).

---

### 5. Previsão com Temperatura Real

Para simular um cenário real, o código permite definir uma temperatura prevista ou real e o modelo retorna uma estimativa da quantidade de vendas:

```python
entrada = pd.DataFrame({'Temperatura (°C)': [temperatura_futura]})
previsao = modelo.predict(entrada)
```

---

##  Resultados Esperados
- Prever a quantidade de sorvetes que serão vendidos com base na temperatura do dia.
- Melhorar a eficiência da produção, reduzindo perdas e evitando falta de estoque.
- Automatizar a tomada de decisões baseando-se em dados climáticos reais.

---

##  Melhorias Futuras
- Integração com APIs meteorológicas para obter a temperatura em tempo real.
- Adição de variáveis como dia da semana, eventos, e sazonalidade para aumentar a precisão.
- Salvamento automático das previsões em banco de dados ou relatórios.

---

##  Conclusão
Esse projeto demonstra como dados climáticos simples podem ser utilizados para prever demanda de produtos sensíveis à temperatura (como sorvetes) e, com isso, otimizar a cadeia de produção e minimizar desperdícios.


