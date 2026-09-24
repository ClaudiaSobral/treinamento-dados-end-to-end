# Treinamento de Dados end-to-end

Repositório criado para registrar minha evolução durante o desafio de dados. Esse desafio se concentra no dataset [IMDB movies dataset](https://www.kaggle.com/datasets/ashpalsingh1525/imdb-movies-dataset), que pode ser consultado no Kaggle.

19/09 - EDA
26/09 - Tira-dúvidas
03/10 - Apresentação

Estrutura do repositório


    treinamento-dados-end-to-end
    ├── anotacoes
    ├── apresentacao
    ├── notebooks
    └── src


## O passo a passo

### Estatística resumida e verificação da integridade do dataset

- Primeiramente, verifiquei as 5 primeiras linhas do dataset com o método .head(). Percebi que o dataset contém: nomes de filmes, data, score do IMDB, gênero, sinopse, elenco, título original, status de lançamento, linguagem de origem, orçamento, faturamento e país (sigla)

- Através do método .info(), percebi que o dataset contém 10178 linhas. Há nulos na coluna de gênero (85) e elenco (56). Não há duplicatas. No geral, o dataset aparenta não precisar de muito tratamento.

- Verifiquei a tipagem dos dados e, a primeira vista, apenas data parece estar incorreta como objeto. O formato está em mm/dd/aaaa.

- Apesar de estarem na tipagem correta, a coluna "genre" pode conter mais de um gênero. A coluna "crew" também contém nomes dos atores e dos personagens separados por vírgula.

> Nesse momento, considero que vou precisar dar atenção específica a "date_x", "genre" e "crew"

## Investigação pessoal para entender o dataset

- Em seguida, pesquisei alguns filmes de minha preferência para ver até onde vai o dataset. Primeiramente, busquei se o dataset continha algum filme d"Os Trapalhões" (nacional e antigo). Cinderela Baiana também não estava lá. Depois, "Cidade de Deus" (nacional porém célebre no exterior). Estava! Qual critério?

Depois, pesquisei por "The Room", americano e independente. Não estava lá.

Então procurei por alguns filmes do diretor americano David Lynch. Fire Walk with Me, sequência da série Twin Peaks estava lá (célebre porém cult). Para tirar a dúvida, busquei por "Eraserhead", um filme um pouco mais obscuro do diretor. Estava lá também.

- Depois, fiz o processo inverso: procurei por alguns filmes contidos no cabeçalho do dataset. Creed III consta com score 73.0 no dataset, mas 6.7 no IMDB. Avatar: The Way of Water está com 78.0 no dataset e 7.5 no IMDB. São valores relativamente próximos, o que me leva a crer que só não está atualizado.


- Fiz o tratamento de datas e voltei a investigar o critério de escolha dos filmes. Ainda não ficou claro o porquê de alguns filmes estarem e outros não, mas provavelmente a pessoa que elaborou o dataset optou por não colocar alguns filmes com NaNs e principalmente não colocar filmes obscuros demais.


### Onde eu tropecei

- Procurei filme nacional pela coluna name_x. Obviamente não apareceu.
- Tentei converter as datas do formato string para o formato dd-mm-aaaa. Tinha um espaço extra na coluna original de datas. Tratei o espaço, mas acabei convertendo datetime[us], por ser o formato 