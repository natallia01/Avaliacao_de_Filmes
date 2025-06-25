# Avaliacao_de_Filmes
Análise exploratória de um banco de dados de avaliação de filmes

import pandas as pd

notas = pd.read_csv('/ratings.csv')
notas.head()

notas['rating'].count()
notas['rating'].value_counts()

notas["rating"].plot(kind='hist')

import seaborn as sns
sns.boxplot(notas["rating"])

notas['rating'].mean()
print(f'A Média das notas é: {notas["rating"].mean()}')
notas['rating'].median()
print(f'A Mediana das notas é: {notas["rating"].median()}')


notas['rating'].describe()


