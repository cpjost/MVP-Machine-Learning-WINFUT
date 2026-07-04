# 📈 Machine Learning para Classificação de Operações no WINFUT

Projeto desenvolvido como MVP da Pós-Graduação em Ciência de Dados e Analytics da PUC-Rio.

O objetivo é construir um modelo de Machine Learning capaz de classificar operações de compra (Long) no contrato futuro do Índice Bovespa (WINFUT), utilizando apenas informações disponíveis no momento da abertura da operação, evitando Data Leakage.

---

# Objetivos

Este projeto busca responder à seguinte pergunta:

> É possível utilizar técnicas de Machine Learning para identificar operações com maior probabilidade de atingir um alvo de lucro antes de atingir o stop loss?

---

# Dataset

- Ativo: WINFUT
- Timeframe: 5 minutos
- Mais de 56 mil observações
- Dados históricos em formato OHLCV

Variáveis principais:

- Abertura
- Máximo
- Mínimo
- Fechamento
- Volume

---

# Fluxo do Projeto

```text
Dados Históricos
        │
        ▼
Análise Exploratória
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
Treinamento dos Modelos
        │
        ▼
GridSearchCV + TimeSeriesSplit
        │
        ▼
Avaliação
```

---

# Modelos Avaliados

- Decision Tree
- Random Forest
- XGBoost

---

# Métricas Utilizadas

- Accuracy
- Precision
- Recall
- F1-Score
- Matriz de Confusão
- Classification Report

---

# Técnicas Utilizadas

- Engenharia de atributos
- Data Leakage Prevention
- TimeSeriesSplit
- GridSearchCV
- Feature Importance

---

# Tecnologias

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-Learn
- XGBoost
- Google Colab

---

# Estrutura do Projeto

```text
.
├── notebooks/
├── data/
├── images/
├── docs/
├── README.md
├── requirements.txt
└── LICENSE
```

---

# Como Executar

```bash
git clone https://github.com/cpjost/MVP-Machine-Learning-WINFUT.git

cd MVP-Machine-Learning-WINFUT

pip install -r requirements.txt

jupyter notebook
```

---

# Principais Resultados

- Comparação entre três algoritmos supervisionados.
- Utilização de validação temporal para evitar Data Leakage.
- Otimização de hiperparâmetros utilizando GridSearchCV.
- O XGBoost apresentou o melhor desempenho geral entre os modelos avaliados.

---

# Melhorias Futuras

- Inclusão de indicadores técnicos (RSI, MACD, ATR, ADX e Bandas de Bollinger).
- Técnicas de balanceamento de classes (SMOTE e ADASYN).
- Otimização Bayesiana.
- Testes com LightGBM e CatBoost.
- Avaliação em outros ativos financeiros.

---

# Autor

**Carlos Peter Jost**

Pós-Graduação em Ciência de Dados e Analytics — PUC-Rio

