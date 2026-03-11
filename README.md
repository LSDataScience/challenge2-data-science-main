# Telecom X - Análise de Evasão de Clientes

Projeto de análise exploratória de dados sobre evasão de clientes da Telecom X, desenvolvido em Python com foco em ETL, limpeza, visualização e geração de insights para apoiar estratégias de retenção.

## Objetivo

Investigar os fatores associados ao churn de clientes, preparando uma base confiável para análises futuras e para a próxima etapa de modelagem preditiva.

## Conteúdo do Projeto

- TelecomX_BR.ipynb: notebook principal com extração, tratamento, EDA e relatório final.
- TelecomX_Data.json: base de dados em JSON.
- TelecomX_dicionario.md: dicionário de dados com descrição das variáveis.

## Etapas Realizadas

1. Extração dos dados a partir de uma fonte remota no GitHub, com fallback local.
2. Normalização do JSON aninhado para DataFrame.
3. Limpeza de inconsistências, conversão de tipos e padronização textual.
4. Criação da variável Contas_Diarias com base no gasto mensal.
5. Análise descritiva e visual da evasão por variáveis categóricas e numéricas.
6. Consolidação de conclusões e recomendações dentro do notebook.

## Principais Insights

- A taxa geral de evasão observada foi de 26,54%.
- Clientes com contrato mensal apresentaram o maior risco de evasão.
- O método de pagamento com maior evasão foi cheque eletrônico.
- Clientes com internet por fibra óptica concentraram a maior taxa de churn.
- Clientes que evadiram, em média, permaneceram menos tempo na base e tinham gasto mensal maior.

## Tecnologias Utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Requests
- Jupyter Notebook

## Como Executar

1. Crie e ative um ambiente virtual Python.
2. Instale as dependências:

```bash
pip install -r requirements.txt
```

3. Abra o notebook TelecomX_BR.ipynb.
4. Execute as células em ordem.

## Fonte dos Dados

Os dados são carregados preferencialmente a partir do arquivo remoto:

https://raw.githubusercontent.com/ingridcristh/challenge2-data-science/main/TelecomX_Data.json

## Próximos Passos

- Construir variáveis derivadas para modelagem.
- Testar algoritmos preditivos de churn.
- Avaliar métricas de classificação e interpretar variáveis mais importantes.