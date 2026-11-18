---
tipo: anotacao
periodo: 4
disciplina: Prob
trilhas:
---
## Bayes:

### Teorema da Probabilidade Total:

Se $C_1,C_2,...,C_n$ é uma [[Partição do Espaço Amostral|partição do espaço amostral]], $\Omega$ tal que $P(C_j) > 0, \forall j=1,2,...,n$ então qualquer evento $A \subset \Omega$, tem-se
$$
P(A) = P(C_1)P(A \mid C_1) + P(C_2)P(A \mid C_2) + ... + P(C_n)P(A \mid C_n).
$$
Ou seja,
$$
P(A) = \sum_{j=1}^{n}P(C_j)P(A \mid C_j).
$$
*Comentário: O Teorema da Probabilidade Total nos mostra como obter a probabilidade a **priori** de um evento $A$ em termos das probabilidades a **posteriori** de $A$ dado a ocorrência dos eventos $C_1,C_2,...,C_n$ quando estes constituem uma partição do espaço amostral $\Omega$* 
### Teorema de Bayes:

Se $C_1,C_2,...,C_n$ é uma partição do espaço amostral $\Omega$ tal que $P(C_j) > 0, \forall j = 1,2,...,n$ e $A$ é um evento de $\Omega \mid P(A) > 0$, então 
$$P(C_i\mid A) = \frac{P(C_i)P(A\mid C_i)}{\sum_{j=1}^{n}P(C_j)P(A \mid C_j)},\forall i = 1,2,...,n$$
