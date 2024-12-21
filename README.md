# Modelo de Predição de Diabetes

Este projeto tem como objetivo prever a diabetes com base em várias características de saúde e demográficas. Ele utiliza o conjunto de dados **Diabetes Prediction**, processa os dados e treina um classificador de árvore de decisão. Além disso, o projeto demonstra o impacto do uso de undersampling para lidar com o desbalanceamento das classes no conjunto de dados.

## Etapas do Projeto

### 1. Importação e Exploração dos Dados
- O conjunto de dados é carregado utilizando `pandas.read_csv`.
- A exploração inicial é realizada com funções como `.head()`, `.info()` e `.describe()`.
- A coluna `gender` é mapeada para valores numéricos (`Female` = 0, `Male` = 1, `Other` = 3), e outras colunas necessárias são convertidas para os tipos de dados apropriados.

### 2. Pré-processamento dos Dados
- As colunas com tipo de dado inteiro são convertidas para valores numéricos.
- A coluna `smoking_history` é convertida para o tipo categórico e variáveis dummy são criadas usando `pd.get_dummies()`.

### 3. Separação entre Atributos e Target
- A coluna alvo `diabetes` é separada das colunas de atributos.
- Os dados são divididos entre treino e teste utilizando `train_test_split()`.

### 4. Treinamento do Modelo (Sem Balanceamento)
- Um classificador de árvore de decisão é treinado com o conjunto de dados original.
- O modelo é avaliado utilizando várias métricas de desempenho, como acurácia, precisão, recall, F1 score e ROC AUC.
- A matriz de confusão e a curva ROC são exibidas para avaliar o desempenho do modelo.

### 5. Undersampling para Desbalanceamento de Classes
- O conjunto de dados é reamostrado utilizando a técnica de undersampling `ClusterCentroids` para lidar com o desbalanceamento das classes.
- O classificador de árvore de decisão é re-treinado com os dados reamostrados e as métricas de desempenho são recalculadas.

### 6. Comparação de Desempenho
- As métricas de desempenho são comparadas antes e depois do balanceamento do conjunto de dados, a fim de avaliar o impacto do undersampling.

## Requisitos

Para rodar este projeto, você precisará das seguintes bibliotecas Python:

- `pandas`
- `seaborn`
- `matplotlib`
- `scikit-learn`
- `imblearn`

Você pode instalar as bibliotecas necessárias utilizando o comando `pip install`.
