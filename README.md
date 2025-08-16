# Análise de Evasão de Clientes – Telecom X

## Descrição do Projeto
Este projeto tem como objetivo analisar a **evasão de clientes (Churn)** na Telecom X, identificar os fatores que mais influenciam o cancelamento de serviços e construir modelos preditivos para antecipar a evasão.

O projeto inclui:
- Limpeza e tratamento de dados;
- Análise exploratória para identificar padrões;
- Construção de modelos preditivos (Regressão Logística e Random Forest);
- Avaliação do desempenho dos modelos;
- Identificação das variáveis mais relevantes para a previsão de churn;
- Estratégias de retenção de clientes com base nos insights obtidos.

---

## Estrutura do Dataset
O dataset utilizado contém informações sobre contratos, serviços utilizados, características dos clientes e métricas de consumo. Algumas colunas importantes:
- `Churn` – indica se o cliente cancelou (`yes`) ou não (`no`);
- `account_Contract` – tipo de contrato do cliente;
- `account_Charges` – valor total das cobranças;
- `customer_tenure` – tempo de permanência do cliente;
- `Contas_Diarias` – gasto médio diário;
- Variáveis categóricas relacionadas a serviços de internet, telefone e billing.

---

## Limpeza e Tratamento de Dados
- Importação dos dados em formato CSV ou JSON.
- Conversão de colunas numéricas para float/int.
- Padronização da coluna `Churn` para valores binários (`0 = no`, `1 = yes`).
- Remoção de duplicados e valores ausentes.
- Expansão de colunas categóricas via **One-Hot Encoding**.

---

## Análise Exploratória
- Clientes `month-to-month` apresentam maior risco de churn.
- Clientes com menor tempo de contrato e menor gasto diário tendem a cancelar mais.
- Serviços adicionais influenciam na retenção dos clientes.
- Distribuição de Churn:
  - Não cancelaram: 5.174 (73%)
  - Cancelaram: 1.869 (27%)

---

## Modelos Preditivos
Foram treinados dois modelos:

1. **Regressão Logística**
   - Normalização aplicada.
   - Bom desempenho geral, mas baixo recall para a classe `churn`.

2. **Random Forest**
   - Sem normalização necessária.
   - Melhor equilíbrio entre classes, maior recall para churn.

**Conclusão:** Random Forest foi o modelo mais eficiente para identificar clientes propensos a cancelar.

---

## Variáveis Mais Relevantes
Principais fatores que influenciam o churn:
- Tipo de contrato (`month-to-month`);
- Tempo de contrato (`customer_tenure`);
- Gasto diário (`Contas_Diarias`);
- Serviços adicionais (ex.: `Paperless Billing`, `Online Security`).

---

## Recomendações de Negócio
- Incentivar contratos mais longos com descontos ou benefícios.
- Criar campanhas direcionadas para clientes recentes ou com baixo gasto diário.
- Promover serviços adicionais para aumentar engajamento e retenção.

---
## Tecnologias Utilizadas

- Python

- Pandas, NumPy

- Scikit-learn

- Matplotlib, Seaborn
---

## Como Rodar
1. Clonar o repositório:
```bash
git clone 
pip install -r requirements.txt
