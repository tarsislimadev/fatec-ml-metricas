# Plano do projeto

## Objetivo

Desenvolver uma análise de classificação usando a base de dados Titanic para prever se um passageiro sobreviveu ao naufrágio. O projeto deverá demonstrar o tratamento dos dados, o treinamento de um modelo e a avaliação por métricas de classificação.

## Entregas

- `analise_titanic.ipynb`: notebook com todo o processo executável.
- `titanic.csv`: base de dados utilizada.
- `apresentacao.pptx`: material para a apresentação de 10 minutos.
- `README.md`: documentação resumida do projeto e instruções de execução.

## Etapas de desenvolvimento

### 1. Seleção e entendimento da base

- Utilizar a base Titanic do Kaggle ou uma fonte pública equivalente.
- Definir `Survived` como variável-alvo.
- Identificar as variáveis preditoras, seus tipos e possíveis valores ausentes.
- Registrar a fonte e uma breve descrição da base no notebook.

### 2. Preparação dos dados

- Carregar a base com `pandas`.
- Inspecionar dimensões, tipos, estatísticas e valores ausentes.
- Remover colunas que não contribuam para a previsão, como identificadores.
- Preencher ou remover valores ausentes com uma justificativa.
- Transformar variáveis categóricas em valores numéricos.
- Separar as variáveis de entrada (`X`) da variável-alvo (`y`).
- Dividir os dados em conjuntos de treino e teste, mantendo uma semente aleatória definida.

### 3. Treinamento do modelo

- Treinar inicialmente um `DecisionTreeClassifier` ou `LogisticRegression`.
- Documentar os principais parâmetros utilizados.
- Gerar previsões para o conjunto de teste.
- Evitar utilizar informações do conjunto de teste durante o treinamento.

### 4. Avaliação

- Calcular a matriz de confusão.
- Calcular acurácia, precisão e recall.
- Calcular também o F1-score para complementar a análise.
- Exibir a matriz de confusão e os resultados em tabelas ou gráficos legíveis.
- Explicar o significado de verdadeiros positivos, verdadeiros negativos, falsos positivos e falsos negativos no contexto do Titanic.

### 5. Interpretação dos resultados

- Comparar as métricas e explicar o desempenho do modelo.
- Avaliar se o modelo identifica adequadamente os passageiros sobreviventes.
- Comentar o impacto dos falsos negativos e falsos positivos.
- Registrar limitações, como tamanho da base, variáveis utilizadas e possível desbalanceamento das classes.

### 6. Preparação da apresentação

Organizar a apresentação em aproximadamente 10 minutos:

1. Problema e objetivo.
2. Descrição da base de dados.
3. Tratamento e transformação das variáveis.
4. Modelo de Machine Learning escolhido.
5. Matriz de confusão e métricas.
6. Interpretação dos resultados.
7. Conclusão e limitações.

## Critérios de conclusão

- [ ] O notebook executa do início ao fim sem erros.
- [ ] A base de dados está incluída no projeto ou possui uma fonte documentada.
- [ ] As variáveis categóricas foram transformadas em números.
- [ ] A matriz de confusão foi apresentada.
- [ ] Acurácia, precisão e recall foram calculados e interpretados.
- [ ] A avaliação final relaciona as métricas ao problema analisado.
- [ ] O material de apresentação está pronto para uma exposição de 10 minutos.
- [ ] Os arquivos estão organizados para a entrega antes do prazo definido no README.

## Dependências sugeridas

```text
pandas
numpy
scikit-learn
matplotlib
seaborn
jupyter
```