# Modelo - Classificador Naive Bayes

## Importando Bibliotecas Necessárias

import numpy as np # linear algebra
import pandas as pd # data processing, CSV file I/O (e.g. pd.read_csv)
import matplotlib.pyplot as plt # for data visualization purposes
import seaborn as sns # for statistical data visualization
from sklearn.model_selection import train_test_split
from sklearn.tree import DecisionTreeClassifier
from sklearn.preprocessing import StandardScaler
from sklearn.metrics import accuracy_score
from sklearn.impute import SimpleImputer
import warnings

warnings.filterwarnings('ignore')
%matplotlib inline
import os
for dirname, _, filenames in os.walk('/kaggle/input'):
    for filename in filenames:
        print(os.path.join(dirname, filename))

        import pandas as pd

## Colocando Dataset em uma variável

df = pd.read_csv('/content/sample_data/heart_attack_dataset.csv')

## Mapeando, convertando e aplicando colunas categórias para númericas do tipo float, padrão americano

Gender_map = {'Male': 1, 'Female': 0}
Has_Diabetes_map = {'Yes': 1, 'No': 0}
Smoking_Status_map = {' Never': 0, 'Former': 1, 'Current': 2}
Chest_Pain_Type_map = {'Typical Angina': 0, 'Atypical Angina': 1, 'Non-anginal Pain': 2, 'Asymptomatic': 3}
Treatment_map = {'Lifestyle Changes': 0, 'Angioplasty': 1, 'Coronary Artery Bypass Graft (CABG)': 2, 'Medication': 3}

df['Gender'] = df['Gender'].map(Gender_map).astype(float)
df['Has Diabetes'] = df['Has Diabetes'].map(Has_Diabetes_map).astype(float)
df['Smoking Status'] = df['Smoking Status'].map(Smoking_Status_map).astype(float)
df['Chest Pain Type'] = df['Chest Pain Type'].map(Chest_Pain_Type_map).astype(float)
df['Treatment'] = df['Treatment'].map(Treatment_map).astype(float)


## Categorizando colunas

num_cols = ['Age', 'Blood Pressure (mmHg)', 'Cholesterol (mg/dL)']
cat_cols = ['Gender', 'Has Diabetes', 'Smoking Status', 'Chest Pain Type']

num_imputer = SimpleImputer(strategy='median')
cat_imputer = SimpleImputer(strategy='most_frequent')

df[num_cols] = num_imputer.fit_transform(df[num_cols])
df[cat_cols] = cat_imputer.fit_transform(df[cat_cols])


## Mostrando informações do sobre os dados


- ![image](/src/images/df.info().PNG)

## Definindo Colunas 

col_names = ['Gender', 'Age', 'Blood Pressure (mmHg)', 'Cholesterol (mg/dL)', 'Has Diabetes', 'Smoking Status', 'Chest Pain Type', 'Treatment']

df.columns = col_names
df.columns


## Encontrando Variáveis Categóricas

categorical = [var for var in df.columns if df[var].dtype=='O']

print('Há {} variáveis categóricas\n'.format(len(categorical)))

print('As variáveis categóricas são :\n\n', categorical)

## Resultado 

- ![image](/src/images/VarCat.png)

## Declarando Var. Destino e Vetor de Características

X = df.drop(['Treatment'], axis=1)

y = df['Treatment']

## Declarando Var. Destino e Vetor de Características

from sklearn.model_selection import train_test_split

X_train, X_test, y_train, y_test = train_test_split(X, y, test_size = 0.3, random_state = 0)

## Resultado tamanho dos set de treinamento e de teste

X_train.shape, X_test.shape

- ![image](/src/images/set.png)


## Como foi executado no início do código o mapeamento das variáveis, não há valores categóricos 

categorical = [col for col in X_train.columns if X_train[col].dtypes == 'O']

categorical


numerical = [col for col in X_train.columns if X_train[col].dtypes != 'O']

numerical


- ![image](/src/images/Tipos%20Dados.png)



## Feature Scaling(Determinando volume de recurso para treinametno)

cols = X_train.columns


## Começando o procedimento para criação do modelo 

from sklearn.naive_bayes import GaussianNB

## Instanciando o modelo

gnb = GaussianNB()

## Ajustando Modelo 

gnb.fit(X_train, y_train)


## Prevendo o resultado

y_pred = gnb.predict(X_test) # Cada número é o tipo de treinamento realizado

### Treatment_map ={'Lifestyle Changes': 1, 'Angioplasty': 2, 'Coronary Artery Bypass Graft (CABG)': 3, 'Medication': 4}

y_pred

 - ![image](/src/images/Prevendo%20Resultado.png)