# 🔍 Detecção de Fraude Bancária com Machine Learning

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML-orange)
![Status](https://img.shields.io/badge/Status-Concluído-green)

## 📌 Sobre o Projeto

Modelo de Machine Learning para detectar transações bancárias fraudulentas
em cartões de crédito, utilizando Random Forest com balanceamento SMOTE.

## 📊 Dataset

- **Fonte:** [Kaggle - Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
- **Registros:** 284.807 transações
- **Features:** 30 (V1-V28 via PCA + Amount + Time)
- **Desbalanceamento:** apenas 0,17% de transações fraudulentas

## 🛠️ Tecnologias Utilizadas

- Python
- Pandas & NumPy
- Scikit-learn
- Imbalanced-learn (SMOTE)
- Matplotlib & Seaborn

## 🤖 Metodologia

1. Análise Exploratória dos Dados (EDA)
2. Pré-processamento e balanceamento com SMOTE
3. Treinamento com Random Forest (150 estimadores)
4. Avaliação com AUC-ROC, Matriz de Confusão e F1-Score
5. Análise de Feature Importance

## 📈 Resultados

| Métrica | Valor |
|--------|-------|
| AUC-ROC | **0.9293** |
| Acurácia Geral | **99,97%** |
| Precisão (Fraude) | **99%** |
| Recall (Fraude) | **72%** |
| F1-Score (Fraude) | **0.83** |

## 🔑 Features Mais Importantes

| Rank | Feature | Importância |
|------|---------|-------------|
| 1 | V14 | ~19% |
| 2 | V10 | ~12% |
| 3 | V17 | ~10% |
| 4 | V4 | ~10% |

## 📁 Estrutura do Projeto

├── Projeto1.ipynb        
└── images/               
    ├── class_distribution.png
    ├── correlation_matrix.png
    ├── media_features.png
    ├── confusion_matrix.png
    ├── roc_curve.png
    └── feature_importance.png
