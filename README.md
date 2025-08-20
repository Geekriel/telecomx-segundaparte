# Telecom X - Parte 2: Previsão de Churn

## O propósito da análise
O objetivo principal desta análise é **prever a evasão de clientes (Churn)** da Telecom X, utilizando variáveis relevantes extraídas do dataset. Com essa previsão, a empresa poderá identificar clientes em risco e tomar ações para melhorar a retenção.

---

## Estrutura do projeto e organização dos arquivos
- `telecomx_predicao.ipynb` → Notebook principal com todo o fluxo da análise e modelagem preditiva.
- `telecomx_tratado.csv` → Dataset tratado da Parte 1, pronto para ser utilizado na modelagem.
- `visualizacoes/` → Pasta opcional para armazenar gráficos e visualizações geradas durante a análise.

---

## Preparação dos dados
1. **Classificação das variáveis**
   - Categóricas: `gender`, `Partner`, `Dependents`, `Contract`, `PaymentMethod`, `PaperlessBilling`.
   - Numéricas: `tenure`, `Charges.Monthly`, `Charges.Total`, `SeniorCitizen`.

2. **Normalização e codificação**
   - Variáveis numéricas foram convertidas para tipo `float` ou `int`.
   - Valores nulos foram preenchidos com 0.
   - Variáveis categóricas foram codificadas usando `LabelEncoder` quando necessário.

3. **Separação treino/teste**
   - Conjunto de treino: 80%
   - Conjunto de teste: 20%
   - Escalonamento das variáveis numéricas com `StandardScaler`.

4. **Justificativas da modelagem**
   - Escolha do **Random Forest** por ser robusto a outliers e lidar bem com dados categóricos e numéricos.
   - Divisão treino/teste para avaliar a performance do modelo em dados não vistos.
   - Escalonamento das variáveis numéricas para melhorar o desempenho de algoritmos sensíveis a escala.

---

## Exemplos de gráficos e insights da análise exploratória (EDA)
- **Distribuição de Churn**: mostra a proporção de clientes que saíram.
- **Churn por tipo de contrato**: clientes com contratos curtos apresentam maior risco de evasão.
- **Boxplot de gastos totais**: clientes com menor gasto tendem a abandonar mais.
- **Mapa de correlação**: evidencia relações entre `tenure`, `Charges.Total` e `Charges.Monthly`.

---

## Instruções para executar o notebook
1. Clonar o repositório ou baixar os arquivos.
2. Instalar as bibliotecas necessárias (caso ainda não tenha):
   ```bash
   pip install pandas seaborn matplotlib scikit-learn
