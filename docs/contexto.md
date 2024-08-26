# Introdução

Texto descritivo introdutório apresentando a visão geral do projeto a ser desenvolvido considerando o contexto em que ele se insere, os objetivos gerais, a justificativa e o público-alvo do projeto.

## Problema

Nesta seção, você deve apresentar o problema que a sua investigação/experimentação busca resolver. Por exemplo, caso o _dataset_ selecionado, seja um _dataset_ que contenha uma série temporal com o preço de diversas ações da bolsa de valores, o problema pode estar relacionado a dificuldade em saber a melhor hora (hora certa??) de comprar ou então, de executar a venda de uma determinada ação.

Descreva ainda o contexto em que essa aplicação será usada, se houver: empresa parceira, tecnologias etc. Novamente, descreva apenas o que de fato existir, pois ainda não é a hora de apresentar requisitos  detalhados ou projetos.

> **Links Úteis**:
> - [Objetivos, Problema de pesquisa e Justificativa](https://medium.com/@versioparole/objetivos-problema-de-pesquisa-e-justificativa-c98c8233b9c3)
> - [Matriz Certezas, Suposições e Dúvidas](https://medium.com/educa%C3%A7%C3%A3o-fora-da-caixa/matriz-certezas-suposi%C3%A7%C3%B5es-e-d%C3%BAvidas-fa2263633655)
> - [Brainstorming](https://www.euax.com.br/2018/09/brainstorming/)

## Questão de pesquisa

A questão de pesquisa é a base de todo o trabalho que será desenvolvido. É ela que motiva a realização da pesquisa e deverá ser adequada ao problema identificado. Ao término de sua pesquisa/experimentação, o objetivo é que seja encontrada a resposta da questão de pesquisa previamente definida.

> **Links Úteis**:
> - [Questão de pesquisa](https://www.enago.com.br/academy/how-to-develop-good-research-question-types-examples/)
> - [Problema de pesquisa](https://blog.even3.com.br/problema-de-pesquisa/)

## Objetivos preliminares

Aqui você deve descrever os objetivos preliminares do trabalho indicando que o objetivo geral é experimentar modelos de aprendizado de máquina adequados para solucionar o problema apresentado acima. 

Apresente também alguns (pelo menos 2) objetivos específicos dependendo de onde você vai querer concentrar a sua prática investigativa, ou como você vai aprofundar no seu trabalho.

Por exemplo: um objetivo específico pode estar relacionado a predizer a tendência de alta, estabilidade ou queda de uma determinada ação em uma determinada janela do tempo ou então, predizer o valor exato de uma determinada ação.
Lembre-se que, à medida que a pesquisa/experimentação evolui, os objetivos podem evoluir também, portanto, não se esqueça de fazer as atualizações necessárias.
 
> **Links Úteis**:
> - [Objetivo geral e objetivo específico: como fazer e quais verbos utilizar](https://blog.mettzer.com/diferenca-entre-objetivo-geral-e-objetivo-especifico/)

## Justificativa -Lucas 

Descreva a importância ou a motivação para trabalhar com o conjunto de dados escolhido. Indique as razões pelas quais você escolheu seus objetivos específicos, as razões para aprofundar o estudo do problema identificado e qual o impacto que tal problema provoca na sociedade. Lembre-se de quantificar (com dados reais e suas respectivas fontes) este impacto.

> **Links Úteis**:
> - [Como montar a justificativa](https://guiadamonografia.com.br/como-montar-justificativa-do-tcc/)

## Público-Alvo - Mateus 

Descreva quem serão as pessoas que poderão se beneficiar com a sua investigação indicando os diferentes perfis. O objetivo aqui não é definir quem serão os clientes ou quais serão os papéis dos usuários na aplicação. A ideia é, dentro do possível, conhecer um pouco mais sobre o perfil dos usuários: conhecimentos prévios, relação com a tecnologia, relações hierárquicas, etc.

Adicione informações sobre o público-alvo por meio de uma descrição textual, diagramas de personas e mapa de stakeholders.

> **Links Úteis**:
> - [Público-alvo](https://blog.hotmart.com/pt-br/publico-alvo/)
> - [Como definir o público alvo](https://exame.com/pme/5-dicas-essenciais-para-definir-o-publico-alvo-do-seu-negocio/)
> - [Público-alvo: o que é, tipos, como definir seu público e exemplos](https://klickpages.com.br/blog/publico-alvo-o-que-e/)
> - [Qual a diferença entre público-alvo e persona?](https://rockcontent.com/blog/diferenca-publico-alvo-e-persona/)

## Estado da arte

Nesta seção, deverão ser descritas outras abordagens identificadas na literatura que foram utilizadas para resolver problemas similares ao problema em questão. Para isso, faça uma pesquisa detalhada e identifique, no mínimo, 5 trabalhos que tenham utilizado dados em contexto similares e então: (a) detalhe e contextualize o problema, (b) descreva as principais características do _dataset_ utilizado, (c) detalhe quais abordagens/algoritmos foram utilizados (e seus parâmetros), (d) identifique as métricas de avaliação empregadas, e (e) fale sobre os resultados obtidos. 

> **Links Úteis**:
> - [Google Scholar](https://scholar.google.com/)
> - [IEEE Xplore](https://ieeexplore.ieee.org/Xplore/home.jsp)
> - [Science Direct](https://www.sciencedirect.com/)
> - [ACM Digital Library](https://dl.acm.org/)

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


chrome-extension://efaidnbmnnnibpcajpcglclefindmkaj/https://www.ufmg.br/cienciaparatodos/wp-content/uploads/2013/12/pag14-Ciencia.pdf 22/08/2024 às 20:23

https://www.abbottbrasil.com.br/corpnewsroom/nutrition-health-and-wellness/pressao-alta--o-maior-inimigo-e-a-falta-de-informacao.html#:~:text=Quando%20o%20sangue%20circula%20com,angina%20(dores%20no%20peito). 22/08/2024


# Canvas analítico

Nesta seção, você deverá estruturar o seu Canvas Analítico. O Canvas Analítico tem o papel de registrar a organização das ideias e apresentar o modelo de negócio. O Canvas Analítico deverá ser preenchido integralmente mesmo que você não tenha "tantas certezas".

> **Links Úteis**:
> - [Modelo do Canvas Analítico](https://github.com/ICEI-PUC-Minas-PMV-SI/PesquisaExperimentacao-Template/blob/main/help/Software-Analtics-Canvas-v1.0.pdf)

# Referências

Inclua todas as referências (livros, artigos, sites, etc) utilizados no desenvolvimento do trabalho utilizando o padrão ABNT.

> **Links Úteis**:
> - [Padrão ABNT PUC Minas](https://portal.pucminas.br/biblioteca/index_padrao.php?pagina=5886)
