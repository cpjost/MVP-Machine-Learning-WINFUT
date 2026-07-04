# Classificação de Operações no WINFUT utilizando Machine Learning

[![Open in Colab][(https://colab.research.google.com/drive/1HAx0aJuSPACW1npf0R5WChOxzUHRM47c#scrollTo=JWDDt3U8MSMy)

---

# Descrição do Projeto

Este projeto foi desenvolvido como parte do MVP da disciplina de Machine Learning da Pós-Graduação em Ciência de Dados e Analytics da PUC-Rio.

O objetivo é desenvolver um modelo supervisionado capaz de classificar operações de compra (Long) no contrato futuro do Índice Bovespa (WINFUT), utilizando exclusivamente informações disponíveis no momento da abertura da operação.

Todo o desenvolvimento foi realizado seguindo boas práticas de Ciência de Dados, incluindo prevenção de Data Leakage, engenharia de atributos, validação temporal, comparação entre diferentes algoritmos e otimização de hiperparâmetros.

---

# Objetivos

- Construir uma variável-alvo baseada em uma estratégia de risco-retorno;
- Realizar análise exploratória dos dados;
- Preparar e transformar o conjunto de dados para modelagem;
- Desenvolver novos atributos (Feature Engineering);
- Comparar diferentes algoritmos de classificação;
- Otimizar hiperparâmetros utilizando GridSearchCV;
- Avaliar o desempenho utilizando métricas apropriadas para problemas de classificação.

---

# Dataset

O conjunto de dados é composto por candles de 5 minutos do contrato futuro do Índice Bovespa (WINFUT).

A base contém aproximadamente:

- 56 mil observações;
- informações OHLC (Open, High, Low e Close);
- Volume;
- Quantidade negociada;
- Data e hora.

Após a engenharia de atributos foram criadas novas variáveis derivadas utilizadas durante o treinamento.

---

# Fluxo do Projeto

```text
Coleta dos Dados
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
Treinamento
        │
        ▼
Comparação dos Modelos
        │
        ▼
GridSearchCV + TimeSeriesSplit
        │
        ▼
Avaliação Final
```

---

# Modelos Avaliados

- Decision Tree
- Random Forest
- XGBoost

---

# Principais Técnicas Utilizadas

- Feature Engineering
- TimeSeriesSplit
- GridSearchCV
- Matriz de Confusão
- Classification Report
- Feature Importance
- Prevenção de Data Leakage

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

```
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
└── LICENSE
```

---

# Principais Resultados

Após a comparação entre os modelos, o XGBoost apresentou o melhor desempenho geral, obtendo os maiores valores de Precision, Recall e F1-Score entre os algoritmos avaliados.

A etapa de otimização utilizando GridSearchCV confirmou que a configuração inicial do modelo já apresentava o melhor desempenho dentre as combinações avaliadas.

---

# Como Executar

Clone o repositório:

```bash
git clone https://github.com/SEU_USUARIO/MVP-Machine-Learning-WINFUT.git
```

Instale as dependências:

```bash
pip install -r requirements.txt
```

Abra o notebook:

```bash
jupyter notebook
```

ou utilize diretamente o botão **Open in Colab** disponível no início desta página.

---

# Autor

**Carlos Peter Jost**

Pós-Graduação em Ciência de Dados e Analytics – PUC-Rio
