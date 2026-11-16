---
tipo: anotacao
periodo: 4
disciplina: Prob
trilhas:
---
## Classificação dos Espaços Amostrais:

- **Espaço Amostral:**
	- É o conjunto de todos os resultados possíveis de um experimento aleatório, representado por $\Omega$.
	- Veja também: [[Teoria das Probabilidades - Conceitos Iniciais#Conceitos Iniciais:|Conceitos iniciais de probabilidade]].

- **Espaço Amostral Discreto:**
	- Os resultados possíveis podem ser **enumerados um a um**, em uma lista finita ou infinita.
	- **Finito:**
		- Possui uma quantidade limitada de resultados possíveis.
		- Exemplo: lançar um dado e observar a face superior.
		- $\Omega = \{1,2,3,4,5,6\}$.
	- **Infinito enumerável:**
		- Exemplo: lançar uma moeda até obter a primeira cara e contar o número de lançamentos.
		- $\Omega = \{1,2,3,4,\ldots\}$.
		- Não há um limite para a quantidade de lançamentos, mas os resultados podem ser listados: $1$, $2$, $3$, e assim por diante.
	- **Importante:** discreto não significa necessariamente finito.

- **Espaço Amostral Contínuo:**
	- Em exemplos usuais, os resultados podem assumir **qualquer valor de um intervalo**, não sendo possível enumerá-los um a um.
	- Exemplo: medir o tempo de espera até a chegada de uma pessoa.
	- Considerando qualquer tempo não negativo, $\Omega = [0,+\infty)$.
	- O tempo pode ser $2$ segundos, $2{,}1$ segundos, $2{,}15$ segundos, entre outros valores.
	- Aqui consideramos o tempo idealizado, sem a limitação de precisão do instrumento de medida.

- **Equiprobabilidade:**
	- É uma característica das **probabilidades atribuídas aos resultados**, e não apenas do conjunto $\Omega$.
	- **Equiprovável:** todos os resultados possíveis têm a mesma probabilidade de ocorrer.
		- Exemplo: em um dado honesto, cada face tem probabilidade $\frac{1}{6}$.
	- **Não equiprovável:** os resultados possíveis não têm todos a mesma probabilidade de ocorrer.
		- Exemplo: em um dado viciado, algumas faces podem ter maior chance de ocorrer que outras.
	- **Importante:** ser finito não garante ser equiprovável. Um dado honesto e um dado viciado têm o mesmo espaço amostral $\Omega = \{1,2,3,4,5,6\}$, mas podem ter probabilidades diferentes.

- **Espaço Amostral Finito e Equiprovável:**
	- Combina duas características: uma **quantidade finita de resultados** e a **mesma probabilidade para cada resultado**.
	- Se $\Omega$ possui $n$ resultados, cada resultado tem probabilidade $\frac{1}{n}$.
	- Para um evento $A$, usamos:
		- $P(A) = \frac{|A|}{|\Omega|} = \frac{\text{número de resultados favoráveis}}{\text{número total de resultados possíveis}}$.
		- $|A|$ representa a quantidade de resultados do evento $A$, e $|\Omega|$ representa a quantidade de resultados do espaço amostral.
	- **Exemplo:** obter um número par ao lançar um dado honesto.
		- $\Omega = \{1,2,3,4,5,6\}$ e $A = \{2,4,6\}$.
		- $P(A) = \frac{3}{6} = \frac{1}{2}$.
	- Essa fórmula de contagem exige que os resultados sejam **equiprováveis**.

- **Resumo dos Critérios:**
	- **Quanto à quantidade de resultados:** o espaço pode ser finito ou infinito; no caso infinito, pode ser enumerável ou não enumerável.
	- **Quanto às probabilidades atribuídas:** em um espaço finito, o modelo pode ser equiprovável ou não equiprovável.
	- Esses critérios são diferentes: dizer quantos resultados existem não informa, por si só, a chance de cada um.

- **Relação com o Modelo Probabilístico:**
	- Estabelecer o espaço amostral é uma das etapas da construção de um modelo probabilístico.
	- Além dos resultados possíveis, é necessário definir os eventos e as probabilidades atribuídas a eles.
	- **Observação:** essa classificação descreve os resultados possíveis; não determina, sozinha, como as probabilidades são distribuídas.
