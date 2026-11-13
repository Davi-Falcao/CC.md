# Como contribuir

Não precisa escrever um capítulo inteiro: uma explicação clara, um exemplo resolvido ou uma correção já ajudam muito.

## Primeira contribuição? Comece por aqui

Se ainda não conhece as ferramentas, os tutoriais mostram o caminho com imagens e exemplos:

- [Guia do Obsidian](GUIA-OBSIDIAN.md): como instalar o aplicativo, abrir o acervo, configurar o menu lateral, visualizar o grafo e criar links entre notas.
- [Guia de Git](GUIA-GIT.md): como criar e acessar seu fork, cloná-lo, salvar suas mudanças e abrir uma *pull request* (PR) para o repositório principal.

O Obsidian é opcional: qualquer editor de texto funciona. Para enviar uma contribuição, trabalhe na cópia do seu fork e depois proponha as mudanças ao CC.md pela PR. Os tutoriais explicam as ferramentas; as orientações abaixo ajudam a organizar o conteúdo.

## Onde colocar os arquivos

Use a pasta da disciplina em `P1/` a `P9/` (por exemplo, `P5/IA/`). Para optativas, crie `Optativas/Nome_da_Disciplina/` se ainda não existir. Uma nota por conceito, com nome descritivo (por exemplo, `Busca em largura.md`), facilita a busca e os links. Se o conteúdo relaciona duas matérias, escolha a pasta mais relevante e faça links para as notas da outra; não duplique o arquivo.

Recursos gerais da universidade, sem vínculo com uma disciplina, vão em [`Acervo/`](Acervo/Acervo%20da%20universidade.md). Para materiais de uma matéria específica, crie um `.md` na pasta da disciplina, mesmo quando o arquivo estiver hospedado fora do repositório; veja o exemplo nas [orientações do Acervo](Acervo/Acervo%20da%20universidade.md).

Para começar uma anotação, copie [`templates/Nota.md`](templates/Nota.md) para a pasta escolhida, renomeie e substitua os valores de exemplo. Para outros materiais em Markdown, inclua também as propriedades descritas na próxima seção: elas ajudam a localizar o conteúdo no acervo.

Toda disciplina com conteúdo no acervo deve ter um sumário na própria pasta. Ao adicionar o primeiro conteúdo de uma matéria, copie o [modelo de sumário](templates/Sumario%20da%20disciplina.md) e salve-o com o nome da disciplina, como [`P4/Grafos/Grafos.md`](P4/Grafos/Grafos.md). Preencha as propriedades, apresente a matéria em poucas palavras e inclua links `[[...]]` para as notas que já existem, com uma frase sobre cada uma.

Conforme surgirem novos assuntos, agrupe-os no sumário do jeito que fizer sentido para a disciplina; veja também [`P5/Psoft/Projeto de Software.md`](P5/Psoft/Projeto%20de%20Software.md). Ao criar uma nota, inclua-a no sumário da matéria e, quando houver relação, ligue-a a outros conceitos: assim o grafo não fica com notas soltas. Mantenha o sumário atualizado, sem preencher a lista com links para notas que ainda não foram escritas.

Guarde imagens e outros anexos autorizados que acompanham as notas em `midia/` dentro da pasta da disciplina (por exemplo, `P4/BD1/midia/`). Nos `.md`, referencie-os pelo caminho relativo, como `![[midia/imagem.png]]` no Obsidian ou `![Descrição](midia/imagem.png)` em Markdown. Ao mover um arquivo, atualize todas as referências a ele. Para materiais de estudo distribuídos como PDFs ou vídeos, siga as orientações de hospedagem e links na seção **O que vale compartilhar**.

## Propriedades e conexões

No início da nota, preencha as propriedades YAML conforme o conteúdo. Este é um exemplo de anotação de IA do quinto período:

```yaml
---
tipo: anotacao
periodo: 5
disciplina: IA
trilhas:
  - IA
---
```

- `tipo`: `anotacao`, `material`, `link`, `questao` ou `prova`.
- `periodo`: número de 1 a 9, conforme a pasta; em optativas, use `optativa`.
- `disciplina`: sigla da pasta (por exemplo, `IA`); em optativas, use o nome da pasta.
- `trilhas`: lista de áreas relacionadas. Comece por `IA`, `Engenharia de Software` ou `Infra` quando fizer sentido; outras trilhas podem surgir conforme o acervo crescer. Não é preciso forçar uma trilha em toda nota: use `trilhas: []` quando nenhuma se aplicar.

Use `[[Nome da nota]]` para ligar conceitos. Prefira títulos únicos no acervo; se houver nomes repetidos, especifique o caminho, como `[[P5/IA/Busca em largura]]`. Antes de criar um link, confira se a nota já existe com outro nome; no sumário da disciplina, inclua apenas notas existentes. Para recursos externos, use links Markdown como `[Descrição](https://exemplo.org)` e diga por que o recurso é útil.

## O que vale compartilhar

- **Anotações:** explique com suas palavras, inclua um exemplo e, quando possível, diga como o conceito se relaciona com outros. Evite notas que sejam apenas uma lista de termos.
- **Materiais e links:** indique a fonte e um resumo do que a pessoa encontrará. Prefira links para a fonte original a cópias de arquivos.
- **Questões e provas:** inclua enunciados ou arquivos somente se tiver autorização para redistribuí-los; identifique a origem e, quando possível, acrescente uma resolução comentada. Nunca publique dados pessoais, gabaritos restritos ou material de avaliação ainda em uso.

Se um material permitido não couber em `.md` (como um PDF ou vídeo), hospede-o no Google Drive e coloque o link em um `.md` com título, fonte e breve descrição. Configure **Acesso geral → Qualquer pessoa com o link → Leitor**, sem exigir login institucional, e teste o link em uma janela anônima antes do *pull request*. Não publique dados pessoais. Um link público não substitui autorização: não envie slides, livros, PDFs, provas ou imagens de terceiros sem permissão ou licença compatível, nem para o repositório nem para o Drive. Para conteúdo de terceiros sem autorização de redistribuição, aponte apenas para a fonte oficial ou autorizada e atribua autoria.

## Enviando sua contribuição

Se precisar dos comandos para clonar o projeto, salvar alterações e enviá-las ao GitHub, siga o [guia de Git](GUIA-GIT.md).

1. Faça um *fork*, clone sua cópia e crie uma branch para sua mudança.
2. Adicione ou edite os arquivos Markdown na pasta correspondente. Confira se o título, as propriedades, os links e as fontes estão corretos; confira também se a nota consta no sumário da disciplina. Se estiver usando o Obsidian, veja se a nota aparece na busca pelas propriedades que você preencheu.
3. Confira os arquivos selecionados, registre as mudanças em um commit e envie a branch para seu fork com `git push`. Inclua o sumário e as imagens necessários, sem enviar configurações pessoais.
4. Abra um *pull request* da sua branch no fork para a branch `main` de `UFCG-CC-md/CC.md`, explicando o que você adicionou ou corrigiu. Acompanhe a revisão e, se houver pedidos de ajuste, envie novos commits na mesma branch.

Se preferir começar com uma ideia, dúvida ou erro encontrado, abra uma *issue* no repositório principal. Você não precisa ter uma nota pronta para participar.
