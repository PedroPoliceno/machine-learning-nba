# Previsão de Desempenho na NBA com Machine Learning

Este projeto consiste no desenvolvimento de um modelo preditivo de Aprendizado de Máquina (Machine Learning) em Python para estimar o desempenho de jogadores de basquete (medido através de métricas como *WinShares*), utilizando dados históricos de estatísticas de atletas.

## Tecnologias Utilizadas

O projeto foi desenvolvido em ambiente Jupyter Notebook utilizando as seguintes bibliotecas da linguagem Python:
* **Python** (versão 3.x)
* **Pandas** / **NumPy** para manipulação, limpeza e análise exploratória de dados.
* **Scikit-Learn** (`sklearn`) para a construção e avaliação do modelo de Machine Learning.

## Etapas do Projeto

1. **Carregamento e Limpeza dos Dados:**
   * Importação da base de dados através do `pandas`.
   * Identificação e tratamento de valores nulos (`isnull().sum()`) para garantir a integridade do dataset.

2. **Engenharia de Atributos (Feature Engineering):**
   * Seleção das variáveis estatísticas mais relevantes utilizando o método `SelectKBest` em conjunto com a função de pontuação `f_regression` para otimizar o poder preditivo do modelo.

3. **Divisão dos Dados:**
   * Separação do conjunto de dados entre treino e teste utilizando `train_test_split`, prevenindo o vazamento de dados (*data leakage*).

4. **Modelagem Preditiva:**
   * Treinamento de um modelo de regressão baseado em árvores de decisão avançadas: **`RandomForestRegressor`**.

## Estrutura do Repositório

```text
├── atividade_somativa.ipynb  # Notebook principal contendo todo o código e análises
├── nba_stats.csv             # Base de dados utilizada
└── README.md                 # Documentação do projeto
