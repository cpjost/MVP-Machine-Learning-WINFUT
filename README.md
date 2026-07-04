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

Todo o fluxo foi desenvolvido seguindo boas práticas de Ciência de Dados, contemplando:

- Análise Exploratória dos Dados (EDA);
- Engenharia de Atributos (*Feature Engineering*);
- Construção da variável-alvo;
- Prevenção de *Data Leakage*;
- Divisão temporal dos dados;
- Comparação entre diferentes algoritmos;
- Otimização de hiperparâmetros;
- Avaliação completa dos modelos.

---

# Objetivos

- Construir uma variável-alvo baseada em uma estratégia objetiva de risco-retorno;
- Realizar análise exploratória dos dados;
- Preparar o conjunto de dados para modelagem;
- Desenvolver novos atributos (*Feature Engineering*);
- Comparar diferentes algoritmos de classificação;
- Otimizar hiperparâmetros utilizando **GridSearchCV**;
- Avaliar os modelos utilizando métricas apropriadas para classificação.

---

# Dataset

| Informação | Valor |
|------------|-------|
| Ativo | WINFUT |
| Frequência | Candles de 5 minutos |
| Registros após preparação | **56.356** |
| Variáveis preditoras | **12** |
| Variável-alvo | Target |
| Tipo do problema | Classificação Binária |

---

# Fluxo do Projeto

```text
Dados Históricos
        │
        ▼
Análise Exploratória (EDA)
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
Divisão Temporal
        │
        ▼
Baseline (Dummy Classifier)
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

| Modelo | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|---------|---------:|----------:|--------:|---------:|--------:|
| Baseline (Dummy) | 0.7444 | 0.0000 | 0.0000 | 0.0000 | 0.5000 |
| Decision Tree | 0.7120 | 0.2675 | 0.0729 | 0.1146 | 0.5022 |
| Random Forest | 0.7144 | 0.2599 | 0.0635 | 0.1021 | 0.5123 |
| XGBoost | 0.6944 | 0.2700 | 0.1149 | 0.1612 | 0.5058 |
| **XGBoost Otimizado** | **0.3992** | **0.2542** | **0.6984** | **0.3727** | **0.4991** |

---

# Principais Técnicas Utilizadas

- Análise Exploratória dos Dados (EDA)
- Feature Engineering
- Construção da Variável-Alvo
- Divisão Temporal dos Dados
- TimeSeriesSplit
- GridSearchCV
- Baseline (Dummy Classifier)
- Decision Tree
- Random Forest
- XGBoost
- Matriz de Confusão
- Classification Report
- Feature Importance
- Prevenção de Data Leakage

---

# Principais Resultados

- Foram comparados cinco modelos, incluindo um modelo **Baseline (Dummy Classifier)**.
- O **XGBoost Otimizado** apresentou o melhor **F1-Score (0.3727)** entre todos os modelos avaliados.
- A etapa de otimização elevou significativamente o **Recall** da classe positiva para **0.6984**, aumentando a capacidade de identificar operações vencedoras.
- A utilização do **TimeSeriesSplit** garantiu uma validação compatível com séries temporais, preservando a ordem cronológica dos dados.
- Todo o processo foi conduzido evitando **Data Leakage**, utilizando apenas informações disponíveis no momento da abertura de cada operação.

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
│
├── README.md
├── requirements.txt
├── LICENSE
└── .gitignore
```

---

# Como Executar

 utilize diretamente o botão **Open in Colab** disponível no início desta página.

---

# Trabalhos Futuros

- Incorporar indicadores técnicos adicionais (RSI, MACD, ATR, ADX e Bandas de Bollinger);
- Avaliar técnicas de balanceamento das classes (SMOTE, ADASYN e ajuste de pesos);
- Expandir a busca de hiperparâmetros utilizando Random Search e Bayesian Optimization;
- Comparar o desempenho com algoritmos como LightGBM, CatBoost e Redes Neurais;
- Avaliar o modelo em diferentes ativos financeiros e períodos históricos para verificar sua capacidade de generalização.

---

# Autor

**Carlos Peter Jost**

Engenheiro de Produção

Pós-Graduando em Ciência de Dados e Analytics — PUC-Rio

GitHub: https://github.com/CarlosPeterJost
