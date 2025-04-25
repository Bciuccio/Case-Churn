Resumo do Tratamento de Dados no Projeto de Churn Bancário
Este projeto tem como objetivo prever a rotatividade de clientes (churn) em um banco, utilizando técnicas de análise de dados e machine learning. O tratamento dos dados segue um pipeline estruturado para garantir que o modelo final seja preciso e confiável.

1. Objetivo Principal
Desenvolver um modelo preditivo para identificar clientes com alta probabilidade de deixar o banco (churn), permitindo ações preventivas de retenção.

2. Principais Etapas do Tratamento de Dados
📌 1. Carregamento e Exploração Inicial
Dados utilizados:

BankChurners.csv (informações dos clientes)

metadados.xlsx (descrição das variáveis)

Análise inicial:

Verificação do tamanho do dataset (shape)

Tipos de dados (info())

Estatísticas descritivas (describe())

📌 2. Limpeza e Tratamento
Remoção de colunas irrelevantes:

CLIENTNUM (ID único do cliente, não útil para modelagem)

Colunas relacionadas a modelos anteriores (Naive_Bayes_*) para evitar vazamento de dados

Verificação de dados duplicados e nulos

duplicated().sum() para checar duplicatas

isnull().sum() para identificar valores ausentes

📌 3. Análise Exploratória (EDA)
Visualizações para entender padrões de churn:

Distribuição de churn por gênero, escolaridade, tipo de cartão

Análise de idade, tempo como cliente e gastos mensais

Uso de gráficos (countplot, histplot, boxplot, scatterplot)

📌 4. Pré-processamento para Machine Learning
Codificação de variáveis categóricas (LabelEncoder)

Transforma textos (ex: "M" / "F") em números para o modelo

Balanceamento de classes com SMOTE

Gera dados sintéticos da classe minoritária (clientes que deixaram o banco) para evitar viés no modelo

Normalização/Padronização (MinMaxScaler e StandardScaler)

Reduz impacto de escalas diferentes (ex: idade vs. saldo bancário)

📌 5. Modelagem e Avaliação
Teste de múltiplos algoritmos:

Random Forest

Regressão Logística

Árvore de Decisão

SVM

Métricas de avaliação:

AUC-ROC (área sob a curva)

Precision, Recall, F1-Score

Matriz de confusão

Otimização com GridSearchCV

Ajuste de hiperparâmetros do melhor modelo (Random Forest)

📌 6. Interpretação e Deploy
Análise de importância das variáveis

Quais fatores mais impactam o churn? (ex: tempo como cliente, utilização do cartão)

Salvamento do modelo (joblib) para uso futuro

3. Conclusão
Este projeto segue um fluxo completo de Ciência de Dados, desde a limpeza e análise exploratória até a construção e otimização de modelos preditivos. O tratamento de dados foi crucial para:
✅ Garantir qualidade nos dados (remoção de ruídos, correção de desbalanceamento)
✅ Melhorar a performance do modelo (escalonamento, codificação)
✅ Permitir interpretação clara (identificar fatores de churn)

O resultado é um modelo capaz de prever clientes em risco de churn, ajudando o banco a agir preventivamente e reduzir perdas. 🚀
