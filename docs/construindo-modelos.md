# Preparação dos dados

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


## Importando métrica de acurácia e demonstrando resultado da acurácia

 - ![image](/src/images/Acurácia.png)

## Treinamento de Y 

y_pred_train = gnb.predict(X_train)

y_pred_train

## Resultado dos treinamntos

print('Training set score: {:.4f}'.format(gnb.score(X_train, y_train)))

print('Test set score: {:.4f}'.format(gnb.score(X_test, y_test)))

![image](/src/images/Treinamento.png)

## Checando o score de acurácia nula


null_accuracy = (7407/(7407+2362))

print('Null accuracy score: {0:0.4f}'. format(null_accuracy))


![image](/src/images/AcuráciaNula.png)

## Criando e plotando a matriz de confusão 

import seaborn as sns
from sklearn.metrics import confusion_matrix

cm = confusion_matrix(y_test, y_pred)


plt.figure(figsize=(8, 6))
sns.heatmap(cm, annot=True, fmt="d", cmap="Blues",
            xticklabels=Treatment_map.keys(),
            yticklabels=Treatment_map.keys())
plt.title("Matriz de confusão do modelo Naive Bayes")
plt.xlabel("Predicted Treatment")
plt.ylabel("Actual Treatment")
plt.savefig("knn_matriz_confusão.png")  
plt.show()

## Resultado 

![image](/src/images/MatrizConfusão%20NB.png)


# Descrição dos modelos

Nesta seção, conhecendo os dados e de posse dos dados preparados, é hora de descrever os algoritmos de aprendizado de máquina selecionados para a construção dos modelos propostos. Inclua informações abrangentes sobre cada algoritmo implementado, aborde conceitos fundamentais, princípios de funcionamento, vantagens/limitações e justifique a escolha de cada um dos algoritmos. 

Explore aspectos específicos, como o ajuste dos parâmetros livres de cada algoritmo. Lembre-se de experimentar parâmetros diferentes e principalmente, de justificar as escolhas realizadas.

Como parte da comprovação de construção dos modelos, um vídeo de demonstração com todas as etapas de pré-processamento e de execução dos modelos deverá ser entregue. Este vídeo poderá ser do tipo _screencast_ e é imprescindível a narração contemplando a demonstração de todas as etapas realizadas.

# Avaliação dos modelos criados

## Métricas utilizadas

Nesta seção, as métricas utilizadas para avaliar os modelos desenvolvidos deverão ser apresentadas (p. ex.: acurácia, precisão, recall, F1-Score, MSE etc.). A escolha de cada métrica deverá ser justificada, pois esta escolha é essencial para avaliar de forma mais assertiva a qualidade do modelo construído. 

## Discussão dos resultados obtidos

Nesta seção, discuta os resultados obtidos pelos modelos construídos, no contexto prático em que os dados se inserem, promovendo uma compreensão abrangente e aprofundada da qualidade de cada um deles. Lembre-se de relacionar os resultados obtidos ao problema identificado, a questão de pesquisa levantada e estabelecendo relação com os objetivos previamente propostos. 

# Pipeline de pesquisa e análise de dados

Em pesquisa e experimentação em sistemas de informação, um pipeline de pesquisa e análise de dados refere-se a um conjunto organizado de processos e etapas que um profissional segue para realizar a coleta, preparação, análise e interpretação de dados durante a fase de pesquisa e desenvolvimento de modelos. Esse pipeline é essencial para extrair _insights_ significativos, entender a natureza dos dados e, construir modelos de aprendizado de máquina eficazes. 

## Observações importantes

Todas as tarefas realizadas nesta etapa deverão ser registradas em formato de texto junto com suas explicações de forma a apresentar  os códigos desenvolvidos e também, o código deverá ser incluído, na íntegra, na pasta "src".

Além disso, deverá ser entregue um vídeo onde deverão ser descritas todas as etapas realizadas. O vídeo, que não tem limite de tempo, deverá ser apresentado por **todos os integrantes da equipe**, de forma que, cada integrante tenha oportunidade de apresentar o que desenvolveu e as  percepções obtidas.
