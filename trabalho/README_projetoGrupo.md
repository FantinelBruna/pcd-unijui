# Análise e Previsão de Aprovação de Empréstimos Bancários

Projeto desenvolvido para a disciplina de **Programação para Ciência de Dados**, com o objetivo de analisar solicitações de empréstimos bancários e utilizar Machine Learning para prever sua aprovação ou rejeição.

## Integrantes

- Bruna Fantinel
- Francisco Aquino
- Nícolas Hartmann
- Matheus Tonetto

## Objetivo

Analisar dados de solicitações de empréstimos para identificar quais características estão relacionadas à aprovação ou rejeição de crédito, utilizando Python para tratamento dos dados, visualizações e treinamento de um modelo de classificação.

## Base de dados

Foi utilizado o [Loan Approval Prediction Dataset](https://www.kaggle.com/datasets/architsharma01/loan-approval-prediction-dataset), disponível no Kaggle.

A base contém inicialmente **4.269 registros e 13 colunas**, com informações como:

- Renda anual do solicitante;
- Valor e prazo do empréstimo;
- Pontuação de crédito (CIBIL Score);
- Escolaridade e situação profissional;
- Patrimônio do solicitante;
- Situação do empréstimo (aprovado ou rejeitado).

Os dados são carregados por meio de um arquivo CSV público hospedado no GitHub.

## Tecnologias utilizadas

- **Python:** linguagem utilizada no desenvolvimento.
- **Pandas:** leitura, organização e limpeza dos dados.
- **Matplotlib e Seaborn:** criação de gráficos.
- **Scikit-learn:** treinamento e avaliação do modelo.
- **Google Colab:** ambiente de desenvolvimento e execução.

## Desenvolvimento

O projeto foi organizado nas seguintes etapas:

1. **Obtenção dos dados:** leitura do arquivo CSV e identificação das variáveis.
2. **Preparação e limpeza:** padronização das colunas, verificação de valores ausentes, duplicados e inconsistências.
3. **Análise exploratória:** criação de gráficos para investigar as características das solicitações.
4. **Preparação para Machine Learning:** conversão das variáveis categóricas em valores numéricos.
5. **Treinamento:** utilização do algoritmo `DecisionTreeClassifier`, com 80% dos dados para treinamento e 20% para teste.
6. **Avaliação:** análise da acurácia, matriz de confusão e importância das variáveis.

Durante a limpeza, foram encontrados **28 registros com valores negativos** na coluna `residential_assets_value`. Esses registros foram removidos, resultando em **4.241 solicitações** utilizadas na análise.

## Resultados

Na análise exploratória, observamos que:

- 62,2% das solicitações foram aprovadas e 37,8% rejeitadas.
- A pontuação de crédito CIBIL apresentou uma diferença significativa entre os dois grupos.
- A renda anual e a escolaridade, isoladamente, não apresentaram diferenças tão expressivas entre aprovados e rejeitados.

O modelo de árvore de decisão obteve os seguintes resultados:

| Indicador | Resultado |
|---|---|
| Acurácia | 99,53% |
| Solicitações utilizadas no teste | 849 |
| Previsões corretas | 845 |
| Previsões incorretas | 4 |

A variável mais importante para a classificação foi a **pontuação de crédito CIBIL**.

Os resultados representam o desempenho do modelo na base utilizada e não garantem o mesmo comportamento em outras bases de dados.

## Como executar

1. Acesse o [Google Colab](https://colab.research.google.com/).
2. Abra o arquivo `projetoGrupo.ipynb` disponível neste repositório.
3. Execute as células do notebook em ordem.
4. Acompanhe os resultados, gráficos e previsões gerados.

O notebook realiza a leitura dos dados diretamente por URL, sem necessidade de baixar o CSV manualmente.

## Conclusão

O projeto permitiu aplicar conceitos estudados na disciplina, desde a preparação e análise exploratória até a utilização de um algoritmo de Machine Learning.

A árvore de decisão apresentou um bom desempenho na classificação das solicitações, e a análise destacou a importância da pontuação de crédito nos resultados.

O trabalho possui finalidade acadêmica e não deve ser utilizado para decisões reais de concessão de crédito.

## Fonte dos dados

[Loan Approval Prediction Dataset — Kaggle](https://www.kaggle.com/datasets/architsharma01/loan-approval-prediction-dataset)

[Cópia pública do CSV utilizada no notebook](https://github.com/loh-0/Loan-Approval-Prediction)
