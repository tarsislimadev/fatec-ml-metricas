# Resultados da análise

## Contexto

Foi treinado um modelo de regressão logística para prever a variável `survived` da base Titanic:

- `0`: passageiro não sobreviveu.
- `1`: passageiro sobreviveu.

A base possui 891 registros. Foram utilizados 712 registros para treinamento e 179 para teste, com divisão estratificada e `random_state=42`.

## Tratamento dos dados

- Variáveis utilizadas: `pclass`, `sex`, `age`, `sibsp`, `parch`, `fare` e `embarked`.
- Valores ausentes de idade preenchidos pela mediana.
- Valores ausentes de embarque preenchidos pela categoria mais frequente.
- Variáveis categóricas transformadas com one-hot encoding.
- Variáveis numéricas padronizadas.
- A coluna `deck` não foi utilizada devido à quantidade elevada de valores ausentes.

## Métricas

| Métrica | Resultado |
| --- | ---: |
| Acurácia | 80,45% |
| Precisão | 79,31% |
| Recall | 66,67% |
| F1-score | 72,44% |

### Interpretação das métricas

- **Acurácia:** o modelo classificou corretamente 80,45% dos passageiros do conjunto de teste.
- **Precisão:** entre os passageiros classificados como sobreviventes, 79,31% realmente sobreviveram.
- **Recall:** o modelo identificou 66,67% dos passageiros que realmente sobreviveram.
- **F1-score:** o equilíbrio entre precisão e recall foi de 72,44%.

## Matriz de confusão

A matriz foi organizada com as linhas representando a classe real e as colunas representando a classe prevista:

|  | Previsto: não sobreviveu | Previsto: sobreviveu |
| --- | ---: | ---: |
| Real: não sobreviveu | 98 | 12 |
| Real: sobreviveu | 23 | 46 |

- **Verdadeiros negativos:** 98 passageiros que não sobreviveram foram classificados corretamente.
- **Falsos positivos:** 12 passageiros foram classificados como sobreviventes, mas não sobreviveram.
- **Falsos negativos:** 23 passageiros sobreviveram, mas não foram identificados pelo modelo.
- **Verdadeiros positivos:** 46 passageiros que sobreviveram foram classificados corretamente.

## Avaliação final

O modelo apresentou desempenho geral razoável, com acurácia de 80,45%. A precisão próxima de 80% indica que as previsões positivas são relativamente confiáveis. Porém, o recall de 66,67% revela uma limitação importante: 23 dos 69 sobreviventes do conjunto de teste não foram identificados.

Portanto, o modelo é adequado como uma análise inicial e reproduzível, mas pode ser aprimorado com comparação entre outros algoritmos, ajuste de hiperparâmetros, engenharia de atributos e validação cruzada. A acurácia não deve ser analisada isoladamente, pois a base possui mais casos de não sobrevivência do que de sobrevivência.

## Reprodutibilidade

Os resultados foram gerados em [analise_titanic.ipynb](./analise_titanic.ipynb), usando a base [titanic.csv](./titanic.csv) e as dependências listadas em [requirements.txt](./requirements.txt).
