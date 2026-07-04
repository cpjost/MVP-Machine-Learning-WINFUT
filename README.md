# MVP de Machine Learning — Previsão de Trades no WINFUT

Este projeto apresenta um MVP de Machine Learning aplicado ao mercado financeiro, com foco na classificação de operações no contrato futuro do Ibovespa (WINFUT).

O objetivo é prever se uma operação hipotética de compra atingiria primeiro o Take Profit ou o Stop Loss, utilizando dados históricos de candles, engenharia de atributos e modelos supervisionados de classificação.

## Objetivo do Projeto

Construir um pipeline reproduzível de Machine Learning capaz de:

- carregar dados históricos do WINFUT;
- preparar e limpar os dados;
- criar uma variável-alvo baseada em regra operacional;
- desenvolver atributos técnicos;
- treinar modelos de classificação;
- comparar os resultados;
- discutir limitações e próximos passos.

## Problema de Machine Learning

Tipo de problema:

**Classificação binária supervisionada**

Variável-alvo:

- `1`: Take Profit atingido antes do Stop Loss;
- `0`: Stop Loss atingido antes do Take Profit.

Regra operacional utilizada:

- Entrada: fechamento do candle atual;
- Take Profit: 450 pontos;
- Stop Loss: 150 pontos;
- Horizonte máximo: 12 candles de 5 minutos.

## Dataset

A base utilizada contém candles de 5 minutos do WINFUT, com as seguintes variáveis principais:

- Data;
- Hora;
- Abertura;
- Máximo;
- Mínimo;
- Fechamento;
- Volume;
- Quantidade de contratos.

O arquivo está disponível em:

```text
data/WINFUT_F_0_5min.csv
