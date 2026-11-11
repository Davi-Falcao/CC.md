# Acervo da universidade

Este espaço reúne **links e materiais úteis para estudantes em geral**: páginas oficiais, serviços, guias e recursos que não pertencem a uma disciplina específica. Para começar, adicione aqui um arquivo Markdown por recurso ou tema, com nome descritivo (por exemplo, `Biblioteca.md`). Não é necessário criar categorias ou pastas extras.

## Como contribuir aqui

1. Confira se o recurso já não está listado e se o link funciona.
2. Crie um `.md` em `Acervo/` com o nome do recurso, um resumo de sua utilidade, a fonte e o link. Indique se o conteúdo é oficial ou produzido por estudantes e mantenha informações sujeitas a mudanças (como horários) apontadas para a página de origem.
3. Se o material não puder ser colocado diretamente em Markdown (por exemplo, um PDF ou vídeo **que você tem permissão para divulgar**), hospede-o no Google Drive e inclua seu link no `.md`. No Drive, configure **Acesso geral → Qualquer pessoa com o link → Leitor**; teste em janela anônima para confirmar que não exige solicitação de acesso ou login institucional. Não inclua dados pessoais nem arquivos sem autorização de publicação. Para materiais de terceiros que não podem ser redistribuídos, use somente o link oficial/autorizado.

Exemplo de entrada em `Acervo/Biblioteca.md`:

```md
# Biblioteca

Fonte: site oficial da universidade.

Guia para encontrar livros, serviços e informações atualizadas da biblioteca.

[Acessar a biblioteca](https://exemplo.org/biblioteca)
```

## E se o material for de uma matéria?

Não coloque em `Acervo/`: use a pasta da disciplina, por exemplo `P5/IA/` (ou `Optativas/Nome_da_Disciplina/`). Crie ali um arquivo como `Materiais de busca.md` com as propriedades `tipo`, `periodo`, `disciplina` e `trilhas`, conforme o [guia de contribuição](../CONTRIBUTING.md). Liste cada recurso com título, fonte, link e uma frase dizendo o que ajuda a estudar. Se for um arquivo seu ou autorizado no Drive, aplique as mesmas regras de acesso público por link e teste; não crie um link para material protegido sem permissão.

Exemplo em `P5/IA/Materiais de busca.md`:

```md
---
tipo: material
periodo: 5
disciplina: IA
trilhas:
  - IA
---

# Materiais de busca

- [Exercícios comentados](https://drive.google.com/file/d/EXEMPLO/view) — exercícios autorizados para divulgação, com resolução. Fonte: material próprio.
- [Referência sobre algoritmos de busca](https://exemplo.org/busca) — leitura complementar na fonte original.

Veja também [[Busca em largura]].
```

Para anotações de conceitos, use o [modelo de nota](../templates/Nota.md). Para enviar a contribuição, siga o [guia geral](../CONTRIBUTING.md).
