# Classificação de Operações no Contrato Futuro do Índice Bovespa (WINFUT) utilizando Machine Learning

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/cpjost/MVP-Machine-Learning-WINFUT/blob/main/notebooks/MVP_ML_WINFUT.ipynb)

![Python](https://img.shields.io/badge/Python-3.11-blue)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Machine%20Learning-orange)
![XGBoost](https://img.shields.io/badge/XGBoost-Gradient%20Boosting-green)
![Google Colab](https://img.shields.io/badge/Google-Colab-F9AB00)
![PUC-Rio](https://img.shields.io/badge/PUC--Rio-MVP-blueviolet)

---

# Descrição do Projeto

Este projeto foi desenvolvido como parte do **MVP da disciplina de Machine Learning** da Pós-Graduação em **Ciência de Dados e Analytics da PUC-Rio**.

O objetivo deste trabalho é desenvolver e comparar modelos supervisionados de Machine Learning capazes de classificar operações de compra (**Long**) no contrato futuro do Índice Bovespa (**WINFUT**), utilizando exclusivamente informações disponíveis no momento da abertura da operação.

Foram avaliados três algoritmos de classificação (**Decision Tree, Random Forest e XGBoost**), empregando validação temporal com **TimeSeriesSplit** e otimização de hiperparâmetros utilizando **GridSearchCV**, respeitando a natureza cronológica da série temporal e prevenindo vazamento de informações (*Data Leakage*).

Todo o desenvolvimento foi realizado seguindo boas práticas de Ciência de Dados, contemplando análise exploratória, engenharia de atributos, validação temporal, comparação entre modelos e avaliação completa dos resultados.

---

# Objetivos

- Construir uma variável-alvo baseada em uma estratégia objetiva de risco-retorno;
- Realizar análise exploratória dos dados;
- Preparar e transformar o conjunto de dados para modelagem;
- Desenvolver novos atributos (*Feature Engineering*);
- Comparar diferentes algoritmos de classificação;
- Otimizar hiperparâmetros utilizando **GridSearchCV**;
- Avaliar o desempenho utilizando métricas apropriadas para problemas de classificação;
- Desenvolver um fluxo completo de Machine Learning aplicado ao mercado financeiro.

---

# Dataset

| Informação | Valor |
|------------|-------|
| Ativo | WINFUT |
| Frequência | Candles de 5 minutos |
| Registros | 56.338 |
| Variáveis preditoras | 12 |
| Variável-alvo | Target (Sucesso / Insucesso da operação) |
| Tipo do problema | Classificação Binária |

---

# Fluxo do Projeto

```text
Dados Históricos
        │
        ▼
Análise Exploratória dos Dados (EDA)
        │
        ▼
Preparação dos Dados
        │
        ▼
Engenharia de Atributos
        │
        ▼
Construção da Variável-Alvo
        │
        ▼
Divisão Temporal dos Dados
        │
        ▼
Decision Tree
        │
        ▼
Random Forest
        │
        ▼
XGBoost
        │
        ▼
GridSearchCV + TimeSeriesSplit
        │
        ▼
Avaliação dos Modelos
```

---

# Modelos Avaliados

| Modelo | Accuracy | Precision | Recall | F1-Score |
|---------|---------:|----------:|--------:|---------:|
| Decision Tree | 0.7104 | 0.2618 | 0.0729 | 0.1140 |
| Random Forest | 0.7141 | 0.2511 | 0.0597 | 0.0965 |
| **XGBoost** | **0.7126** | **0.2862** | **0.0830** | **0.1286** |

---

# Principais Técnicas Utilizadas

- Análise Exploratória dos Dados (EDA)
- Feature Engineering
- Construção da Variável-Alvo
- Divisão Temporal dos Dados
- TimeSeriesSplit
- GridSearchCV
- Decision Tree
- Random Forest
- XGBoost
- Matriz de Confusão
- Classification Report
- Feature Importance
- Prevenção de Data Leakage

---

# Principais Resultados

- Foram comparados três algoritmos supervisionados de classificação.
- O **XGBoost** apresentou o melhor desempenho geral.
- A utilização do **TimeSeriesSplit** preservou a ordem cronológica dos dados durante a validação.
- A otimização utilizando **GridSearchCV** confirmou que os hiperparâmetros inicialmente definidos já representavam a melhor configuração dentre as combinações avaliadas.
- As variáveis **Máximo**, **Mínimo**, **Fechamento**, **MM9** e **MM21** foram as mais relevantes para a classificação das operações.

---

# Principais Bibliotecas

- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- xgboost

---

# Tecnologias

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
- XGBoost
- Google Colab

---

# Estrutura do Repositório

```text
MVP-Machine-Learning-WINFUT/
│
├── notebooks/
│   └── MVP_ML_WINFUT.ipynb
│
├── data/
│   └── WINFUT_F_02_5min.csv
│
├── images/
│   ├── comparacao_modelos.png
│   ├── importancia_variaveis.png
│   └── matriz_confusao_xgboost.png
│
├── README.md
├── requirements.txt
├── LICENSE
└── .gitignore
```

---

# Trabalhos Futuros

- Incorporar indicadores técnicos adicionais (RSI, MACD, ATR, ADX e Bandas de Bollinger);
- Investigar técnicas de balanceamento das classes (SMOTE, ADASYN e ajuste de pesos);
- Ampliar a busca de hiperparâmetros utilizando Random Search e Bayesian Optimization;
- Comparar o desempenho com algoritmos como LightGBM, CatBoost e Redes Neurais;
- Avaliar o modelo em diferentes ativos financeiros e períodos históricos.

---

# Autor

**Carlos Peter Jost**


