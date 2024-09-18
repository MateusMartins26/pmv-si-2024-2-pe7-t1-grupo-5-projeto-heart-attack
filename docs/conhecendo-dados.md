# Conhecendo os dados



### Utilizando o Google Colab, conseguimos obter as informações abaixo:


![image](https://github.com/user-attachments/assets/057f62bb-73ee-45ba-a983-3000ab840a01)

O Dataset é composto por 8 colunas: 
- Gender (Gênero Masculino e Feminino);
- Age (Idade);
- Blood Pressure (Pressão Sanguínea);
- Cholesterol (Colesterol);
- Has Diabetes (se paciente tem ou não Diabetes);
- Smoking Status (se paciente é, já foi ou não é fumante);
- Chest Pain Type (tipo de dor no peito que o paciente sente);
- Treatment (tipo de tratamento indicado).
Temos também 1.000 rows (linhas) referente à dados de 1.000 pessoas participantes do estudo/pesquisa.


![image](https://github.com/user-attachments/assets/9e21d732-08c7-4cca-8eb7-d6f990d45edf)

Das 8 colunas presentes no Dataset, 5 colunas apresentam dados do tipo objeto (Gender, Has Diabetes, Smoking Status Chest Pain Type, Treatment) sendo variáveis qualitativas e 3 colunas apresentam dados do tipo inteiro/int64 que são quantitativas (Age, Blood Pressure, Cholesterol). 


![image](https://github.com/user-attachments/assets/21f7d0b3-aed6-4dcb-9d47-2205d19f5156)

Importante destacar que não há dados nulos (linhas e colunas sem conteúdo) nesse Dataset. 


![image](https://github.com/user-attachments/assets/1dbfb213-7420-4129-8a40-f0f6f53371f5)

Realizando o describe do Dataset, temos para as variáveis quantitativas com dados do tipo inteiro/int64 que são numéricas das colunas Age, Blood Pressure e Choleterol, e obtemos os parâmetros abaixo para cada uma das colunas:
- Count (contagem);
- Mean (média);
- Std (desvio padrão);
- Min (mínimo);
- Quartis (25%. 50%, 75%);
- Max (máximo).
  
Para as colunas que possuem variáveis qualitativas faremos uma análise e definiremos a melhor transformação dos dados para se tornarem booleanas ou numéricas.

Importante: aqui começamos a ver algumas características, median 50% e mean média estão próximas, indicativo de formato parecido com distribuição normal, está bem distribuída, com comportamento regular.

## Análises Realizadas


O grupo utilizou a ferramenta software Power BI para coletar métricas que auxiliarão nas análises dos pacientes do dataset selecionado. Para elaborar as métricas, foi necessário a utilização da linguagem DAX(Data Analysis Expressions) para criar algumas funções como a média de colesterol dos pacientes envolvidos.

Nesta tabela, os componentes trouxeram um breve detalhamento da média de colesterol dos pacientes. Para realizar o agrupamento dos participantes, foi necessário criar uma coluna condicional através do Power Query, ferramenta ETL para limpeza e preparação de dados do Power BI. Com isso, os pacientes foram separados por sua faixa etária.


![image](/src/images/Colesterol.png)

Segue o código utilizado para se chegar nestas medidas:

![image](/src/images/Colesterol%20Geral.png)

Com essa medida, é realizado o cálculo da média de colesterol e após este procedimento, por meio da função All, os demais filtros serão ignorados dentro do ambiente de desenvolvimento. 


![image](/src/images/Razão%20e%20Proporção.png)

Essa outra medida faz a divisão da média de colesterol das faixas etárias pela média geral de colesterol. Os valores gerados são úteis para se perceber a variação dos itens em relação à tendência central.

## Hipótese 1

Pessoas com colesterol alto possuem mais chance de sofrerem de ataque cardíaco?

Segundo o Dr. Fernando Oliva afirmou que: “O excesso de colesterol é diretamente responsável por formar depósitos de gordura nas artérias, também conhecidos como placa de ateroma, podendo provocar com o tempo obstruções e até mesmo oclusões destes vasos. Consequentemente, os órgãos deixam de receber aporte sanguíneo, deixando de funcionar. No coração, isso é conhecido como infarto”. 

Isso também pode ser mostrado no dataset escolhido pelos componentes, pois 92,51% dos pacientes possuem colesterol alto. Segue um gráfico que mostra o agrupamento desta informação. Basicamente foi adicionado uma coluna adicional no dataset para agrupar pacientes por colesterol alto e baixo(Acima de 160 mg/dL, de acordo com a Unimed) e a contagem dos pacientes do dataset.

![image](/src/images/Pacientes%20por%20%20Nível%20de%20Colesterol.png)

Com isso, conclui-se que o nível de colesterol é um fator importante para causar ataques cardíacos. 

## Hipótese 2

Teste de Hipóteses

Passo 1 : Formulando a Hipótese. 

Teste de hipótese estatístico: A média da pressão arterial é superior a 130 ?  

Hipótese Nula (H₀): A média da pressão arterial é menor ou igual a 130. 
𝐻0: 𝜇 ≤ 130

Hipótese Alternativa (H₁): A média da pressão arterial é superior a 130. 
𝐻1: 𝜇 > 130

Passo 2 : Estabelecendo as Regiões de Aceitação e Rejeição (RA ; RR);

Para realizar o teste, é necessário calcular a média e o desvio padrão da amostra.

Número de dados selecionados (n): 600 

Média da amostra (xˉ) = 147.5 

Desvio padrão da amostra (s) = 20.7 

Utilizando a fórmula: ![image](https://github.com/user-attachments/assets/9121daea-4abd-4f6b-814d-67c55ad6a60d)

t é aproximadamente = 20.7

Passo 3 : Calculando a estatística do teste;

Para um nível de significância  𝛼 de 0.05 , o valor crítico t para uma distribuição t com 599  para uma cauda (direita) é aproximadamente 1.645.

Passo 4 : Concluindo o teste:

Como o valor calculado de t (20.7) é muito maior do que o valor crítico (1.645), é rejeitado a hipótese nula, pois há evidências suficientes para concluir-se que a média da pressão arterial é significativamente superior a 130.

## Descrição dos achados

A partir da análise descrita e exploratória realizada, descreva todos os achados considerados relevantes para o contexto em que o trabalho se insere. Por exemplo: com relação à centralidade dos dados algo chamou a atenção? Foi possível identificar correlação entre os atributos? Que tipo de correlação (forte, fraca, moderada)? 

## Ferramentas utilizadas

Existem muitas ferramentas diferentes que podem ser utilizadas para fazer a análise dos dados. Nesta seção, descreva as ferramentas/tecnologias utilizadas e sua aplicação. Vale destacar que, preferencialmente, as análises deverão ser realizadas utilizando a linguagem de programação Python.


Para algumas das análises, foi utilizado a solução Microsoft Power BI, ferramenta muito conhecida para se realizar análise de dados.

