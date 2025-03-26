# Análise de Churn em Telecomunicações

Este projeto apresenta uma análise exploratória de dados (EDA) e criação de modelo preditivo para identificar clientes com risco de churn (cancelamento de serviços) em uma empresa de telecomunicações.

## 📊 Visão Geral

A análise utiliza o dataset Telco Churn da Kaggle, que contém informações sobre clientes, seus serviços contratados, características demográficas e histórico de pagamentos. O projeto foca em entender os fatores que levam ao cancelamento de serviços e criar um modelo preditivo para identificar clientes em risco.

## 🔍 Principais Componentes da Análise

### 1. Carregamento e Limpeza de Dados
- Tratamento de valores inválidos no campo `TotalCharges`
- Conversão de variáveis categóricas para numéricas

### 2. Análise Exploratória
- Estatísticas descritivas
- Distribuição de churn no dataset (26.54% dos clientes cancelaram)
- Análise da distribuição de gastos mensais e totais
- Segmentação por métodos de pagamento
- Análise demográfica (gênero, idade, parceiros, dependentes)

### 3. Insights Principais
- Clientes com parceiros têm taxas de churn significativamente menores
- O tempo de permanência (tenure) é um forte preditor de churn, com risco maior nos primeiros 10-15 meses
- Clientes com dependentes têm menor probabilidade de cancelar (15% vs 31% dos sem dependentes)
- Métodos de pagamento influenciam o comportamento de churn, com "Electronic Check" associado a maiores taxas

### 4. Modelo de Machine Learning
- Random Forest Classifier para prever churn
- Balanceamento do dataset com RandomOverSampler
- Codificação de variáveis categóricas com OrdinalEncoder
- Métricas de avaliação:
  - Precisão: 94% (classe 0), 84% (classe 1)
  - Recall: 82% (classe 0), 95% (classe 1)
  - F1-score: 88% (classe 0), 89% (classe 1)
  - Acurácia geral: 88%

### 5. Análise de ROI
- Implementação do modelo pode gerar economias estimadas em $319,600
- ROI de aproximadamente 219.6% considerando 30% de conversão dos clientes identificados

## 📋 Recomendações para Retenção de Clientes

1. Foco em programas de onboarding para os primeiros 10 meses de relacionamento
2. Implementar pontos de verificação de satisfação especialmente nos primeiros 2 anos
3. Criar programas de fidelidade baseados em tempo de permanência
4. Desenvolver estratégias específicas para clientes sem dependentes ou parceiros
5. Investigar possíveis problemas com pagamentos via "Electronic Check"
6. Segmentar estratégias por perfil familiar e demográfico

## 🛠️ Ferramentas Utilizadas
- Python
- Pandas e NumPy para manipulação de dados
- Matplotlib e Seaborn para visualizações
- Scikit-learn para modelagem preditiva
- Imbalanced-learn para balanceamento de classes

## 🔄 Próximos Passos
- Testar outros algoritmos de machine learning
- Implementar ajuste de hiperparâmetros
- Desenvolver um sistema de pontuação de propensão a churn
- Criar um pipeline automatizado para previsão contínua

---

Este projeto demonstra como a análise de dados e machine learning podem ser aplicados para reduzir o churn e aumentar a retenção de clientes, gerando valor significativo para empresas de telecomunicações.
