# 🔍 Detecção de Fraude Bancária com Machine Learning

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML-orange)
![Status](https://img.shields.io/badge/Status-Concluído-green)

## 📌 Problemática
Identificar transações bancárias fraudulentas é um dos maiores desafios do setor financeiro.  
O volume massivo de transações e o extremo desbalanceamento entre classes (fraude vs. legítima) tornam o problema complexo para modelos tradicionais. Este projeto aplica análise de dados e Machine Learning com técnicas de balanceamento para detectar fraudes em cartões de crédito com alta precisão.

## 📦 Coleta de Dados
- **Fonte:** Kaggle — Credit Card Fraud Detection
- **Arquivo:** `creditcard.csv`
- **Registros:** 284.807 transações | **Variáveis:** 30 preditoras + 1 target
- **Valores nulos:** Nenhum | **Duplicatas:** Nenhuma
- **Desbalanceamento:** apenas **0,17%** das transações são fraudulentas

| Variável | Descrição |
|---|---|
| V1 – V28 | Componentes principais obtidos por PCA (dados anonimizados) |
| Amount | Valor da transação |
| Time | Tempo decorrido desde a primeira transação |
| **Class** | 🎯 0 = legítima, 1 = fraude |

## 🛠️ Tecnologias Utilizadas
- **Python**
- **Pandas** e **NumPy**
- **Scikit-learn**
- **Imbalanced-learn (SMOTE)**
- **Matplotlib** e **Seaborn**

## 🔍 Análise Exploratória
- O dataset é extremamente desbalanceado, com predominância quase total de transações legítimas
- As variáveis `V1` a `V28` já passaram por transformação PCA, preservando anonimização
- `Amount` e `Time` foram escaladas para melhorar o desempenho do modelo
- Algumas variáveis, como **V14**, **V10**, **V17** e **V4**, mostraram maior relevância para separar fraudes de transações legítimas

![Distribuição de Classes](images/class_distribution.jpg)
![Correlação entre Variáveis](images/correlation_matrix.jpg)
![Média das Features por Classe](images/media_features.jpg)

## 🤖 Modelagem

| Técnica | Resultado |
|---|---|
| Balanceamento com SMOTE | Reequilibrou a classe minoritária no treino |
| Random Forest | Modelo principal utilizado |
| Avaliação ROC | **AUC = 0.9293** |
| Matriz de Confusão | 56.650 verdadeiros negativos e 68 verdadeiros positivos |

| Métrica | Resultado |
|---|---|
| AUC-ROC | **0.9293** |
| Acurácia | **99,97%** |
| Precisão (fraude) | **99%** |
| Recall (fraude) | **72%** |
| F1-Score | **0.83** |

![Distribuição de Classes](class_distribution-4.jpg)
![Correlação entre Variáveis](correlation_matrix-6.jpg)
![Média das Features por Classe](media_features-8.jpg)
![Matriz de Confusão](confusion_matrix-5.jpg)
![Curva ROC](roc_curve-9.jpg)
![Feature Importance](feature_importance-7.jpg)

## ✅ Conclusões
- O modelo **Random Forest com SMOTE** apresentou ótimo desempenho geral, com **AUC de 0.9293**
- A detecção de fraudes foi altamente precisa, embora ainda existam falsos negativos
- A variável **V14** foi a mais importante para a classificação, seguida por **V10**, **V17** e **V4**
- O projeto mostra como técnicas de balanceamento e modelos de ensemble podem ser eficazes em cenários altamente desbalanceados
- **Próximos passos:** testar XGBoost/LightGBM, ajustar threshold de decisão e otimizar hiperparâmetros

---
> Projeto desenvolvido por **Henrique Ximenes** — Portfólio de Ciência de Dados
