# 🔍 Detecção de Fraudes com Machine Learning - Projeto DIO

## 📖 Sobre o Projeto

Este projeto tem como objetivo desenvolver e avaliar modelos de **Machine Learning** para detecção de transações fraudulentas.

O estudo contempla desde a análise exploratória dos dados até a interpretabilidade do modelo, utilizando técnicas modernas de classificação supervisionada, tratamento de dados desbalanceados e explicabilidade baseada em SHAP.

---

## 🎯 Objetivos

- Identificar transações fraudulentas com alta capacidade de detecção.
- Comparar diferentes algoritmos de Machine Learning.
- Avaliar o impacto do desbalanceamento das classes.
- Aplicar técnicas de Feature Engineering.
- Interpretar as previsões dos modelos utilizando SHAP.

---

## 📊 Dataset

O projeto utiliza o conjunto de dados **Credit Card Fraud Detection**, amplamente utilizado em estudos acadêmicos e pesquisas na área de detecção de fraudes.

Características do dataset:

- Transações reais de cartões de crédito.
- Classes altamente desbalanceadas.
- Variáveis anonimizadas através de PCA (`V1` até `V28`).
- Variável alvo:
  - `Class = 0` → Transação legítima
  - `Class = 1` → Fraude

---

## ⚙️ Etapas Desenvolvidas

### 1️⃣ Análise Exploratória dos Dados (EDA)

- Verificação da estrutura dos dados.
- Distribuição das classes.
- Análise de valores ausentes.
- Estatísticas descritivas.

### 2️⃣ Feature Engineering

Foram criadas novas variáveis para auxiliar os modelos:

- `Amount_log`
  - Transformação logarítmica da variável monetária.
  - Redução da assimetria dos dados.

- `Amount_scaled`
  - Padronização utilizando StandardScaler.

- `High_Amount`
  - Identificação de transações com valores acima do percentil 95.

### 3️⃣ Tratamento de Dados Desbalanceados

Foram avaliadas diferentes abordagens:

- Random Undersampling
- SMOTE (Synthetic Minority Over-sampling Technique)
- Ajuste de pesos das classes

### 4️⃣ Modelagem

Os seguintes algoritmos foram avaliados:

- Logistic Regression
- Random Forest
- XGBoost

### 5️⃣ Otimização de Hiperparâmetros

Foi utilizado:

- RandomizedSearchCV
- Validação Cruzada Estratificada (StratifiedKFold)

### 6️⃣ Avaliação dos Modelos

Métricas utilizadas:

- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC
- Precision-Recall Curve

### 7️⃣ Interpretabilidade

Aplicação da biblioteca SHAP para:

- Importância global das variáveis
- Impacto das variáveis nas previsões
- Explicação do comportamento do modelo

---

## 🛠️ Tecnologias Utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-Learn
- XGBoost
- SHAP
- Imbalanced-Learn

---

## 📂 Estrutura do Projeto

.
├── Projeto1-Analise de dados.ipynb
├── README.md
└── requirements.txt

---

## 🚀 Como Executar

### Clonar o repositório

```bash
git clone https://github.com/seu-usuario/seu-repositorio.git
```

### Instalar dependências

```bash
pip install -r requirements.txt
```

### Executar o notebook

```bash
jupyter notebook Projeto1.ipynb
```

ou

```bash
jupyter lab
```

---

## 📈 Principais Resultados

O projeto demonstrou que modelos baseados em árvores de decisão, especialmente o **XGBoost**, apresentam excelente desempenho na detecção de fraudes, principalmente quando combinados com técnicas adequadas para tratamento do desbalanceamento das classes.

Além da performance preditiva, a utilização de SHAP permitiu compreender quais variáveis exercem maior influência nas decisões do modelo.

---

## 👨‍💻 Autor

**Peterson Lima**

Projeto desenvolvido para fins acadêmicos na disciplina de Machine Learning e Ciência de Dados.
