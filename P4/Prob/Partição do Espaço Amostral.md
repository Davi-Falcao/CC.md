---
tipo: anotacao
periodo: 4
disciplina: Prob
trilhas: []
---

# Partição do Espaço Amostral

## Em poucas palavras

Uma **partição do espaço amostral** $\Omega$ é uma coleção de eventos não vazios que divide todos os resultados possíveis em grupos **sem sobreposição e sem deixar nenhum resultado de fora**.

Para uma partição finita $C_1,C_2,\ldots,C_n$, temos:

- **Cada grupo é não vazio:** $C_j \neq \varnothing$.
- **Os grupos são dois a dois disjuntos:**
	$$C_i \cap C_j = \varnothing,\qquad \forall i \neq j.$$
- **Juntos, os grupos cobrem todo o espaço amostral:**
	$$C_1 \cup C_2 \cup \cdots \cup C_n = \Omega.$$

**Ideia-chave:** cada resultado de $\Omega$ pertence a **exatamente um** grupo da partição. Não precisamos reunir todos os eventos disjuntos possíveis; basta escolher grupos que satisfaçam essas condições.

## Entendendo na prática

- **Exemplo: lançamento de um dado.**
	- O espaço amostral é $\Omega = \{1,2,3,4,5,6\}$.
	- Podemos dividi-lo em:
		$$C_1 = \{1,3,5\},\qquad C_2 = \{2,4,6\}.$$
	- Esses eventos formam uma partição: nenhum número é simultaneamente par e ímpar, e todo resultado do dado pertence a um desses grupos.
	- A partição não é única. Outra possibilidade é:
		$$D_1 = \{1,2\},\qquad D_2 = \{3,4\},\qquad D_3 = \{5,6\}.$$
	- **Contraexemplo:** apenas $\{1,2\}$ e $\{3,4\}$ não formam uma partição de $\Omega$. São disjuntos, mas deixam os resultados $5$ e $6$ de fora.

- **Disjuntos não significa independentes.**
	- Disjuntos não podem ocorrer juntos; independentes não alteram a probabilidade um do outro.
	- No dado honesto, $C_1$ e $C_2$ são disjuntos, mas não independentes:
		$$P(C_1 \cap C_2) = 0 \neq P(C_1) \cdot P(C_2) = \frac{1}{4}.$$
	- Saber que saiu um número ímpar torna impossível ter saído um número par.

### Relação com o Teorema da Probabilidade Total

Para calcular a probabilidade de um evento $A$, podemos separar sua ocorrência conforme os grupos da partição:

$$A = (A \cap C_1) \cup (A \cap C_2) \cup \cdots \cup (A \cap C_n).$$

Essas partes são disjuntas, então suas probabilidades podem ser somadas. Se $P(C_j) > 0$ para todo $j$, aplicamos a regra do produto:

$$P(A) = \sum_{j=1}^{n} P(A \cap C_j) = \sum_{j=1}^{n} P(C_j) \cdot P(A \mid C_j).$$

**Intuição:** calculamos a contribuição de cada grupo para a ocorrência de $A$ e somamos todas elas.

**Observação:** exigir $P(C_j) > 0$ permite definir as probabilidades condicionais. Essa é uma condição adicional do teorema nessa forma, não da definição de partição: um evento não vazio pode ter probabilidade zero.

## Conexões

- [[Teoria das Probabilidades - Bayes]] — utiliza partições no Teorema da Probabilidade Total.
- [[Teoria das Probabilidades - Probabilidade Condicional]] — explica a regra do produto e a diferença entre eventos disjuntos e independentes.
- [[Teoria das Probabilidades - Conceitos Iniciais]] — apresenta espaço amostral, eventos e operações com conjuntos.
