# Pandas: conhecendo a biblioteca

Curso: https://cursos.alura.com.br/course/pandas-conhecendo-biblioteca

Trello: https://trello.com/b/TUp6cdkC/pandas-conhecendo-a-biblioteca

O que aprendemos : 
* Importar a biblioteca Pandas;
```python
import pandas as pd
```
* Realizar a leitura de arquivos csv;
```python
pd.read_csv(dados, sep=",")
```
* Visualizar linhas iniciais e finais de um DataFrame;
```python
DataFrame.head(5) # Retorna as 5 primeiras linhas.

DataFrame.tail(5) # Retorna as 5 últimas linhas.
``` 
* Verificar a quantidade de linhas e colunas de um DataFrame;
```python
DataFrame.shape()
```
* Conferir os tipos de dados de cada coluna de um DataFrame;
```python
DataFrame.info()
```
* Selecionar uma ou múltiplas colunas.
```python
DataFrame['Coluna']

DataFrame[['Coluna1'. 'Coluna2']] # Passar uma lista com os nomes das colunas.
```
* Calcular a média de valores de um DataFrame;
```python
DataFrame.mean()
```
* Agrupar os dados de acordo com uma coluna específica utilizando o groupby;
```python
DataFrame.groupby('Coluna').mean() # Essa função funciona em conjunto com sum(), mean() e etc.
```
* Fazer seleções utilizando o método query;
```python
DataFrame.query("@var in Coluna") # Para usarmos uma var na expressão necessário botar @ antes.
```
* Transformar Series em DataFrames;
```python
DataFrame.to_frame()
```
* Ordenar valores de um DataFrame com o sort_values;
```python
DataFrame.sort_values()
```
* Plotar gráficos de barras verticais e horizontais;
```python
DataFrame.plot(kind="barh", figsize=(10,4), xlabel="Eixo_x", ylabel="Eixo_y", color="green")
```
* Visualizar valores únicos com o unique;
```python
DataFrame["Coluna"].unique()
```
* Utilizar o value_counts para contar valores únicos e calcular percentuais;
```python
DataFrame['Coluna'].value_counts() # Para transformar em % passamos o argumento "normalize=True".
```
* Mudar nomes de colunas.
```python
DataFrame.rename(columns={'nome_antigo': 'novo_nome'})
```
* Verificar se uma base de dados possui dados nulos;
```python
DataFrame.isnull() # Retorna um df com True e False.
```
* Tratar os dados nulos;
```python
DataFrame.fillna(value=0) # substitui todos os valores nulos com um método ou por algum valor.

DataFrame.dropna()  # Remove todas as linhas ou colunas que possuem pelo menos um valor nulo.
```
* Remover linhas e colunas de um DataFrame;
```python
DataFrame.drop(columns=['nome_da_coluna']) # Remover uma coluna pelo nome

DataFrame.drop([índice_da_linha]) # Remover uma linha pelo índice
```
* Realizar diferentes seleções em uma base de dados;
```python
selecao = (DataFrame['Coluna1'] >= 2) & (DataFrame['Coluna2'] < 3000) # Series de True e False

DataFrame[selecao] # Filtra utilizando o uma Series Booleana

DataFrame.query('Coluna1 >= 2 & Coluna2 < 3000') # O mesmo filtro utilizando query
```
* Salvar dados no formato csv;
```python
DataFrame.to_csv('nome_do_arquivo', index=False) # Salva um data frame na pasta local sem a coluna de index.
```
* Utilizar o método replace para substituir valores em uma base de dados.
```python

```