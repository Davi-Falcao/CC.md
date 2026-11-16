---
tipo: anotacao
periodo: 4
disciplina: Prob
trilhas:
---
## Conceitos Iniciais:

- **Experimentos Determinísticos:**
	- São experimentos os quais quando quando repetidos sob as mesmas condições levam ao mesmo resultado.
- **Experimentos Aleatórios:**
	- São experimentos os quais quando repetidos sob as mesmas condições levam a resultados geralmente diferentes.
	- **Notação:** ϵ. 
- **Espaço Amostral:**
	- **Classificação:** [[Classificação dos Espaços Amostrais|Espaços amostrais discretos e contínuos]].
	- Ao conjunto de **todos os possíveis resultados de um experimento aleatório** damos o nome de espaço amostral.
	- **Notação:** Ω.
	- Exemplo: 
		   $ϵ^1$ : Lança-se um dado e anota-se o número da face superior. 
		   $Ω^1 =\{1, 2, 3, 4, 5, 6\}$.
- **Evento:**
	- Seja **Ω** um **espaço amostral** associado a um **experimento ϵ**. Um **evento** é qualquer subconjunto desse espaço amostral.
	- **Notação:** A, B, C, ...
	- Dizemos que um evento A **ocorre** se o resultado do experimento, ω, pertencer ao evento A (subconjunto A do espaço amostral). Caso contrário, A **não ocorre**.
	- Os subconjuntos **unitários** de **Ω** (espaço amostral) são chamados de **eventos simples**.
	- Como os eventos de um espaço amostral são conjuntos, **todas** as operações da teoria dos conjuntos são válidas para obter novos eventos.

- **Leis de Morgan**:
	- $(A ∪ B)^c = A^c ∩ B^c .$
	- $(A ∩ B)^c = A^c ∪ B^c$.

- **Eventos Mutuamente Excludentes (ou Disjuntos):**
	- Dois eventos A e B são ditos mutuamente excludentes (ou **disjuntos**) se eles não puderem ocorrer simultanemante, ou seja, $A ∩ B = ϕ.$ 
	- **Exemplo:** Considere o fenômeno aleatório que consiste em lançar um dado honesto. Sejam os seguintes eventos: 
		- A: ocorrer um número ímpar; 
		- B: ocorrer um número par; 
		- C: ocorrer um número maior que 3.
		Temos que:
		- A = {1,3,5};
		- B = {2,4,6};
		- C = {4,5,6}.
		Note que:
		- Os eventos A e B são disjuntos, pois $A ∩ B = ϕ$;
		- Os eventos A e C **não** são disjuntos, pois $A \cap B = \{5\} \neq \phi$   
		- Os eventos B e C **não** são disjuntos, pois $A \cap B = \{4,6\} \neq \phi$  

## Exercícios:

- **Exercício 1:**
	- Lança-se um dado e observa-se o número da face superior. Considere este experimento aleatório e os eventos a seguir:
		- $A$: o número da face superior ser par.
		- $B$: o número da face superior ser menor que $4$.
		- $C$: o número da face superior ser menor que $7$.
		- $D$: o número da face superior ser maior que $6$.
	- Determine em notação de conjuntos os seguintes eventos:
		- (a) $A \cup B$.
		- (b) $A \cap B$.
		- (c) $A^c$.
		- (d) $B^c$.
		- (e) $(A \cup B)^c$.
		- (f) $(A \cap B)^c$.
		- (g) $A^c \cup B^c$.
		- (h) $A^c \cap B^c$.
		- (i) $A - B = A \cap B^c$.
		- (j) $B - A = B \cap A^c$.
	- **Resolução:**
		- O espaço amostral associado ao experimento aleatório e os eventos citados podem ser representados pelos seguintes conjuntos:
			- $\Omega = \{1,2,3,4,5,6\}$.
			- $A = \{2,4,6\}$.
			- $B = \{1,2,3\}$.
			- $C = \{1,2,3,4,5,6\}$.
			- $D = \varnothing$.
		- Portanto:
			- (a) $A \cup B = \{1,2,3,4,6\}$.
			- (b) $A \cap B = \{2\}$.
			- (c) $A^c = \{1,3,5\}$.
			- (d) $B^c = \{4,5,6\}$.
			- (e) $(A \cup B)^c = \{5\}$.
			- (f) $(A \cap B)^c = \{1,3,4,5,6\}$.
			- (g) $A^c \cup B^c = \{1,3,4,5,6\} = (A \cap B)^c$.
			- (h) $A^c \cap B^c = \{5\} = (A \cup B)^c$.
			- (i) $A - B = A \cap B^c = \{4,6\}$.
			- (j) $B - A = B \cap A^c = \{1,3\}$.

- **Exercício 2:**
	- Sejam $A$ e $B$ dois eventos de um espaço amostral. Determine expressões em função de $A$ e $B$ para os seguintes eventos:
		- (a) $A$ e $B$ ocorrem simultaneamente;
		- (b) Pelo menos um dos eventos ocorre;
		- (c) Nenhum dos eventos ocorre;
		- (d) Apenas $A$ ocorre;
		- (e) Apenas $B$ ocorre;
		- (f) Exatamente um dos eventos ocorre.
	- **Resolução:**
		- (a): $A \cap B$
		- (b): $A \cup B$
		- (c): $(A \cup B)^c$
		- (d): $A \cap B^c$
		- (e): $A^c \cap B$
		- (f): $(A \cap B^c) \cup (A^c \cap B)$

- **Exercício 3:**
	- Sejam $A$, $B$ e $C$ três eventos de um espaço amostral. Determine expressões em função de $A$, $B$ e $C$ para os seguintes eventos:
		- (a) $A$, $B$ e $C$ ocorrem simultaneamente;
		- (b) Pelo menos um dos eventos ocorre;
		- (c) Nenhum dos eventos ocorre;
		- (d) Apenas $A$ ocorre;
		- (e) Apenas $B$ ocorre;
		- (f) Exatamente um dos eventos ocorre;
		- (g) Pelo menos dois eventos ocorrem;
		- (h) Exatamente dois eventos ocorrem;
		- (i) Não mais do que dois eventos ocorrem;
		- (j) $A$ e $B$ ocorrem mas $C$ não ocorre;
		- (l) $A$ e $C$ ocorrem.
	- **Resolução:**
		- (a): $A \cap B \cap C$
		- (b): $A \cup B \cup C$
		- (c): $(A \cup B \cup C)^c = A^c \cap B^c \cap C^c$
		- (d): $A \cap B^c \cap C^c$
		- (e): $A^c \cap B \cap C^c$
		- (f): $(A \cap B^c \cap C^c) \cup (A^c \cap B \cap C^c) \cup (A^c \cap B^c \cap C)$
		- (g): $(A \cap B) \cup (A \cap C) \cup (B \cap C)$
		- (h): $(A \cap B \cap C^c) \cup (A \cap B^c \cap C) \cup (A^c \cap B \cap C)$
		- (i): $(A \cap B \cap C)^c = A^c \cup B^c \cup C^c$
			- Explicação (i): Não mais do que dois eventos ocorrem significa que o único caso que não ocorre, dado o espaço amostral, são os três simultaneos e o complemento da interseção dos três é, justamente, tudo dentro do espaço amostral menos os três ocorrendo.
		- (j): $A \cap B \cap C^c$
		- (l): $(A \cap C)$
	
>[!cite] Fontes:
> **Slides Professora Grayci Mary - 26.2**
