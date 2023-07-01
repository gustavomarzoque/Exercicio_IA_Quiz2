# Problema do Caixeiro Viajante (Traveling Salesman Problem - TSP) utilizando Algoritmos Genéticos
#### _Gustavo Alvarenga Marzoque - 201910392_
#### Professor: Eric Fernandes de Mello Araújo
#### Disciplina - Inteligência Artificial -Turma 14A - UFLA

 
## Introdução

 Esse código visa resolver ao Problema do Caixeiro Viajante (Traveling Salesman Problem - TSP) usando algoritmos genéticos para otimizar a ordem em que um vendedor
visita um conjunto de cidades, buscando encontrar a rota mais curta possível.


## Sobre o Código

#### Bibliotecas utilizadas:
- numpy
- random
- operator
- pandas
- matpllotlib.pyplot

#### Passo a passo

#####Criação da população inicial:
O código vai ser responsável por criar uma população inicial de rotas, recebendo como entrada o tamanho da população e qual a quantidade de cidades. Vai gerar rotas aleatórias pra cada indivíduo da população.

##### Escolha do parceiro
Vai ser selecionado de maneira aleatória um indivíduo da população como 'parceiro de acasalamento'. Recebe como entrada o número máximo de indivíduos presente na população.

##### Distância
É calculada qual a distância entre duas cidades 'i' e 'j' baseado nas suas coordenadas (x,y).

##### Score da população
É realizado o cálculo da distância total percorrida (aptidão) para cada rota na população. Recebe como entrada a população e uma lista de cidades.

##### Fitness ( Função de aptidão) 
É calculado a aptidão de uma rota específica. É recebido como entrada uma rota e a lista das cidades. Vai ser percorrido toda a rota, realizando o cálculo de qual a distância total percorrida.

##### Criação de um novo membro
É criada uma nova rota aleatória que recebe o número de cidades como entrada. É gerada uma lista com todas as cidades e essa lista é embaralhada para se obter uma nova rota aleatória.

##### Crossover
Realiza-se o operador de crossover entre duas rotas 'a' e 'b'. Seleciona uma parte da rota 'a' e insere essa parte na mesma posicao na rota 'b'. Retorna a nova rota resultante do Crossover.

##### Mutação
É feita a mutação em uma rota, com uma certa probabilidade pra cada posição da rota. Para cada posição, a rota pode ser trocada com outra posição aleatória.

##### Seleção
Seleciona os melhores indivíduos (rotas) da população atual com base em seus rankings e retorna uma lista com os índices dos indivíduos selecionados.

##### Rank Rotas
Calcula o ranking de todas as rotas da população com base em sua aptidão (distância percorrida) e retorna uma lista de tuplas contendo o índice da rota e sua aptidão, ordenadas pelo ranking.

##### Cruzamento 
É realizado o cruzamento entre os indivíduos da população de acasalamento (mating_pool), gerando novos indivíduos através do operador de crossover.

##### Mutação 
Realizada a mutação em uma população de indivíduos (rotas) com uma determinada taxa de mutação, se aplica a função mutate em cada indivíduo da população.

##### Acasalamento
Cria a população de acasalamento (matingpool) com base nos resultados da seleção, e seleciona os indivíduos da população com base nos índices fornecidos.

##### Próxima Geração
Gera a próxima geração de indivíduos. Calculando o ranking da população atual, realiza a seleção dos melhores indivíduos, cria a população de acasalamento, realiza o cruzamento e a mutação para gerar a próxima geração.

##### Algoritmo Genético
Faz a implementação do algoritmo genético completo. Recebe como entrada a lista de cidades, o tamanho da população, o tamanho da elite, a taxa de mutação e o número de gerações. Gera a população inicial, itera através das gerações, realiza a seleção, o cruzamento e a mutação para gerar a próxima geração, e retorna a melhor rota encontrada.

## Experimentação e análise
