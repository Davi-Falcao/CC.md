---
tipo: anotacao
periodo: 4
disciplina: Prob
trilhas:
---
\## Abordagem Clássica:

### Modelo Probabilístico:

Todo fenômeno aleatório terá seu modelo probabilístico especificado quando estabelecermos:
- Um **espaço amostral**, $\Omega$, que consiste, no **caso discreto**, da enumeração (finita ou infinita) de todos os possíveis resultados do fenômeno em questão 
- $\Omega = \{\ \omega_1,\omega_2,...,\omega_n\}$ .
- Uma **probabilidade**, $P(\omega_i)$, para cada ponto amostral $\omega_i$, de modo que seja possível encontrar a probabilidade $P(A)$ de qualquer subconjunto (**evento**) A de $\Omega$.
### Abordagem Clássica:

Se $\Omega$ for um **Espaço Finito e Equiprovável** (Definição: [[Classificação dos Espaços Amostrais]]) podemos utilizar a **abordagem clássica** para definir a probabilidade de um evento $A \subset \Omega$.
- **Definição Clássica de Probabilidade:**
	Seja $\Omega$ um espaço amostral **finito**, $\Omega = \{\omega_1,...,\omega_n\}$, em que todos os pontos amostrais têm **mesma probabilidade** $\frac{1}{n}$, ou seja, um espaço finito e equiprovável. se $A$ for um evento com $m$ pontos amostrais, então:
	$$P(A) = \frac{\text{número de casos favoráveis à ocorrência do evento A}}{\text{número de casos possíveis}} = \frac{m}{n} = \frac{\#A}{\#\Omega}.$$
	*obs: a $\#$ antes do conjunto significa Cardinalidade, quantidade de elementos dentro do conjunto.*

- Exemplo 1:
	- Considere o lançamento de dois dados honestos. Considere os seguintes eventos:
		- $A$: soma dos números obtidos igual a $9$;
		- $B$: número no primeiro dado maior do que o segundo.
	- (a) Enumere os elementos de $A$, $B$, $A \cap B$ e $A \cup B$.
	- (b) Calcule a probabilidade dos eventos dados no item (a).
	- Solução:
		-  $\Omega = \{(1,1);(1,2);...(1,6);(2,1);(2,2);...;(6,1);(6,2),...,(6,6)\}; \#\Omega = 36$. 
		- (a): 
			- $A = \{(3,6);(4,5);(5,4);(6,3)\}$; 
			- $B=\{(2, 1); (3, 1); (4, 1); (5, 1); (6, 1); (3, 2); (4, 2); (5, 2); (6, 2); (4, 3);(5, 3); (6, 3); (5, 4); (6, 4); (6, 5)\}$;
			- $A \cap B = \{(5,4);(6,3)\}$;
			- $A \cup B = \{(2, 1); (3, 1); (3,6); (4, 1); (5, 1); (6, 1); (3, 2); (4, 2); (4,5); (5, 2); (6, 2); (4, 3);(5, 3); (6, 3); (5, 4); (6, 4); (6, 5)\}$.
		- (b):
			- $P(A) = \frac{\#A}{\#\Omega}= \frac{4}{36}$ .
			- $P(B) = \frac{15}{36}$
			- $P(A \cap B) = \frac{2}{36}$
			- $P(A \cup B) = \frac{17}{36}$

### Ferramentas de Contagem:

Existem várias ferramentas de Análise Combinatória que nós ajudam a **contar** o número de elementos de certos conjuntos, sem a necessidade de listar (exibir) os elementos, por exemplo:

- Príncipio Multiplicativo ou Princípio Fundamental da Contagem;
- Príncipio Aditivo,
- Permutações,
- Arranjos,
- Combinações.

dentre outras.

### Combinação Simples:

Dentre as ferramentas citadas, daremos ênfase às Combinações Simples.

- A quantidade de **subconjuntos** com k elementos do conjunto $\{a_1,a_2,...,a_n\}$ é dada por:
	$$\binom{n}{k} = \frac{n!}{k!(n-k)!}$$
	Ou seja, é o número de maneiras de escolher $k$  objetos distintos dentre $n$ objetos distintos.
	*Obs: Lê-se "combinação simples de $n$ elementos tomados $k$ a $k$"* 
- Exemplo 2:
	- Uma empresa é formada por 10 sócios brasileiros e 5 japoneses.
		- (a) De quantos modos podemos formar uma diretoria de 6 sócios?
		- (b) Calcule a probabilidade de formar uma diretoria de 6 sócios, sendo 4
		 brasileiros e 2 japoneses.
	- Solução:
		- (a)