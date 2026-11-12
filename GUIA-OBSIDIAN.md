# Primeiros passos com o CC.md no Obsidian

O Obsidian abre uma pasta de arquivos Markdown como um **cofre** (*vault*). Aqui, o cofre é a pasta `CC.md` inteira: os períodos, as disciplinas e as notas continuam sendo arquivos comuns, que você também pode ler fora do aplicativo.

## Abrir o acervo como cofre

1. [Instale o Obsidian e baixe ou clone o CC.md](INSTALACAO-OBSIDIAN.md). Se quiser contribuir com Git, siga nesse guia as instruções para clonar o seu *fork*.
2. Abra o Obsidian. Na tela inicial, escolha **Abrir pasta como cofre** (*Open folder as vault*). Se já estiver em outro cofre, abra o seletor de cofres e escolha essa opção.
3. Selecione a pasta **`CC.md`** que você baixou ou clonou, e confirme. Não selecione `P1/`, `.git/` ou uma pasta vazia criada pelo Obsidian: a raiz `CC.md` é o cofre que reúne todo o acervo.
4. Na barra lateral de arquivos, abra um período (`P1/` a `P9/`) ou `Optativas/`, entre na disciplina e abra o sumário com o nome da matéria. Se a pasta ainda estiver vazia, tudo bem: o acervo está em construção.

Baixou um ZIP? Extraia-o antes e selecione a pasta extraída que contém `README.md`, `P1/` e as demais pastas. O ZIP serve para ler, mas não inclui o histórico do Git; para receber mudanças com `git pull` e contribuir, faça o clone conforme o [guia de instalação e Git](INSTALACAO-OBSIDIAN.md).

## Encontrar assuntos e entender as conexões

- Use a busca do Obsidian para encontrar um conceito pelo nome ou pelo texto da nota. As propriedades `periodo`, `disciplina` e `trilhas` ajudam a filtrar as anotações; por exemplo, pesquise `[disciplina: IA]`.
- Clique nos links `[[...]]` das notas para seguir de um conceito a outro. A pasta mostra onde a nota está guardada; os links mostram como os assuntos se relacionam.
- Abra a **Visualização de grafo** (*Graph view*) para ver essas conexões. Uma nota aparece ligada a outra quando há um link interno entre elas. Pastas e propriedades, sozinhas, não criam linhas no grafo; não é preciso instalar plugins adicionais para usar essa visualização.

## Escrever sem deixar notas soltas

Para contribuir, copie o [modelo de nota](templates/Nota.md) para a pasta da disciplina, dê ao arquivo o nome do conceito e preencha as propriedades no começo. No texto, use `[[Nome da nota]]` para apontar para conceitos relacionados. Inclua sua nota no sumário da disciplina; se ainda não houver um, crie-o com o [modelo de sumário](templates/Sumario%20da%20disciplina.md). Confira os nomes dos links antes de enviar: um link para uma nota que não existe não conecta o conteúdo. O [guia de contribuição](CONTRIBUTING.md) explica o padrão das notas e como compartilhar seu trabalho.

## Quer ver mais?

- [Ajuda oficial do Obsidian](https://help.obsidian.md/) — documentação para aprender a usar cofres, notas, links e a visualização de grafo.
- [Tutorial em vídeo sobre o Obsidian](https://youtu.be/64qkBzaGnIw?si=It14TuE97oT8q0Ab) — para acompanhar os primeiros passos em vídeo; use as orientações acima para abrir especificamente o acervo `CC.md`.
