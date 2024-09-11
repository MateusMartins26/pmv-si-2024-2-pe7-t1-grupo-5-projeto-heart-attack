# Conhecendo os dados

Nesta seção, deverá ser registrada uma detalhada análise descritiva e exploratória sobre a base de dados selecionada na Etapa 1 com o objetivo de compreender a estrutura dos dados, detectar eventuais _outliers_ e também, avaliar/detectar as relações existentes entre as variáveis analisadas.

Para isso, sugere-se que sejam utilizados cálculos de medidas de tendência central, como média, mediana e moda, para entender a centralidade dos dados; sejam exploradas medidas de dispersão como desvio padrão e intervalos interquartil para avaliar a variabilidade dos dados; sejam utilizados gráficos descritivos como histogramas e box plots, para representar visualmente as características essenciais dos dados, pois essas visualizações podem facilitar a identificação de padrões e anomalias; sejam analisadas as relações entre as variáveis por meio de análise de correlação, gráficos de dispersões, mapas de calor, entre outras técnicas. 



O grupo utilizou a ferramenta utilizou o software Power BI para coletar métricas que auxiliarão nas análises dos pacientes do dataset selecionado. Para elaborar as métricas, foi necessário a utilização da linguagem DAX(Data Analysis Expressions) para criar algumas funções como a média de colesterol dos pacientes envolvidos.

Nesta tabela, os componentes trouxeram um breve detalhamento da média de colesterol dos pacientes. Para realizar o agrupamento dos participantes, foi necessário criar uma coluna condicional através do Power Query, ferramenta ETL para limpeza e preparação de dados do Power BI. Com isso, os pacientes foram separados por sua faixa etária.


![image](/src/images/Colesterol.png)

Segue o código utilizado para se chegar nestas medidas:

![image](/src/images/Colesterol%20Geral.png)

Com essa medida, é realizado o cálculo da média de colesterol e após este procedimento, por meio da função All, os demais filtros serão ignorados dentro do ambiente de desenvolvimento. 


![image](/src/images/Razão%20e%20Proporção.png)

Essa outra medida faz a divisão da média de colesterol das faixas etárias pela média geral de colesterol. Os valores gerados são úteis para se perceber a variação dos itens em relação à tendência central.

Inclua nesta seção, gráficos, tabelas e demais artefatos que você considere relevantes para entender os dados com os quais você irá trabalhar.  Além disso, inclua e comente os trechos de código mais relevantes desenvolvidos para realizar suas análises. Na pasta "src", inclua o código fonte completo.


## Descrição dos achados

A partir da análise descrita e exploratória realizada, descreva todos os achados considerados relevantes para o contexto em que o trabalho se insere. Por exemplo: com relação à centralidade dos dados algo chamou a atenção? Foi possível identificar correlação entre os atributos? Que tipo de correlação (forte, fraca, moderada)? 

## Ferramentas utilizadas

Existem muitas ferramentas diferentes que podem ser utilizadas para fazer a análise dos dados. Nesta seção, descreva as ferramentas/tecnologias utilizadas e sua aplicação. Vale destacar que, preferencialmente, as análises deverão ser realizadas utilizando a linguagem de programação Python.

