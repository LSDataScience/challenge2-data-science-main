# Telecom X - Análise de Evasão de Clientes

Projeto completo em duas etapas sobre evasão de clientes da Telecom X, cobrindo desde ETL e análise exploratória até modelagem preditiva com Machine Learning.

## Objetivo

Investigar os fatores associados ao churn de clientes e construir uma base analítica para prever evasão e apoiar estratégias de retenção.

## Conteúdo do Projeto

- TelecomX_BR.ipynb: Parte 1 com extração, tratamento, EDA e relatório final.
- TelecomX_tratado.csv: base tratada gerada ao fim da Parte 1.
- TelecomX_BR_Parte2_Prevendo_Churn.ipynb: Parte 2 com pipeline de Machine Learning e conclusões estratégicas.
- TelecomX_Data.json: base de dados em JSON.
- TelecomX_dicionario.md: dicionário de dados com descrição das variáveis.

## Etapas Realizadas

1. Extração dos dados a partir de fonte remota no GitHub, com fallback local.
2. Normalização do JSON aninhado para DataFrame.
3. Limpeza de inconsistências, conversão de tipos e padronização textual.
4. Criação da variável Contas_Diarias com base no gasto mensal.
5. Análise descritiva e visual da evasão por variáveis categóricas e numéricas.
6. Preparação para modelagem (remoção de ID, encoding e split treino/teste).
7. Treinamento de dois modelos de classificação: Regressão Logística e Random Forest.
8. Avaliação com acurácia, precisão, recall, F1-score e matriz de confusão.
9. Análise de importância de variáveis e recomendações estratégicas de retenção.

## Principais Insights

- A taxa geral de evasão observada foi de 26,54%.
- Clientes com contrato mensal apresentaram o maior risco de evasão.
- O método de pagamento com maior evasão foi cheque eletrônico.
- Clientes com internet por fibra óptica concentraram maior taxa de churn.
- Na modelagem, a Regressão Logística apresentou melhor equilíbrio entre precisão, recall e F1 no conjunto de teste.
- O Random Forest mostrou sinal de overfitting no comparativo treino x teste.
- Tempo de contrato, gasto total e tipo de contrato foram fatores centrais para previsão de evasão.

## Tecnologias Utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Requests
- Scikit-learn
- Jupyter Notebook

## Como Executar

1. Crie e ative um ambiente virtual Python.
2. Instale as dependências:

```bash
pip install -r requirements.txt
```

3. Execute a Parte 1 no notebook `TelecomX_BR.ipynb`.
4. Em seguida, execute a Parte 2 no notebook `TelecomX_BR_Parte2_Prevendo_Churn.ipynb`.

## Fonte dos Dados

Os dados são carregados preferencialmente a partir do arquivo remoto:

https://raw.githubusercontent.com/ingridcristh/challenge2-data-science/main/TelecomX_Data.json

## Próximos Passos

- Testar técnicas de balanceamento (SMOTE/undersampling) e comparar impacto no recall da classe de evasão.
- Realizar tuning de hiperparâmetros com validação cruzada.
- Gerar dashboard executivo para acompanhamento de risco de churn.