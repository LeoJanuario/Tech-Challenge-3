# 📊 Previsão de Criptomoedas com CatBoost

Este projeto coleta dados de uma API pública, realiza o pré-processamento e treina modelos de Regressão e Classificação usando CatBoost para prever o comportamento de criptomoedas no dia seguinte.

---

## 🔗 Fonte de Dados

- API: [AWS Lambda Endpoint](https://6gt6hotdph.execute-api.us-east-1.amazonaws.com/Prod/GetCoinData)

---

## 🧪 Tecnologias Utilizadas

- Python 3
- Google Colab
- Pandas
- Requests
- CatBoost
- Scikit-learn

---

## ⚙️ Funcionalidades

- Coleta e agregação de dados de preço, volume e market cap.
- Conversão de timestamp para data.
- Cálculo da média diária por moeda.
- Criação de rótulo para previsão de tendência (`alta_amanha`).
- Treinamento de dois modelos:
  - `CatBoostRegressor` para prever o preço médio do dia seguinte.
  - `CatBoostClassifier` para prever se o preço irá subir ou cair.
- Função para prever a próxima tendência e variação percentual de uma moeda específica.

---

## 📈 Exemplo de Saída

```
Último dado disponível 2025-05-25: Preço médio = R$ 607,959.22  
Previsão para o dia: 2025-05-26: A tendência da 'bitcoin' é Descer.  
Estimativa de preço: R$ 596,715.36 (-1.85%)
```

---

## 🚀 Como Executar

1. Abra no Google Colab:
   [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/)

2. Instale as dependências:
```bash
!pip install catboost
```

3. Execute o notebook completo.

---

## 🧠 Modelos

- **CatBoostRegressor**
  - `RMSE`: ~9930
- **CatBoostClassifier**
  - `Acurácia`: 50%

---

## 📁 Estrutura do Projeto

```
├── previsao_cripto.ipynb  # Notebook principal com código completo
├── README.md              # Este arquivo
```

---

## 📌 Observações

- O modelo de classificação teve acurácia de 50%, indicando necessidade de melhorias (mais dados ou features).
- O modelo de regressão obteve RMSE razoável dado o contexto.

---
