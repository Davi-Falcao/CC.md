# CC.md

Já aconteceu de você entender um assunto só depois que alguém da turma explicou de outro jeito? O **CC.md** é um lugar para guardar essas explicações e compartilhá-las com quem vier depois.

Este repositório é um acervo aberto de Ciência da Computação: anotações que **explicam conceitos**, materiais de estudo, links, questões e provas que podem ser compartilhadas. A ideia é conectar os assuntos como na Wikipédia: uma nota sobre um conceito pode apontar para outra por meio de `[[links internos]]`. Assim, cada contribuição ajuda a construir um grafo de conhecimento do curso.

## Como encontrar conteúdo

- **Por período:** abra `P1/` até `P9/`. Cada pasta contém as disciplinas daquele período; as optativas ficam em `Optativas/`.
- **Por disciplina:** entre na pasta da matéria, como `P5/IA/`, e abra o sumário com o nome da disciplina para encontrar as notas. As siglas seguem os nomes das pastas já existentes; o acervo ainda está em construção, então nem toda pasta tem um sumário.
- **Recursos gerais da universidade:** consulte o [Acervo](Acervo/Acervo%20da%20universidade.md) para links e materiais úteis que não pertencem a uma disciplina específica.
- **Por trilha:** no Obsidian, use a busca pelas propriedades, por exemplo `[trilhas: IA]`, `[trilhas: Engenharia de Software]` ou `[trilhas: Infra]`. Uma nota pode pertencer a mais de uma trilha.
- **Por conceito:** use a busca do Obsidian ou siga os links `[[...]]` entre as notas. A visualização de grafo mostra essas conexões; não é necessário instalar plugins.

> O acervo está no início: algumas pastas ainda estão vazias. Os períodos e as trilhas ajudam a navegar, mas não substituem a explicação do conteúdo.

## Como usar no Obsidian

Para usar o acervo no Obsidian, instale o aplicativo e abra a pasta `CC.md` como um *cofre* (*vault*). Se você clonar o projeto com Git, a pasta oculta `.git` já estará dentro dele — não é preciso adicioná-la ao Obsidian.

1. Siga o [guia do Obsidian](GUIA-OBSIDIAN.md) para instalar o aplicativo, baixar o acervo, abrir a pasta como cofre e configurar o menu lateral para visualizar o grafo. Se preferir clonar o repositório em vez de baixar o ZIP, consulte o [guia de Git](GUIA-GIT.md).
2. Navegue pelas pastas ou pesquise pelas propriedades `periodo`, `disciplina` e `trilhas` (por exemplo, `[periodo: 5]` e `[disciplina: IA]`).
3. Ao escrever, copie o [modelo de nota](templates/Nota.md) para a pasta da disciplina. Preencha as propriedades no início do arquivo e conecte conceitos com links internos. Inclua a nota no sumário da disciplina; se ele ainda não existir, crie-o a partir do [modelo de sumário](templates/Sumario%20da%20disciplina.md).

Quer compartilhar uma nota? O [guia de Git](GUIA-GIT.md) explica como instalar o Git, clonar seu *fork*, criar uma branch e enviar a contribuição por um *pull request*.

Os arquivos são Markdown comum: você pode lê-los e contribuir também pelo GitHub, sem usar Obsidian. Para contribuir, use as propriedades e os links `[[...]]` conforme o [guia de contribuição](CONTRIBUTING.md); eles ajudam a encontrar as notas e a manter o grafo conectado.

## Vamos construir juntos?

Você pode começar por uma explicação curta de algo que aprendeu, corrigir uma nota existente ou indicar um material útil. Antes de enviar conteúdo, leia o [guia de contribuição](CONTRIBUTING.md) e, para recursos gerais, as [orientações do Acervo](Acervo/Acervo%20da%20universidade.md). Eles explicam onde colocar cada arquivo, como preencher as propriedades e os cuidados com provas e direitos autorais.

Este é um projeto da comunidade, não um material oficial da universidade. Encontrou um erro? Abra uma *issue* ou envie uma correção.
