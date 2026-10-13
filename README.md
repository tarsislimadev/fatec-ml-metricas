# [Fatec Métricas (Machine Learning)](https://classroom.google.com/c/ODcxODQyODAxNTEw/a/ODg5OTM1ODY1Mjgw/details)

Procure por uma base de dados na Internet (por exemplo: Kagle) e utilize o exemplo dado em aula para aplicar as transformações dos dados (tranformá-los em numeros). Depois, apresente:

- [ ] Matriz de confusão
- [ ] Acurácia
- [ ] Precisão
- [ ] Recall
- [ ] Ao final faça uma avaliação, dada as métricas encontradas.

Esta é uma tarefa individual e avaliativa que deverá ser apresentada na próxima aula. 

Tempo de apresentação: 10 minutos

Entrega: 

- [ ] Arquivo .ipynb, 
- [ ] base de dados (.xlsx, .csv...)
- [ ] Arquivo de apresentação (.pptx, .docx, ...)

Atenção: Após o dia 20/10 a atividade se encerará, sem possibilidade de entrega posterior.

## Projeto desenvolvido

Este repositório utiliza a base pública Titanic para prever a sobrevivência de passageiros com regressão logística. O notebook realiza a inspeção dos dados, o tratamento de valores ausentes, a transformação de variáveis categóricas e o cálculo das métricas de classificação.

### Arquivos

- [`analise_titanic.ipynb`](./analise_titanic.ipynb): análise completa e reproduzível.
- [`titanic.csv`](./titanic.csv): base de dados utilizada.
- [`apresentacao_titanic.pptx`](./apresentacao_titanic.pptx): apresentação com metodologia e resultados.
- [`plan.md`](./plan.md): plano de desenvolvimento.
- [`requirements.txt`](./requirements.txt): dependências Python.

### Como executar

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
jupyter notebook analise_titanic.ipynb
```

O notebook usa `random_state=42`, portanto os resultados podem ser reproduzidos. Na execução validada, o modelo obteve acurácia de 80,45%, precisão de 79,31% e recall de 66,67%.

## license

[MIT](./LICENSE)
