# Telecom X - Analise de Evasao de Clientes

Projeto completo em duas etapas sobre evasao de clientes da Telecom X, cobrindo desde ETL e analise exploratoria ate modelagem preditiva com Machine Learning.

## Objetivo

Investigar os fatores associados ao churn de clientes e construir uma base analitica para prever evasao e apoiar estrategias de retencao.

## Conteúdo do Projeto

- TelecomX_BR.ipynb: Parte 1 com extracao, tratamento, EDA e relatorio final.
- TelecomX_tratado.csv: base tratada gerada ao fim da Parte 1.
- TelecomX_BR_Parte2_Prevendo_Churn.ipynb: Parte 2 com pipeline de Machine Learning e conclusoes estrategicas.
- TelecomX_Data.json: base de dados em JSON.
- TelecomX_dicionario.md: dicionario de dados com descricao das variaveis.

## Etapas Realizadas

1. Extracao dos dados a partir de fonte remota no GitHub, com fallback local.
2. Normalizacao do JSON aninhado para DataFrame.
3. Limpeza de inconsistencias, conversao de tipos e padronizacao textual.
4. Criacao da variavel Contas_Diarias com base no gasto mensal.
5. Analise descritiva e visual da evasao por variaveis categoricas e numericas.
6. Preparacao para modelagem (remocao de ID, encoding e split treino/teste).
7. Treinamento de dois modelos de classificacao: Regressao Logistica e Random Forest.
8. Avaliacao com acuracia, precisao, recall, F1-score e matriz de confusao.
9. Analise de importancia de variaveis e recomendacoes estrategicas de retencao.

## Principais Insights

- A taxa geral de evasao observada foi de 26,54%.
- Clientes com contrato mensal apresentaram o maior risco de evasao.
- O metodo de pagamento com maior evasao foi cheque eletronico.
- Clientes com internet por fibra optica concentraram maior taxa de churn.
- Na modelagem, a Regressao Logistica apresentou melhor equilibrio entre precision, recall e F1 no conjunto de teste.
- O Random Forest mostrou sinal de overfitting no comparativo treino x teste.
- Tempo de contrato, gasto total e tipo de contrato foram fatores centrais para previsao de evasao.

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

## Proximos Passos

- Testar tecnicas de balanceamento (SMOTE/undersampling) e comparar impacto no recall da classe de evasao.
- Realizar tuning de hiperparametros com validacao cruzada.
- Gerar dashboard executivo para acompanhamento de risco de churn.