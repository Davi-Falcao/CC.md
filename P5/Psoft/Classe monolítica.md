---

tipo: anotacao

periodo: 5

disciplina: Psoft

trilhas:

- Engenharia de Software

---
## O que é:

Uma **classe monolítica** concentra responsabilidades ou variantes de comportamento demais em um só lugar. Não é apenas uma classe longa: o sinal mais importante é precisar alterá-la por motivos diferentes, muitas vezes em trechos que não deveriam depender uns dos outros.

## Exemplo:

Pense em uma classe `Relatorio` que escolhe o formato (PDF ou HTML), consulta diferentes bancos de dados e envia o resultado por e-mail. Adicionar um formato ou trocar o banco exige mexer na mesma classe, aumentando o risco de afetar outras funções.

## Como evitar:

Separe o que varia de forma independente. O [[Bridge]] ajuda quando há duas dimensões, como tipo de relatório e banco de dados: a abstração delega o acesso ao banco a uma implementação. O [[Strategy]] é útil quando o que muda é o algoritmo usado em uma tarefa. Nem toda classe com mais de uma responsabilidade precisa de um padrão; extraia apenas o que traz clareza.

Veja também: [[Código monolítico|código monolítico]], que descreve o problema em uma escala maior.
