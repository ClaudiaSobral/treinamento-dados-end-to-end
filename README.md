# Treinamento de Dados end-to-end

Repositório criado para registrar minha evolução durante o desafio de dados. Esse desafio se concentra no dataset [IMDB movies dataset](https://www.kaggle.com/datasets/ashpalsingh1525/imdb-movies-dataset), que pode ser consultado no Kaggle.

19/09 - EDA

Contexto Nosso cliente trabalha com produção e distribuição de filmes e quer entender melhor dois pontos antes de decidir onde investir: o que faz um filme ser bem aceito pelo público e o que faz um filme dar retorno financeiro, e principalmente, onde essas duas coisas não andam juntas. Ele não quer só números soltos. Ele quer saber, com base em dado e em pesquisa, em quem apostar e por quê, porque nota alta não significa dinheiro garantido, e dinheiro garantido não significa reputação garantida. Ele precisa entender essa tensão antes de tomar qualquer decisão. As 8 perguntas abaixo existem pra guiar essa investigação. Elas não pedem uma resposta pronta , pedem que vocês explorem o dataset com intenção, usando as ferramentas que vocês têm (pandas, gráficos).

Bloco 1 - Entendendo o cenário Antes de qualquer recomendação, o cliente quer saber se a equipe entende o que está olhando. Essas duas perguntas servem pra vocês mapearem o terreno: o que influencia a nota de um filme, e, igualmente importante, o que os dados que vocês têm em mãos conseguem (e não conseguem) responder.

Bloco 2 - Aceitação do público Aqui o cliente quer entender por que alguns filmes se destacam de forma consistente aos olhos do público, e se existe algum padrão ligado a quem está por trás da produção, não os atores, mas quem constrói o filme. Se o dataset não tiver essa informação de forma direta, o cliente quer saber: vocês percebem essa lacuna, e sabem como preenchê-la?

Bloco 3 - Retorno financeiro x aceitação Aqui o cliente quer entender os casos em que o dinheiro entrou, mas a reputação não acompanhou, filmes ou franquias que faturaram alto com avaliação mediana ou baixa. Ele quer saber se isso é um padrão (ligado a franquias, sequências, gênero) ou um caso isolado, e principalmente: por que isso acontece,

1PERGUNTAS DE NEGÓCIO Bloco 1

1.Além do gênero, o que mais parece influenciar a nota que um filme recebe do público? 2.Existe alguma coisa nesse dataset que vocês esperavam encontrar e não encontraram? O que vocês fariam se precisassem dela? 

Bloco 2

3.Filmes muito bem avaliados pelo público costumam ter algo em comum entre si, além do gênero e do orçamento?

4.O dataset tem informação sobre quem trabalhou em cada filme. Essa informação é suficiente pra explicar por que alguns filmes se destacam de forma consistente, ou falta alguma coisa?

5.Se existisse um "padrão de sucesso" ligado às pessoas por trás dos filmes (não os atores, mas quem os fez), como vocês descobririam isso com os dados que têm e com os que não têm? Bloco 3

6.Os filmes que mais faturaram são também os mais bem avaliados pelo público? Sempre?

7.O que explicaria um filme (ou uma sequência de filmes) que fatura muito, mas recebe uma nota mediana ou baixa?

8.Filmes que fazem parte de uma mesma série/continuação se comportam de forma parecida entre si em termos de nota e receita, ou cada um é um caso isolado?

9. É natural pensar que quanto maior o orçamento de um filme, melhor deveria ser a nota que ele recebe do público, afinal, mais dinheiro deveria significar mais qualidade. Mas os dados confirmam isso? Qual é essa relação, na prática, e por que ela se comporta desse jeito?

Se uma pergunta não vira gráfico, não significa que vocês erraram ou travaram. Significa que essa pergunta é de um tipo diferente, ela existe pra vocês pensarem, não pra vocês plotarem. E isso também é trabalho de analista: boa parte do raciocínio acontece antes de qualquer gráfico existir.