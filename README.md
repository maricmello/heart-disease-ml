# Predição de Doença Cardíaca Utilizando Regressão Logística e Técnicas de Pré-processamento de Dados

## Autores
- Mariana Costa de Mello  
- Michelle de Sales Silva  
- Nathan Bernardo Novais  

## Descrição
Este projeto utiliza técnicas de aprendizado de máquina para prever a presença de doença cardíaca com base em dados clínicos do paciente. O objetivo é treinar modelos capazes de identificar pacientes em risco, auxiliando em decisões médicas.

## Dataset
- **Fonte:** [UCI Heart Disease Data](https://www.kaggle.com/datasets/redwankarimsony/heart-disease-data?select=heart_disease_uci.csv)  
- O dataset contém variáveis numéricas e categóricas, algumas com valores ausentes.  
- Pré-processamento incluiu:
  - Imputação de valores ausentes
  - Codificação One-Hot para variáveis categóricas
  - Padronização de atributos numéricos
- Algumas dificuldades encontradas incluíram lidar com valores ausentes e selecionar a codificação adequada para variáveis categóricas.

## Modelos Utilizados
- Regressão Logística (Logistic Regression) com `GridSearchCV` para ajuste de hiperparâmetros
- Pipeline de pré-processamento incluindo `ColumnTransformer` para tratar separadamente atributos numéricos e categóricos

## Resultados
- **Métricas de avaliação do modelo final:**

| Classe         | Precision | Recall | F1-score | Support |
|----------------|----------|--------|----------|--------|
| Sem Doença (0) | 0.86     | 0.78   | 0.82     | 82     |
| Com Doença (1) | 0.84     | 0.90   | 0.87     | 102    |
| **Accuracy**   |          |        | 0.85     | 184    |

- O modelo apresentou equilíbrio entre precision e recall, especialmente para a classe "Com Doença", garantindo boa detecção de pacientes com risco cardiovascular.

## Conclusão e Trabalhos Futuros
- O pré-processamento foi crucial para o desempenho do modelo.  
- Futuras melhorias podem incluir:
  - Avaliar outros algoritmos de classificação como KNN, Random Forest e XGBoost
  - Aplicar técnicas avançadas de engenharia de atributos e seleção de variáveis
  - Testar estratégias de balanceamento para lidar com possíveis desbalanceamentos nas classes
