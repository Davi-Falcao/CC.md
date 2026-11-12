# Como contribuir

Não precisa escrever um capítulo inteiro: uma explicação clara, um exemplo resolvido ou uma correção já ajudam muito.

## Onde colocar os arquivos

Use a pasta da disciplina em `P1/` a `P9/` (por exemplo, `P5/IA/`). Para optativas, crie `Optativas/Nome_da_Disciplina/` se ainda não existir. Uma nota por conceito, com nome descritivo (por exemplo, `Busca em largura.md`), facilita a busca e os links. Se o conteúdo relaciona duas matérias, escolha a pasta mais relevante e faça links para as notas da outra; não duplique o arquivo.

Recursos gerais da universidade, sem vínculo com uma disciplina, vão em [`Acervo/`](Acervo/Acervo%20da%20universidade.md). Para materiais de uma matéria específica, crie um `.md` na pasta da disciplina, mesmo quando o arquivo estiver hospedado fora do repositório; veja o exemplo nas [orientações do Acervo](Acervo/Acervo%20da%20universidade.md).

Para começar uma anotação, copie [`templates/Nota.md`](templates/Nota.md) para a pasta escolhida, renomeie e substitua os valores de exemplo. O modelo é opcional para materiais que não sejam notas, mas as propriedades ajudam a localizar qualquer arquivo Markdown.

Guarde imagens e outros arquivos não Markdown autorizados em `midia/` dentro da pasta da disciplina (por exemplo, `P4/BD1/midia/`). Nos `.md`, referencie-os pelo caminho relativo, como `![[midia/imagem.png]]` no Obsidian ou `![Descrição](midia/imagem.png)` em Markdown. Ao mover um arquivo, atualize todas as referências a ele. Para PDFs, vídeos e outros materiais de estudo, prefira o link público conforme as regras abaixo.

## Propriedades e conexões

No início da nota, mantenha as propriedades YAML:

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

Use `[[Nome da nota]]` para ligar conceitos. Prefira títulos únicos no acervo; se houver nomes repetidos, especifique o caminho, como `[[P5/IA/Busca em largura]]`. Links para notas ainda inexistentes podem indicar temas a escrever, mas confira se a nota já não existe com outro nome. Para recursos externos, use links Markdown como `[Descrição](https://exemplo.org)` e diga por que o recurso é útil.

## O que vale compartilhar

- **Anotações:** explique com suas palavras, inclua um exemplo e, quando possível, diga como o conceito se relaciona com outros. Evite notas que sejam apenas uma lista de termos.
- **Materiais e links:** indique a fonte e um resumo do que a pessoa encontrará. Prefira links para a fonte original a cópias de arquivos.
- **Questões e provas:** inclua enunciados ou arquivos somente se tiver autorização para redistribuí-los; identifique a origem e, quando possível, acrescente uma resolução comentada. Nunca publique dados pessoais, gabaritos restritos ou material de avaliação ainda em uso.

Se um material permitido não couber em `.md` (como um PDF ou vídeo), hospede-o no Google Drive e coloque o link em um `.md` com título, fonte e breve descrição. Configure **Acesso geral → Qualquer pessoa com o link → Leitor**, sem exigir login institucional, e teste o link em uma janela anônima antes do *pull request*. Não publique dados pessoais. Um link público não substitui autorização: não envie slides, livros, PDFs, provas ou imagens de terceiros sem permissão ou licença compatível, nem para o repositório nem para o Drive. Para conteúdo de terceiros sem autorização de redistribuição, aponte apenas para a fonte oficial ou autorizada e atribua autoria.

## Enviando sua contribuição

1. Faça um *fork* e crie uma branch para sua mudança.
2. Adicione ou edite os arquivos Markdown na pasta correspondente. Confira se o título, as propriedades, os links e as fontes estão corretos; no Obsidian, veja se a nota aparece na busca por período, disciplina e trilha.
3. Abra um *pull request* explicando o que você adicionou ou corrigiu. Se preferir começar com uma ideia, dúvida ou erro encontrado, abra uma *issue*.

Não precisa usar Obsidian para contribuir: qualquer editor de texto funciona. (mas o Obsidian ajuda bastante!)
