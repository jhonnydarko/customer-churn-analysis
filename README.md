# IBM Customer Churn Analysis

### Dashboard Overview

![Dashboard Overview](images/dashboard_overview.png)

## Objetivo

Analisar o churn (cancelamento) de clientes da Telco para identificar padrões de risco, fatores de retenção e insights estratégicos para tomada de decisão.

O notebook inclui:

- Análise exploratória de dados (EDA)
- Limpeza e tratamento de dados
- Taxa de churn por variáveis numéricas e categóricas
- Dashboard com KPIs e gráficos
- Interpretação de insights de negócio

## Ferramentas utilizadas

    Python
    Jupyter Notebook
    Pandas
    Matplotlib
    Git

## Estrutura do projeto

    customer-churn-analysis/
    │
    ├── data/
    │ └── Telco_customer_churn.xlsx
    ├── notebooks/
    │ └── churn_analysis.ipynb
    ├── src/ # funções Python opcionais
    │ └── utils.py
    ├── requirements.txt
    ├── README.md
    └── .gitignore

## Como executar

1. Clonar o repositório:

    git clone https://github.com/jhonnydarko/customer-churn-analysis.git
    cd customer-churn-analysis

## Criar e ativar ambiente virtual:

    python -m venv venv
    source venv/Scripts/activate   # Windows + bash

## Instalar dependências:

    pip install -r requirements.txt

## Abrir notebook:

    jupyter notebook notebooks/churn_analysis.ipynb


## Principais Insights

1. Tempo de Permanência (Tenure Months)

    Correlação negativa com churn: -0.352
    Clientes novos têm risco muito maior de cancelar
    Estratégia: priorizar retenção de clientes recém-contratados

2. Tipo de Contrato (Contract)

    Month-to-month: 42,7% de churn
    One year: 11,3%
    Two year: 2,8%

Insight: contratos mensais são os “maiores ofensores” → foco de campanhas de fidelização

3. Cobranças Mensais (Monthly Charges)

    Correlação positiva: 0.193
    Clientes com valores altos tendem a cancelar mais
    Estratégia: analisar planos de preço ou benefícios diferenciados

4. Total Charges

    Correlação negativa: -0.199
    Clientes com histórico de faturamento maior tendem a permanecer
    Insight: fidelização de clientes antigos é importante

5. Serviços Adicionais

    Tech Support, Streaming TV/Movies, Paperless Billing mostram pequenas diferenças

Insight: serviços podem atuar como fatores de retenção ou risco

## Dashboard

O notebook contém um dashboard visual que combina:

    1. KPIs principais: total de clientes, total de churn, taxa média, clientes Month-to-month
    2. Gráficos de barras: churn por contrato, método de pagamento, tipo de internet
    3. Linha temporal: churn vs tempo de permanência

O dashboard permite rapidamente identificar os clientes de maior risco e fatores que influenciam o churn.


## Documento de Requisitos – Análise de Churn IBM

**Projeto:** Análise de Churn de Clientes

**Objetivo do Projeto:**
A IBM solicita uma análise detalhada da base de dados de clientes com o objetivo de entender os fatores que levam ao churn (cancelamento de serviço) e propor ações para mitigar a perda de clientes.

---

### 1. Escopo

* Analisar o histórico de clientes, identificando padrões e variáveis que influenciam o churn.
* Identificar segmentos de clientes mais propensos ao churn.
* Desenvolver insights acionáveis para reduzir a taxa de churn.
* Gerar relatórios, dashboards e visualizações que comuniquem os resultados de forma clara.

### 2. Base de Dados

* **Fonte:** IBM Telco Customer Churn Dataset.
* **Formato:** CSV.
* **Colunas principais:**

  * `customerID`: Identificador do cliente
  * `gender`: Gênero do cliente
  * `SeniorCitizen`: Indica se é idoso
  * `Partner`: Cliente possui parceiro
  * `Dependents`: Cliente possui dependentes
  * `tenure`: Tempo de contrato
  * `PhoneService`, `MultipleLines`: Serviços de telefonia
  * `InternetService`, `OnlineSecurity`, `OnlineBackup`, `DeviceProtection`, `TechSupport`, `StreamingTV`, `StreamingMovies`: Serviços de internet e adicionais
  * `Contract`, `PaperlessBilling`, `PaymentMethod`: Contrato e método de pagamento
  * `MonthlyCharges`, `TotalCharges`: Valores cobrados
  * `Churn`: Indica se o cliente cancelou o serviço (Sim/Não)

### 3. Requisitos Funcionais

1. **Análise exploratória de dados (EDA):**

   * Estatísticas descritivas.
   * Distribuição de variáveis categóricas e contínuas.
   * Identificação de valores ausentes e inconsistentes.

2. **Visualização de dados:**

   * Gráficos que mostrem churn por idade, gênero, tipo de contrato, serviços contratados, etc.
   * Análise de correlação entre variáveis e churn.

3. **Modelagem preditiva:**

   * Desenvolvimento de modelo de machine learning para prever churn.
   * Avaliação de métricas de performance (accuracy, precision, recall, F1-score, AUC-ROC).
   * Identificação das variáveis mais importantes para churn.

4. **Segmentação de clientes:**

   * Agrupamento de clientes em clusters com base em risco de churn.
   * Identificação de características comuns em clientes propensos a churn.

5. **Recomendações e ações:**

   * Sugestões de estratégias para retenção de clientes.
   * Identificação de produtos ou serviços com maior impacto na fidelização.

### 4. Requisitos Não Funcionais

* **Documentação completa:** Todos os passos da análise devem ser documentados.
* **Reprodutibilidade:** Análise deve ser reprodutível (notebook, scripts ou dashboard interativo).
* **Segurança e privacidade:** Dados sensíveis devem ser tratados com confidencialidade.
* **Performance:** Análises devem ser executadas de forma eficiente, mesmo em grandes volumes de dados.

### 5. Entregáveis

* Relatório técnico completo da análise.
* Dashboards interativos (Power BI, Tableau ou similar).
* Notebook Python ou R com scripts de EDA, visualização e modelagem.
* Documento de recomendações estratégicas para mitigação do churn.

### 6. Cronograma sugerido

| Etapa | Atividade                         | Prazo  |
| ----- | --------------------------------- | ------ |
| 1     | Coleta e limpeza de dados         | 2 dias |
| 2     | EDA e visualizações iniciais      | 3 dias |
| 3     | Modelagem preditiva               | 4 dias |
| 4     | Segmentação e análise de clusters | 2 dias |
| 5     | Relatório final e recomendações   | 2 dias |

---

**Observações:**

* O foco da análise é fornecer insights acionáveis para reduzir a taxa de churn.
* Recomenda-se priorizar variáveis com maior impacto no churn ao propor ações de retenção.
