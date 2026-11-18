---
tipo: anotacao
periodo: 4
disciplina: Prob
trilhas:
---
## Abordagem Axiomática:

## Definição Axiomática de Probabilidade

Considere um experimento cujo espaço amostral é $\Omega$. Para cada evento $A$ do espaço amostral $\Omega$, associaremos um número real, representado por $P(A)$ e denominado *probabilidade* de $A$, que satisfaça os três axiomas a seguir:
- **Axioma 1:** $0 \leq P(A) \leq 1$; 
- **Axioma 2:** $P(\Omega) = 1$.
- **Axioma 3:** Se $A_1,A_2,...$ é uma sequência de eventos dois a dois **mutuamente excludentes** (ou **disjuntos**), ou seja $A_i \cap A_j = \phi$, $\forall i \neq j$, então $P(A_1 \cup A_2 \cup ...) = P(A_1) + P(A_2) + ...$ 
### Propriedades:

Seja $A$ e $B$ eventos quaisquer contidos em um espaço amostral $\Omega$.

- (P1): $P(\varnothing) = 0$.
- (P2): $P(A^c) = 1 - P(A)$.
- (P3): $P(A \cap B^c) = P(A) - P(A \cap B)$.
- (P4): $P(A^c \cap B) = P(B) - P(A \cap B)$.
- (P5): $P(A \cup B) = P(A) + P(B) - P(A \cap B)$.

### Demonstrações das Propriedades:

- **(P1): Probabilidade do evento vazio.**
	- O evento vazio não altera a união com $\Omega$ e é disjunto dele:
		$$\Omega \cup \varnothing = \Omega,\qquad \Omega \cap \varnothing = \varnothing.$$
	- Pelo Axioma 3, somamos as probabilidades desses eventos disjuntos:
		$$P(\Omega) = P(\Omega \cup \varnothing) = P(\Omega) + P(\varnothing).$$
	- Como $P(\Omega) = 1$, pelo Axioma 2:
		$$1 = 1 + P(\varnothing) \quad \Rightarrow \quad P(\varnothing) = 0.$$
	- **Intuição:** o evento vazio não possui nenhum resultado possível, logo é um evento impossível.

- **(P2): Probabilidade do evento complementar.**
	- O evento $A$ e seu complementar $A^c$ cobrem todo o espaço amostral e são disjuntos:
		$$\Omega = A \cup A^c,\qquad A \cap A^c = \varnothing.$$
	- Pelo Axioma 2, $P(\Omega) = 1$. Pelo Axioma 3, podemos somar as probabilidades desses eventos disjuntos:
		$$1 = P(\Omega) = P(A \cup A^c) = P(A) + P(A^c).$$
	- Isolando $P(A^c)$, obtemos:
		$$P(A^c) = 1 - P(A).$$
	- **Intuição:** subtrair a probabilidade de $A$ de $1$ (equivalente a $100\%$) deixa a probabilidade de tudo que não é $A$ dentro do espaço amostral, isto é, de $A^c$.

- **(P3): Probabilidade da parte de $A$ que está fora de $B$.**
	- Podemos dividir $A$ em duas partes: a que está **fora de $B$**, $A \cap B^c$, e a que está **dentro de $B$**, $A \cap B$:
		$$A = (A \cap B^c) \cup (A \cap B).$$
	- Essas partes são disjuntas, pois nenhum resultado pode pertencer a $B$ e a $B^c$ ao mesmo tempo. Pelo Axioma 3:
		$$P(A) = P(A \cap B^c) + P(A \cap B).$$
	- Isolando a probabilidade da parte de $A$ que está fora de $B$:
		$$P(A \cap B^c) = P(A) - P(A \cap B).$$

- **(P4): Probabilidade da parte de $B$ que está fora de $A$.**
	- Podemos dividir $B$ em duas partes: a que está **fora de $A$**, $A^c \cap B$, e a que está **dentro de $A$**, $A \cap B$:
		$$B = (A^c \cap B) \cup (A \cap B).$$
	- Essas partes são disjuntas. Pelo Axioma 3:
		$$P(B) = P(A^c \cap B) + P(A \cap B).$$
	- Isolando a probabilidade da parte de $B$ que está fora de $A$:
		$$P(A^c \cap B) = P(B) - P(A \cap B).$$
	- **Observação:** é o mesmo raciocínio de (P3), trocando os papéis de $A$ e $B$.

- **(P5): Probabilidade da união de dois eventos.**
	- Podemos dividir $A \cup B$ em três partes disjuntas: **somente $A$**, **a interseção** e **somente $B$**:
		$$A \cup B = (A \cap B^c) \cup (A \cap B) \cup (A^c \cap B).$$
	- Pelo Axioma 3, a probabilidade da união é a soma das probabilidades dessas partes:
		$$P(A \cup B) = P(A \cap B^c) + P(A \cap B) + P(A^c \cap B).$$
	- Substituindo as propriedades (P3) e (P4):
		$$P(A \cup B) = \bigl[P(A) - P(A \cap B)\bigr] + P(A \cap B) + \bigl[P(B) - P(A \cap B)\bigr].$$
	- Simplificando, obtemos:
		$$P(A \cup B) = P(A) + P(B) - P(A \cap B).$$
	- **Intuição:** ao somar $P(A) + P(B)$, contamos a interseção duas vezes. Subtraímos $P(A \cap B)$ uma vez para corrigir essa contagem.

### Exemplos:

- Exemplo 1:
	- Considere um experimento aleatório com espaço amostral $\Omega$ e os eventos $A \subseteq \Omega$ e $B \subseteq \Omega$, tais que:
		$$P(A) = \frac{2}{5},\qquad P(B) = \frac{1}{3},\qquad P(A \cap B) = \frac{1}{8}.$$
	- Determine:
		- (a) $P(A^c)$.
		- (b) $P(B^c)$.
		- (c) $P(A \cup B)$.
		- (d) $P(A^c \cap B^c)$.
		- (e) $P(A^c \cup B^c)$.
		- (f) $P(A \cap B^c)$.
		- (g) $P(A^c \cup B)$.
	- Solução:
		- (a) Utilizando a propriedade (P2):
			$$P(A^c) = 1 - P(A) = 1 - \frac{2}{5} = \frac{3}{5} = 0{,}6.$$
		- (b) Utilizando a propriedade (P2):
			$$P(B^c) = 1 - P(B) = 1 - \frac{1}{3} = \frac{2}{3} \simeq 0{,}67.$$
		- (c) Utilizando a propriedade (P5):
			$$P(A \cup B) = P(A) + P(B) - P(A \cap B) = \frac{2}{5} + \frac{1}{3} - \frac{1}{8} = \frac{73}{120} \simeq 0{,}61.$$
		- (d) Pela lei de De Morgan, $A^c \cap B^c = (A \cup B)^c$. Aplicando (P2) e o resultado do item (c):
			$$P(A^c \cap B^c) = 1 - P(A \cup B) = 1 - \frac{73}{120} = \frac{47}{120} \simeq 0{,}39.$$
		- (e) Pela lei de De Morgan, $A^c \cup B^c = (A \cap B)^c$. Aplicando (P2):
			$$P(A^c \cup B^c) = 1 - P(A \cap B) = 1 - \frac{1}{8} = \frac{7}{8} = 0{,}875.$$
		- (f) Utilizando a propriedade (P3):
			$$P(A \cap B^c) = P(A) - P(A \cap B) = \frac{2}{5} - \frac{1}{8} = \frac{11}{40} = 0{,}275.$$
		- (g) Utilizando a propriedade (P5):
			$$P(A^c \cup B) = P(A^c) + P(B) - P(A^c \cap B).$$
			- Aplicando (P2) e (P4):
				$$P(A^c \cup B) = [1 - P(A)] + P(B) - [P(B) - P(A \cap B)].$$
			- Simplificando e substituindo os valores:
				$$P(A^c \cup B) = 1 - P(A) + P(A \cap B) = 1 - \frac{2}{5} + \frac{1}{8} = \frac{29}{40} = 0{,}725.$$

- Exemplo 2:
	- Pedro leva dois livros para ler durante as férias. A probabilidade de gostar do primeiro livro é $0{,}7$, de gostar do segundo é $0{,}4$ e de gostar de ambos é $0{,}3$. Calcule a probabilidade de que ele:
		- (a) Goste de pelo menos um dos livros.
		- (b) Não goste nem do primeiro nem do segundo livro.
		- (c) Goste apenas do primeiro livro.
		- (d) Goste de exatamente um dos livros.
	- Solução:
		- Considere os eventos:
			- $A$: Pedro gostar do primeiro livro.
			- $B$: Pedro gostar do segundo livro.
		- Temos $P(A) = 0{,}7$, $P(B) = 0{,}4$ e $P(A \cap B) = 0{,}3$.
		- (a) Gostar de **pelo menos um** significa gostar do primeiro, do segundo ou de ambos. Portanto, queremos $P(A \cup B)$. Pela propriedade (P5):
			$$P(A \cup B) = P(A) + P(B) - P(A \cap B) = 0{,}7 + 0{,}4 - 0{,}3 = 0{,}8.$$
		- (b) Não gostar de nenhum é o complementar de gostar de pelo menos um. Pela lei de De Morgan e pela propriedade (P2):
			$$P(A^c \cap B^c) = P((A \cup B)^c) = 1 - P(A \cup B) = 1 - 0{,}8 = 0{,}2.$$
		- (c) Gostar apenas do primeiro significa que $A$ ocorre, mas $B$ não. Pela propriedade (P3):
			$$P(A \cap B^c) = P(A) - P(A \cap B) = 0{,}7 - 0{,}3 = 0{,}4.$$
		- (d) Gostar de **exatamente um** significa gostar apenas do primeiro ou apenas do segundo. Esses eventos são disjuntos, então, pelo Axioma 3:
			$$P((A \cap B^c) \cup (A^c \cap B)) = P(A \cap B^c) + P(A^c \cap B).$$
			- Utilizando (P3) e (P4), calculamos separadamente:
				- **Apenas o primeiro:**
					$$P(A \cap B^c) = P(A) - P(A \cap B).$$
				- **Apenas o segundo:**
					$$P(A^c \cap B) = P(B) - P(A \cap B).$$
			- Somando as duas parcelas:
				$$P((A \cap B^c) \cup (A^c \cap B)) = [P(A) - P(A \cap B)] + [P(B) - P(A \cap B)].$$
			- O termo $2P(A \cap B)$ aparece porque subtraímos $P(A \cap B)$ **uma vez em cada parcela**, ou seja, duas vezes:
				$$P((A \cap B^c) \cup (A^c \cap B)) = P(A) + P(B) - 2P(A \cap B).$$
			- **Intuição:** em $P(A) + P(B)$, a situação em que Pedro gosta dos dois livros é contada duas vezes. Como queremos **exatamente um**, essa situação não deve ser contada nenhuma vez; por isso, retiramos as duas contagens.
			- Substituindo os valores:
				$$P((A \cap B^c) \cup (A^c \cap B)) = 0{,}7 + 0{,}4 - 2 \cdot 0{,}3 = 0{,}5.$$
			- Também podemos visualizar o cálculo pelas duas possibilidades:
				$$P((A \cap B^c) \cup (A^c \cap B)) = (0{,}7 - 0{,}3) + (0{,}4 - 0{,}3) = 0{,}4 + 0{,}1 = 0{,}5.$$
