---
tipo: anotacao
periodo: 4
disciplina: BD1
trilhas: []
---

# Banco de Dados 1

> [!abstract] Sobre esta pasta
> Mapa das notas e atividades de Banco de Dados 1 (UFCG). Comece pelos comandos SQL; depois explore consultas, visões e programação no banco.

## Estrutura e integridade

| Nota | Para estudar |
| --- | --- |
| [[DDL SQL Commands]] | Criação de tabelas e restrições de integridade. |
| [[Foreign Key]] | Chaves estrangeiras, `ALTER TABLE`, índices e sequências. |
| [[DUMMY TABLE]] | Tabela auxiliar usada em consultas, como a `DUAL` do Oracle. |

## Consultas e alterações

| Nota | Para estudar |
| --- | --- |
| [[DML SQL Commands]] | `SELECT`, junções, agrupamentos, subconsultas, `INSERT`, `UPDATE` e `DELETE`. |
| [[Visões]] | `CREATE VIEW` e valores nulos em consultas. |
| [[STORED PROCEDURES]] | PL/SQL: blocos, cursores, funções e procedimentos. |

## Atividades e exemplos

| Nota | Para praticar |
| --- | --- |
| [[Questoes]] | Exercícios de consultas, alterações, visões e gatilhos (*triggers*). |
| [[PROJETO GRUPO 9 CONSULTAS P1]] | Consultas SQL do projeto, parte 1. |
| [[PROJETO GRUPO 9 CONSULTAS P2]] | Funções, procedimentos, visões e gatilhos do projeto, parte 2. |
| [[PROJETO GRUPO 9 CONSULTAS]] | Cópia das consultas da parte 1, mantida como arquivo original. |

## Scripts do esquema de exemplo

- [Criar e povoar o banco de dados Empresa](https://github.com/lucasemmanuelsa/Sql/blob/main/Scripts/BD%20Empresa/create_schema%281%29.sql) — cria as tabelas e insere dados de exemplo para praticar os comandos SQL. Fonte: repositório original de Lucas Emmanuel.
- [Remover as tabelas do esquema Empresa](https://github.com/lucasemmanuelsa/Sql/blob/main/Scripts/BD%20Empresa/dropSchemaSlide.sql) — comandos `DROP TABLE` para desfazer o esquema de exemplo. Fonte: repositório original de Lucas Emmanuel.

As imagens utilizadas nas notas ficam em `midia/`.

> [!cite] Fonte:
> https://github.com/lucasemmanuelsa/Sql/
