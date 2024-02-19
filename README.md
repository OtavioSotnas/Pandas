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
DataFrame.head(5)

DataFrame.tail(5)
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

DataFrame[['Coluna1'. 'Coluna2']]
```
* Calcular a média de valores de um DataFrame;
```python
DataFrame.mean()
```
* Agrupar os dados de acordo com uma coluna específica utilizando o groupby;
```python
DataFrame.groupby('Coluna').mean()
```
* Fazer seleções utilizando o método query;
```python
DataFrame.query("@variavel_exemplo in Coluna") # Para usarmos uma var na expressão necessário botar @ antes.
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
DataFrame.rename(columns={'nome_antigo': 'novo_nome'}) # Necessário pasar um dict como argumento para columns.
```