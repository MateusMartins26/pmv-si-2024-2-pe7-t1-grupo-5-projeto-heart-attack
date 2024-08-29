# Introdução

Texto descritivo introdutório apresentando a visão geral do projeto a ser desenvolvido considerando o contexto em que ele se insere, os objetivos gerais, a justificativa e o público-alvo do projeto.

## Problema

Através da análise dos dados e identificação dos principais fatores de risco para o desenvolvimento de doenças coronarianas, como o aprendizado de máquina pode auxiliar na melhora da performance médica para prognóstico e posterior diagnóstico em pacientes desse problema de saúde?


## Questão de pesquisa

O que motivou a pesquisa foi a busca por uma análise preditiva que auxilie aos profissionais da saúde a encontrar o melhor tratamento para os pacientes que possuem risco de ataques de coração.



## Objetivos preliminares

Desenvolver um modelo preditivo utilizando técnicas de aprendizado de máquina para estimar com alguma precisão o risco de ocorrência de um doenças coronárias em indivíduos com alguma enfermidade prévia.
Haverá análise dos fatores de risco presentes em um dataset público, identificando quais variáveis influenciam mais o desenvolvimento de doenças coronarianas. 
Definido os fatores e suas respectivas grandezas, será elaborado um modelo preditivo, de modo a contribuir para a tomada de decisões em relação ao tratamento mais adequado por parte dos profissionais de saúde e promoção da saúde cardiovascular dos pacientes.
 

## Justificativa -Lucas 

Descreva a importância ou a motivação para trabalhar com o conjunto de dados escolhido. Indique as razões pelas quais você escolheu seus objetivos específicos, as razões para aprofundar o estudo do problema identificado e qual o impacto que tal problema provoca na sociedade. Lembre-se de quantificar (com dados reais e suas respectivas fontes) este impacto.


## Público-Alvo - Mateus 

O público-alvo são homens e mulheres com idades entre 30 e 89 anos, com ou sem histórico de ataques cardíacos, residentes no Brasil, que desejam verificar se possuem risco de sofrer um ataque cardíaco.

Pendentes - Adicionar Personas

## Estado da arte

Nesta seção, deverão ser descritas outras abordagens identificadas na literatura que foram utilizadas para resolver problemas similares ao problema em questão. Para isso, faça uma pesquisa detalhada e identifique, no mínimo, 5 trabalhos que tenham utilizado dados em contexto similares e então: (a) detalhe e contextualize o problema, (b) descreva as principais características do _dataset_ utilizado, (c) detalhe quais abordagens/algoritmos foram utilizados (e seus parâmetros), (d) identifique as métricas de avaliação empregadas, e (e) fale sobre os resultados obtidos. 

> **Links Úteis**:
> - [Google Scholar](https://scholar.google.com/)
> - [IEEE Xplore](https://ieeexplore.ieee.org/Xplore/home.jsp)
> - [Science Direct](https://www.sciencedirect.com/)
> - [ACM Digital Library](https://dl.acm.org/)

### Android Heart Disease Prediction App ### (Nevon Projects, 2024)

O _Heart Disease Prediction App_, da Nevon Projects, é um projeto voltado para demonstração e aprendizado, geralmente oferecido como um kit para estudantes e desenvolvedores que desejam entender e implementar tecnologias de machine learning em aplicações médicas. Como ferramenta de estudo, ele um exemplo de aplicação móvel projetada para auxiliar os usuários na avaliação do risco de desenvolver doenças cardíacas. Assim como outros aplicativos similares, como o _My Heart_, o _Heart Disease Prediction App_ permite que o usuário insira dados pessoais como idade, gênero, pressão arterial, níveis de colesterol e hábitos de vida, como tabagismo e atividade física. Com base nesses dados, o aplicativo utiliza modelos preditivos, baseados em técnicas de machine learning, para calcular a probabilidade de o usuário desenvolver uma condição cardíaca.

O aplicativo utiliza o _Heart Disease Dataset_ disponível na UCI Machine Learning Repository para realizar suas análises preditivas. Esse dataset é amplamente usado em estudos acadêmicos e aplicações de machine learning para treinar modelos que possam prever o risco de doenças cardíacas com base em dados pessoais dos usuários.

#### Detalhes do Dataset: ####
- Fonte: UCI Machine Learning Repository.
- Objetivo: O objetivo principal do dataset é prever a presença de doenças cardíacas em pacientes, classificando-os em risco alto ou baixo.
- Características: O dataset inclui 14 atributos que são comumente associados ao risco de doenças cardíacas:
1. Age (Idade): Idade do paciente em anos.
2. Sex (Sexo):
    - 1: Masculino
    - 0: Feminino
3. Chest Pain Type (Tipo de Dor no Peito):
    - 1: Angina típica
    - 2: Angina atípica
    - 3: Dor não relacionada à angina
    - 4: Assintomático
4. Resting Blood Pressure (Pressão Arterial em Repouso): Pressão arterial em repouso medida em mm Hg.
5. Serum Cholesterol (Colesterol Sérico): Nível de colesterol sérico em mg/dl.
6. Fasting Blood Sugar (Glicose em Jejum): Se o nível de açúcar no sangue em jejum é maior que 120 mg/dl.
    - 1: Verdadeiro
    - 0: Falso
7. Resting Electrocardiographic Results (Resultados do Eletrocardiograma em Repouso):
    - 0: Normal
    - 1: Anormalidade na onda ST-T (inversão da onda T e/ou elevação ou depressão de ST > 0,05 mV)
    - 2: Hipertrofia ventricular esquerda provável ou definitiva
8. Maximum Heart Rate Achieved (Frequência Cardíaca Máxima Atingida): A frequência cardíaca máxima alcançada durante o teste de esforço.
9. Exercise Induced Angina (Angina Induzida por Exercício):
    - 1: Sim
    - 0: Não
10. ST Depression Induced by Exercise Relative to Rest (Depressão de ST Induzida por Exercício em Relação ao Repouso): Medida da depressão do segmento ST durante o exercício em comparação com o repouso.
11. Slope of the Peak Exercise ST Segment (Inclinação do Segmento ST no Pico do Exercício):
    - 1: Inclinação ascendente
    - 2: Plana
    - 3: Inclinação descendente
12. Number of Major Vessels Colored by Fluoroscopy (Número de Vasos Principais Coloridos por Fluoroscopia): Número de vasos principais (0-3) coloridos por fluoroscopia.
13. Thalassemia (Talassemia):
    - 3: Normal
    - 6: Defeito fixo
    - 7: Defeito reversível
14. Target (Meta): Esta é a variável de saída que indica a presença de doença cardíaca.
    - 0: Não tem doença cardíaca
    - 1: Tem doença cardíaca

O aplicativo utiliza esses dados para treinar modelos de machine learning, que são então empregados para fornecer predições de risco de doenças cardíacas com base nas entradas do usuário.

### Resultados ###

 - **Avaliações de Usuários:** Como o Heart Disease Prediction App da Nevon Projects é voltado para estudantes e desenvolvedores, o feedback frequentemente foca em sua utilidade como ferramenta de aprendizado em vez de seu uso clínico direto. Usuários geralmente consideram o projeto uma boa introdução ao uso de machine learning em saúde.
- **Aplicações Práticas:** Como o aplicativo é mais um protótipo, não há relatos amplamente documentados sobre seu uso em cenários clínicos ou sua aceitação por profissionais de saúde.



### Prevendo Doenças Cardiovasculares com Machine Learning ###
Um estudo sobre predição de doenças cardíacas.

## Objetivo ##
O principal objetivo desta análise é aprimorar minhas habilidades em Análise Exploratória de Dados (AED) como entusiasta no mundo dos dados. Através deste projeto, pretendo trabalhar, crescer e manter minha proficiência em explorar e compreender conjuntos de dados.

## Sobre o problema ##
As doenças cardíacas, uma das principais preocupações globais de saúde, têm sido alvo de estudos aprofundados, e o campo do aprendizado de máquina tem se destacado como uma ferramenta promissora para lidar com essa questão crucial.

## Os dados (variáveis/colunas) ##
Nomes e traduções:

age: idade em anos
sex: sexo (1 = masc 0 = fem)
cp: chest pain type (dor no peito)
Valor 0: asymptomatic (assintomática)
Valor 1: typical angina (típica)
Valor 2: atypical angina (atípica)
Valor 3: non-anginal pain (não anginosa)
trestbps: resting blood pressure (in mm Hg on admission to the hospital) — pressão arterial de repouso (em mm Hg na admissão ao hospital)
chol: serum cholestoral in mg/dl — colesterol sérico em mg/dl
restecg: resting electrocardiographic results (values 0, 1, 2) — Resultados eletrocardiográficos em repouso: Valores 0, 1, 2.
fbs: (fasting blood sugar > 120 mg/dl) (1 = true; 0 = false) — glicemia em jejum
thalach: maximum heart rate achieved — Frequência cardíaca máxima atingida
exang: exercise induced angina (1 = yes; 0 = no) — angina induzida por exercício
oldpeak: ST depression induced by exercise relative to rest — Depressão de ST induzida por exercício em relação ao
slope(inclinação): a inclinação do pico do segmento ST do exercício
Valor 0: inclinação ascendente
Valor 1: plano
Valor 2: descida<br>
ca: number of major vessels (0–3) colored by flouroscopy — Número de vasos principais coloridos por fluoroscopia:
Valor 0: Normal
Valor 1: Com onda ST-T anormal
Valor 2: Mostrando provável (ou definida) hipertrofia do ventrículo esquerdo
thal: 1 = (normal; 2 = fixed defect; 3 = reversable defect)Talassemia:
normal
problema corrigido
problema reversível
target: 0 = não possui doença cardíaca, 1 = possui doença cardíaca
—
Link do Dataset: https://archive.ics.uci.edu/dataset/45/heart+disease

## Conclusão ##
Nesse código gigantesco estudamos algumas variáveis e plots para criarmos modelos de Machine Learning que pudessem prever se, com novas entradas, uma predição assertiva poessa ser feita. Obtivemos bons resultados nas máquinas preditivas mas todo ajuste é bem vindo e o objetivo é aumentar cada mais mais sua capacidade de prever corretamente.

## Fonte ##
**https://medium.com/@jonatasliberato/prevendo-doen%C3%A7as-cardiovasculares-2a2c3dd68789**

# Descrição do _dataset_ selecionado - Marcus

O dataset escolhido para o tema contém atributos pertinentes para criação do modelo para deduzir se um paciente possui ou não o risco de ter um ataque cardíaco. Com isso, a seção do projeto foi elaborada com o fundamento de discorrer e explicar cada um dos atributos do conjunto de dados.


* Gênero: atributo do tipo textual que define se o paciente é um homem ou uma mulher;
* Idade: atributo numérico que determina a idade de cada um dos pacientes apresentados na base de dados;
* Pressão Arterial: de acordo com a UFMG, pressão arterial é a força que o sangue executa contra as paredes da artéria. A partir disso, será possível verificar se os pacientes possuem ou não hipertensão, um fator importante para ataques cardíacos;
* Colesterol: segundo o Hospital Israelita Robert Einstein, colesterol é uma gordura que está no organismo do ser humano, o qual produz hormônios masculinos, femininos e também a vitamina D. Este também é um dos principais fatores para ocorrência de um infarto.
* Se possui ou não diabete: dado booleano que indica basicamente se a pessoa possui ou não diabete.
* Situação sobre fumar: Dado qualitativo que indica se a pessoa fuma por três categorias(Nunca Fumou, fuma atualmente ou se já fumou no passado);
* Tipo de dor no peito: Atributo do tipo textual que indica alguns tipos de dor no peito que os pacientes sentiram.
* Tratamento utilizado: Atributo do tipo textual que mostra os tratamentos recebidos pelos pacientes..


Ao analisar cada um dos atributos desta base de dados, foi possível concluir que não será necessário realizar uma limpeza nos dados, pois não foi encontrado valores inesperados dentro do dataset.

Link para o nosso dataset: https://www.kaggle.com/datasets/waqi786/heart-attack-dataset 



# Canvas analítico

Nesta seção, você deverá estruturar o seu Canvas Analítico. O Canvas Analítico tem o papel de registrar a organização das ideias e apresentar o modelo de negócio. O Canvas Analítico deverá ser preenchido integralmente mesmo que você não tenha "tantas certezas".

> **Links Úteis**:
> - [Modelo do Canvas Analítico](https://github.com/ICEI-PUC-Minas-PMV-SI/PesquisaExperimentacao-Template/blob/main/help/Software-Analtics-Canvas-v1.0.pdf)

# Referências

Nevon Projects. (n.d.). Heart Disease Prediction App. Nevon Projects. Disponível em: https://nevonprojects.com/android-heart-disease-prediction-app/.
UCI Machine Learning Repository. (n.d.). Heart Disease Data Set. Disponível em: https://archive.ics.uci.edu/ml/datasets/heart+disease.


FREESZ, Larissa e PINHEIRO, Paula. ENTENDO A PRESSÃO ARTERIAL. **UFMG**, Minas Gerais, 2011. Disponível em <https://www.ufmg.br/cienciaparatodos/wp-content/uploads/2013/12/pag14-Ciencia.pdf>. Acesso em: 28 de ago. de 2024.

OYAMA, Patrícia. Pressão alta: o maior perigo é a falta de informação. **Abbott**, 2018. Disponível em: <https://www.abbottbrasil.com.br/corpnewsroom/nutrition-health-and-wellness/pressao-alta--o-maior-inimigo-e-a-falta-de-informacao.html#:~:text=Quando%20o%20sangue%20circula%20com,angina%20(dores%20no%20peito)>. Acesso em: 28 de ago. de 2024.

