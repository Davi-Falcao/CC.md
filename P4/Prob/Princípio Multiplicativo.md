---
tipo: anotacao
periodo: 4
disciplina: Prob
trilhas: []
---

# Princípio Multiplicativo

## Em poucas palavras

O **Princípio Multiplicativo**, também chamado de **Princípio Fundamental da Contagem**, permite contar resultados de uma tarefa dividida em etapas.

Se a primeira etapa pode ser realizada de $n_1$ maneiras e, para **cada escolha anterior**, a segunda pode ser realizada de $n_2$ maneiras, então o total de maneiras de realizar as duas etapas é:

$$N = n_1 \cdot n_2.$$

Para $k$ etapas, seguimos a mesma ideia:

$$N = n_1 \cdot n_2 \cdot \ldots \cdot n_k.$$

**Importante:** a quantidade de opções em cada etapa deve ser a mesma para todas as escolhas feitas nas etapas anteriores. Isso não exige independência probabilística: estamos contando possibilidades, não multiplicando probabilidades. Além disso, cada resultado deve ser contado uma única vez.

## Entendendo na prática

### Exemplo 1: escolha de roupas

Uma pessoa tem $3$ camisetas e $2$ calças. Para montar um conjunto, ela deve:

- Escolher uma camiseta: $3$ possibilidades.
- Escolher uma calça: $2$ possibilidades para cada camiseta escolhida.

Assim, o número de conjuntos possíveis é:

$$N = 3 \cdot 2 = 6.$$

### Exemplo 2: formação de uma diretoria

Uma empresa tem $10$ sócios brasileiros e $5$ japoneses. Queremos formar uma diretoria com $4$ brasileiros e $2$ japoneses.

- Escolher os $4$ brasileiros dentre os $10$ disponíveis:
	$$\binom{10}{4} = \frac{10!}{4!6!} = 210.$$
- Para cada grupo de brasileiros escolhido, escolher os $2$ japoneses dentre os $5$ disponíveis:
	$$\binom{5}{2} = \frac{5!}{2!3!} = 10.$$

Como cada escolha do grupo de brasileiros pode ser combinada com qualquer escolha do grupo de japoneses, aplicamos o Princípio Multiplicativo:

$$\#A = \binom{10}{4}\binom{5}{2} = 210 \cdot 10 = 2100.$$

Cada diretoria corresponde a um único par de grupos: o dos brasileiros e o dos japoneses. Por isso, não há contagem repetida.

**Por que usamos combinações?** A ordem de escolha dos sócios não importa: escolher as mesmas pessoas em outra ordem não forma uma nova diretoria.

## Conexões

- [[Teoria das Probabilidades - Abordagem Clássica]] — apresenta as combinações simples e usa o Princípio Multiplicativo para contar os casos favoráveis no Exemplo 2.
- [[Classificação dos Espaços Amostrais]] — em um espaço finito e equiprovável, as contagens dos casos favoráveis e possíveis permitem calcular $P(A) = \frac{\#A}{\#\Omega}$.

## Para saber mais/Referências

- [[Teoria das Probabilidades - Abordagem Clássica#Combinação Simples:|Combinação simples e exemplo da diretoria]] — enunciado e solução completa do exemplo utilizado nesta nota.
