---
tipo: anotacao
periodo: 4
disciplina: Prob
trilhas:
---
## Probabilidade Condicional:

A questão, como calcular uma probabilidade condicional sem reduzir o espaço amostral ao evento condicionante.
### Definição:

Formalmente, definimos **probabilidade condicional** de $A$ dado a ocorrência de $B$ da seguinte maneira:
$$
P(A|B) = \frac{P(A \cap B)}{P(B)}, \text{desde que } P(B) > 0
$$
Analogamente, a **probabilidade condicional** de $B$ dado a ocorrência de $A$ é:
$$

P(B|A) = \frac{P(A \cap B)}{P(A)}, \text{desde que } P(A) > 0

$$
- *Obs:*
	- A cada evento $A \subset \Omega$ associamos dois números:
		- $P(A)$, a probabilidade *não condicionada* de $A$, chamada de probabilidade **a priori** de $A$;
		- $P(A|B)$, a probabilidade condicionada de $A$, desde que algum evento $B$ (para o qual $P(B) > 0$) tenha ocorrido chamadad de probabilidade **a posteriori** de $A$ dado $B$.
		- A probabilidade *condicional* está definida em termos da probabilidade *não condicionada P*.
		- Em geral, $P(A)$ e $P(A|B)$ são números reais diferentes.
		- Probabilidades condicionais satisfazem todas as propriedades das probabilidades comuns, ou seja, se $A$ e $B$ são eventos quaisquer do espaço amostral $\Omega$, tal que $P(B) > 0$, então:
			- $0 \leq P(A|B) \leq 1$;
			- $P(\Omega|B) = 1$;
				- **Observação:** sabendo que $B$ ocorreu, é certo que o resultado pertence a $\Omega$, pois $B \subseteq \Omega$. Pela definição de probabilidade condicional:
					$$P(\Omega \mid B) = \frac{P(\Omega \cap B)}{P(B)} = \frac{P(B)}{P(B)} = 1.$$
				- Isso ocorre porque $\Omega \cap B = B$ e $P(B) > 0$.
				- **Exemplo:** ao lançar um dado, sabendo que saiu um número par, restam os resultados $\{2,4,6\}$. Todos pertencem a $\Omega = \{1,2,3,4,5,6\}$, então a probabilidade de o resultado estar em $\Omega$ continua sendo $100\%$.
				- **Atenção:** $P(\Omega \mid B)$ não pergunta a chance de $B$ ocorrer; pergunta a chance de o resultado pertencer a $\Omega$, **dado que $B$ já ocorreu**.
			- Se $A_i, i = 1,2,...$ é uma sequência de eventos dois a dois **mutuamente excludentes (disjuntos)**, ou seja, se $A_i \cap  A_j = \phi, \forall i \neq j$  e são eventos quaisquer do espaço amostral $\Omega$, tal que $P(B) > 0$, então:
				$$
				P(A_1 \cup A_2 \cup ...|B) = P(A_1|B) + P(A_2|B) + ...
				$$
### Regra do Produto de Probabilidades:

Da definição de probabilidade condicional, podemos dizer que:
$$P(A \cap B) = P(B) \cdot P(A\mid B), \text{ se } P(B) > 0$$
ou equivalentemente,
$$P(B \cap A) = P(A) \cdot P(B\mid A), \text{ se } P(A) > 0$$
Esse resultado é denominado de **Regra do Produto de Probabilidades**.

### Generalização da Regra do Produto:

Para calcular a probabilidade de **vários eventos ocorrerem juntos**, multiplicamos a probabilidade do primeiro pelas probabilidades dos seguintes, **sempre condicionando à ocorrência de todos os anteriores**.

- **Para três eventos:**
	$$P(A_1 \cap A_2 \cap A_3) = P(A_1) \cdot P(A_2 \mid A_1) \cdot P(A_3 \mid A_1 \cap A_2).$$
	- $P(A_1)$: probabilidade de ocorrer o primeiro evento.
	- $P(A_2 \mid A_1)$: probabilidade de ocorrer o segundo, sabendo que o primeiro ocorreu.
	- $P(A_3 \mid A_1 \cap A_2)$: probabilidade de ocorrer o terceiro, sabendo que **os dois primeiros ocorreram**.
	- **Atenção:** o último fator não é, em geral, $P(A_3 \mid A_2)$, pois precisamos considerar também a informação de que $A_1$ ocorreu.

- **De onde vem a fórmula?**
	- Aplicamos a regra do produto ao evento $A_1 \cap A_2$ e ao evento $A_3$:
		$$P(A_1 \cap A_2 \cap A_3) = P(A_1 \cap A_2) \cdot P(A_3 \mid A_1 \cap A_2).$$
	- Em seguida, substituímos $P(A_1 \cap A_2) = P(A_1) \cdot P(A_2 \mid A_1)$, obtendo a fórmula acima.

- **Para $n$ eventos:**
	$$\begin{aligned}
	P(A_1 \cap A_2 \cap \cdots \cap A_n)
	&= P(A_1) \cdot P(A_2 \mid A_1) \cdot P(A_3 \mid A_1 \cap A_2) \cdots \\
	&\quad \cdot P(A_n \mid A_1 \cap A_2 \cap \cdots \cap A_{n-1}).
	\end{aligned}$$
	- $n$ é a quantidade de eventos. Os pontos $\cdots$ indicam que continuamos o mesmo padrão até o último.
	- **Condição:** cada evento condicionante deve ter probabilidade positiva, isto é, $P(A_1 \cap \cdots \cap A_j) > 0$ para $j = 1,\ldots,n-1$.
	- A condição do slide, $P(A_1 \cap \cdots \cap A_n) \neq 0$, garante isso: se a ocorrência de todos tem probabilidade positiva, a ocorrência de cada grupo inicial também tem. É uma condição suficiente, mas não necessária; o último fator pode ser zero sem invalidar a fórmula.
	- **Não é necessário que os eventos sejam independentes.** As probabilidades condicionais levam em conta a informação dos eventos anteriores.

- Exemplo 1:
	- Uma urna contém $5$ bolas vermelhas e $3$ azuis. Retiramos $3$ bolas sucessivamente, **sem reposição**, com todas as bolas restantes tendo a mesma chance de serem escolhidas. Qual é a probabilidade de as três serem vermelhas?
	- Solução:
		- Definimos $A_i$: a $i$-ésima bola retirada ser vermelha.
		- Na primeira retirada, existem $5$ vermelhas entre $8$ bolas:
			$$P(A_1) = \frac{5}{8}.$$
		- Sabendo que a primeira foi vermelha, restam $4$ vermelhas entre $7$ bolas:
			$$P(A_2 \mid A_1) = \frac{4}{7}.$$
		- Sabendo que as duas primeiras foram vermelhas, restam $3$ vermelhas entre $6$ bolas:
			$$P(A_3 \mid A_1 \cap A_2) = \frac{3}{6}.$$
		- Pela regra do produto:
			$$P(A_1 \cap A_2 \cap A_3) = \frac{5}{8} \cdot \frac{4}{7} \cdot \frac{3}{6} = \frac{5}{28} \simeq 0{,}1786.$$
		- **Intuição:** em cada fator, atualizamos as possibilidades considerando o que já sabemos das retiradas anteriores. Não usamos $\left(\frac{5}{8}\right)^3$, pois as bolas não são repostas.
### Eventos Independentes:

Dois eventos $A$ e $B$ são **independetes** se, e  somente se,
$$P(A\mid B) = P(A)\text{ ou } P(B \mid A) = P(B)$$
De forma equivalente, dizemos que dois eventos $A$ e $B$ são **independentes** se, e somente se,
$$P(A \cap B) = P(A)P(B)$$

*se os eventos são independentes, a probabilidade de ambos ocorrerem é o produto das probabilidades individuais.*

### Independência Coletiva:

Dizemos que os eventos $A$, $B$ e $C$ são (coletivamente) **independentes** se, e somenete se,
- $P(A \cap B) = P(A)P(B)$,
- $P(A \cap C) = P(A)P(C)$,
- $P(B \cap C) = P(B)P(C)$,
- $P(A \cap B \cap C) = P(A)P(B)P(C)$.

*Obs: Se apenas as três primeiras relações acima estiverem satisfeitas, dizemos
que os eventos são independentes aos pares. A definição pode ser estendida facilmente para um número finito qualquer de eventos.*

### Exercícios:

Os exercícios abaixo correspondem aos Exemplos 1 a 5 dos slides de Probabilidade Condicional e Independência.

- Exemplo 1:
	- Considere o lançamento de um dado honesto e os eventos:
		- $A$: sair um número par.
		- $B$: sair um número diferente de $4$.
	- Determine:
		- (a) $P(A)$.
		- (b) $P(B)$.
		- (c) $P(A \cap B)$.
	- Solução:
		- O espaço amostral e os eventos são:
			$$\Omega = \{1,2,3,4,5,6\},\quad A = \{2,4,6\},\quad B = \{1,2,3,5,6\}.$$
		- A interseção contém os resultados que são pares e diferentes de $4$:
			$$A \cap B = \{2,6\}.$$
		- Como o dado é honesto, os resultados são equiprováveis:
			- (a) $P(A) = \frac{\#A}{\#\Omega} = \frac{3}{6} = \frac{1}{2} = 0{,}5$.
			- (b) $P(B) = \frac{\#B}{\#\Omega} = \frac{5}{6} \simeq 0{,}83$.
			- (c) $P(A \cap B) = \frac{\#(A \cap B)}{\#\Omega} = \frac{2}{6} = \frac{1}{3} \simeq 0{,}33$.
		- **Observação:** sabendo que $B$ ocorreu, restam os cinco resultados de $B$, dos quais dois pertencem a $A$. Assim, $P(A \mid B) = \frac{2}{5}$. Se sabemos que $A$ ocorreu, restam três resultados, dos quais dois pertencem a $B$: $P(B \mid A) = \frac{2}{3}$.

- Exemplo 2:
	- No contexto do Exemplo 1, calcule pela definição formal de probabilidade condicional:
		- (a) $P(A \mid B)$.
		- (b) $P(B \mid A)$.
	- Solução:
		- Já sabemos que $P(A) = \frac{3}{6}$, $P(B) = \frac{5}{6}$ e $P(A \cap B) = \frac{2}{6}$.
		- (a) A condição conhecida é $B$, por isso dividimos por $P(B)$:
			$$P(A \mid B) = \frac{P(A \cap B)}{P(B)} = \frac{\frac{2}{6}}{\frac{5}{6}} = \frac{2}{5} = 0{,}4.$$
		- (b) A condição conhecida é $A$, por isso dividimos por $P(A)$:
			$$P(B \mid A) = \frac{P(A \cap B)}{P(A)} = \frac{\frac{2}{6}}{\frac{3}{6}} = \frac{2}{3} \simeq 0{,}67.$$
		- **Observação:** a interseção é a mesma, mas a condição muda o denominador. Por isso, em geral, $P(A \mid B) \neq P(B \mid A)$.
-  Exemplo 3:

	O quadro apresenta os dados de $1000$ ingressantes de uma universidade, classificados por área de estudo e classe socioeconômica:
	- Escolhendo um ingressante ao acaso, determine a probabilidade de:
		- (a) Ser da classe média, dado que estuda na área de exatas.
		- (b) Estudar na área de humanas, sendo da classe alta.
		- (c) Ser da classe baixa, sabendo que estuda na área de saúde.
		
- Solução:
	- (a) A condição restringe a escolha aos $344$ alunos de exatas. Desses, $156$ são da classe média:
		$$P(M \mid E) = \frac{P(M \cap E)}{P(E)} = \frac{\frac{156}{1000}}{\frac{344}{1000}} = \frac{156}{344} \simeq 0{,}45.$$
	- (b) A condição restringe a escolha aos $361$ alunos da classe alta. Desses, $72$ estudam humanas:
		$$P(H \mid A) = \frac{P(H \cap A)}{P(A)} = \frac{\frac{72}{1000}}{\frac{361}{1000}} = \frac{72}{361} \simeq 0{,}20.$$
	- (c) A condição restringe a escolha aos $387$ alunos de saúde. Desses, $73$ são da classe baixa:
		$$P(B \mid S) = \frac{P(B \cap S)}{P(S)} = \frac{\frac{73}{1000}}{\frac{387}{1000}} = \frac{73}{387} \simeq 0{,}19.$$
	- **Intuição:** o denominador corresponde ao total do grupo informado na condição, não ao total de ingressantes.

- Exemplo 4:
	- Um empreiteiro apresentou orçamentos separados para as partes elétrica e hidráulica de um edifício. A probabilidade de ganhar a parte elétrica é $\frac{1}{5}$. Se ganhar a parte elétrica, a probabilidade de ganhar a hidráulica é $\frac{3}{4}$; caso não ganhe a elétrica, essa probabilidade é $\frac{1}{3}$. Calcule a probabilidade de:
		- (a) Ganhar os dois contratos.
		- (b) Ganhar apenas um contrato.
		- (c) Não ganhar contrato algum.
		- (d) Ganhar pelo menos um dos contratos.
	- Solução:
		- Considere os eventos:
			- $E$: ganhar o contrato da parte elétrica.
			- $H$: ganhar o contrato da parte hidráulica.
		- Os dados são:
			$$P(E) = \frac{1}{5},\qquad P(H \mid E) = \frac{3}{4},\qquad P(H \mid E^c) = \frac{1}{3}.$$
		- Pelas probabilidades dos complementares:
			$$P(E^c) = \frac{4}{5},\qquad P(H^c \mid E) = 1 - \frac{3}{4} = \frac{1}{4},\qquad P(H^c \mid E^c) = 1 - \frac{1}{3} = \frac{2}{3}.$$
		- (a) Ganhar os dois corresponde à interseção. Pela regra do produto:
			$$P(E \cap H) = P(E) \cdot P(H \mid E) = \frac{1}{5} \cdot \frac{3}{4} = \frac{3}{20} = 0{,}15.$$
		- (b) Ganhar apenas um significa ganhar somente a elétrica ou somente a hidráulica. Essas possibilidades são disjuntas:
			$$P((E \cap H^c) \cup (E^c \cap H)) = P(E \cap H^c) + P(E^c \cap H).$$
			- Aplicando a regra do produto em cada parcela:
				$$P((E \cap H^c) \cup (E^c \cap H)) = P(E) \cdot P(H^c \mid E) + P(E^c) \cdot P(H \mid E^c).$$
			- Substituindo os valores:
				$$P((E \cap H^c) \cup (E^c \cap H)) = \frac{1}{5} \cdot \frac{1}{4} + \frac{4}{5} \cdot \frac{1}{3} = \frac{1}{20} + \frac{4}{15} = \frac{19}{60} \simeq 0{,}32.$$
		- (c) Não ganhar nenhum significa que $E^c$ e $H^c$ ocorrem juntos:
			$$P(E^c \cap H^c) = P(E^c) \cdot P(H^c \mid E^c) = \frac{4}{5} \cdot \frac{2}{3} = \frac{8}{15} \simeq 0{,}53.$$
		- (d) Ganhar pelo menos um é o complementar de não ganhar nenhum. Pela lei de De Morgan:
			$$P(E \cup H) = 1 - P(E^c \cap H^c) = 1 - \frac{8}{15} = \frac{7}{15} \simeq 0{,}47.$$

- Exemplo 5:
	- A probabilidade de o aluno $A$ resolver um problema é $\frac{5}{8}$, e a de o aluno $B$ resolvê-lo é $\frac{3}{4}$. Ambos tentam **independentemente**. Calcule a probabilidade de:
		- (a) Ambos resolverem o problema.
		- (b) O problema ser resolvido.
		- (c) Apenas $B$ conseguir resolver o problema.
		- (d) Nenhum deles conseguir resolver o problema.
	- Solução:
		- Usaremos $A$ para o evento “o aluno $A$ resolver o problema” e $B$ para o evento “o aluno $B$ resolver o problema”.
		- Temos $P(A) = \frac{5}{8}$ e $P(B) = \frac{3}{4}$, com $A$ e $B$ independentes.
		- (a) Pela independência, a probabilidade de ambos resolverem é o produto das probabilidades individuais:
			$$P(A \cap B) = P(A) \cdot P(B) = \frac{5}{8} \cdot \frac{3}{4} = \frac{15}{32} \simeq 0{,}47.$$
		- (b) O problema ser resolvido significa que pelo menos um deles resolve. Portanto, calculamos a união:
			$$P(A \cup B) = P(A) + P(B) - P(A \cap B) = \frac{5}{8} + \frac{3}{4} - \frac{15}{32} = \frac{29}{32} \simeq 0{,}91.$$
		- (c) Apenas $B$ resolver significa que $B$ ocorre e $A$ não. Retiramos de $B$ a interseção com $A$:
			$$P(A^c \cap B) = P(B) - P(A \cap B) = \frac{3}{4} - \frac{15}{32} = \frac{9}{32} \simeq 0{,}28.$$
			- Pela independência, também podemos escrever:
				$$P(A^c \cap B) = [1 - P(A)] \cdot P(B) = \frac{3}{8} \cdot \frac{3}{4} = \frac{9}{32}.$$
		- (d) Nenhum resolver é o complementar de pelo menos um resolver. Pela lei de De Morgan:
			$$P(A^c \cap B^c) = 1 - P(A \cup B) = 1 - \frac{29}{32} = \frac{3}{32} \simeq 0{,}09.$$
