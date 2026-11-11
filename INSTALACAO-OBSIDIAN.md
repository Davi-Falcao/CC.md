# Usando o CC.md no Obsidian

O Obsidian abre pastas de arquivos Markdown como **cofres** (*vaults*). Para usar este projeto, instale o aplicativo e abra a pasta clonada do repositório. O Obsidian é opcional: os arquivos também podem ser lidos em qualquer editor ou no GitHub.

## Instalar o Obsidian

Baixe sempre de fontes confiáveis. A [página oficial de downloads](https://obsidian.md/download) tem versões para Linux, Windows, macOS, Android e iOS e mostra os formatos disponíveis para cada sistema.

No Linux, escolha **uma** das opções compatíveis com sua distribuição:

| Sistema | Opção | Como instalar |
| --- | --- | --- |
| Ubuntu / Linux Mint e derivados | [Pacote `.deb` oficial](https://obsidian.md/download) | Baixe o arquivo `.deb` para sua arquitetura e, na pasta em que o salvou, execute `sudo apt install ./obsidian_*.deb`. O `./` é importante: instala o arquivo baixado, não um pacote chamado `obsidian` dos repositórios. |
| Ubuntu / Linux Mint e outras distros com Snap | [Snap](https://snapcraft.io/obsidian) | Se o Snap estiver disponível, execute `sudo snap install obsidian --classic`. No Mint, o Snap pode estar desativado por padrão; prefira o `.deb` ou o Flatpak se não quiser habilitá-lo. |
| Arch Linux / Manjaro e derivados com repositórios Arch | [Pacote `extra` do Arch](https://archlinux.org/packages/extra/x86_64/obsidian/) | Execute `sudo pacman -Syu obsidian` se sua distribuição disponibilizar o pacote nos repositórios configurados. |
| Distros com Flatpak e Flathub configurados | [Flatpak (mantido pela comunidade)](https://flathub.org/apps/md.obsidian.Obsidian) | Execute `flatpak install flathub md.obsidian.Obsidian`. |
| Outras distribuições Linux | [AppImage oficial](https://obsidian.md/download) | Baixe o AppImage para sua arquitetura, permita sua execução (`chmod +x ./Obsidian-*.AppImage`) e abra o arquivo. |

Se um gerenciador de pacotes não estiver instalado ou configurado no seu sistema, use a opção oferecida pela sua distribuição ou baixe pela página oficial. Os nomes e versões dos arquivos mudam com as atualizações; confira o nome do `.deb`/AppImage que você baixou antes de executar os comandos.

## Colocar o repositório no cofre

Você **não precisa adicionar `.git` manualmente ao Obsidian**: a pasta `.git` é criada pelo `git clone` dentro de `CC.md/`. Ela é oculta no gerenciador de arquivos e contém o histórico e as configurações locais do Git. Não a apague nem a copie sozinha para outro cofre.

1. Instale o Git, caso ainda não tenha: no Ubuntu/Mint, `sudo apt install git`; no Arch, `sudo pacman -S git`.
2. No terminal, vá até a pasta onde deseja guardar o acervo e clone o projeto:

   ```bash
   git clone https://github.com/UFCG-CC-md/CC.md.git
   ```

3. Abra o Obsidian, escolha **Abrir pasta como cofre** (*Open folder as vault*) e selecione a pasta `CC.md` criada pelo clone. **Não** selecione a pasta `.git`.
4. Para receber atualizações, abra o terminal dentro de `CC.md/` e execute `git pull` quando não houver alterações locais pendentes. Se houver, salve-as em um commit antes; se o Git indicar conflitos, resolva-os antes de continuar.

Baixar o ZIP do GitHub permite ler as notas, mas **não inclui `.git`**: para usar `git pull`, faça o clone. Se você já tem um cofre pessoal, mantenha-o separado; não mova apenas `.git` para dentro dele, pois isso não transforma seus arquivos pessoais neste repositório.

## Salvar e enviar uma anotação com Git

Você pode editar a nota no Obsidian e usar o Git pelo terminal. Para contribuir com o projeto, faça primeiro um **fork** no GitHub (botão **Fork** na página do repositório) e clone o **seu fork** em vez da URL acima: `git clone https://github.com/SEU_USUARIO/CC.md.git`. Assim, `git push` enviará a mudança para o seu repositório, e você poderá abrir um *pull request* para o CC.md.

No terminal, entre na pasta clonada e crie uma branch antes de editar:

```bash
cd CC.md
git switch -c nota-busca-em-largura
```

Crie ou edite a nota em `P5/IA/Busca em largura.md` pelo Obsidian. Depois, no terminal:

```bash
git status
git add "P5/IA/Busca em largura.md"
git diff --cached
git commit -m "docs: adiciona anotação sobre busca em largura"
git push -u origin nota-busca-em-largura
```

`git status` mostra o que mudou; `git add` seleciona **somente a nota indicada** para o commit; `git diff --cached` permite conferir exatamente o que será enviado; `git commit` registra a mudança localmente; e `git push` publica a branch no seu fork. Se o Git pedir seu nome e e-mail no primeiro commit, configure-os com `git config --global user.name "Seu Nome"` e `git config --global user.email "seu-email@example.com"` (use um e-mail privado do GitHub se não quiser expor o pessoal). Para enviar via HTTPS, talvez seja necessário autenticar com o GitHub CLI ou um token: a senha da conta não funciona no `git push`.

Por fim, abra seu fork no GitHub e clique em **Compare & pull request** para propor a mudança ao repositório principal. Não use `git add .` sem conferir os arquivos: configurações pessoais do Obsidian (como `.obsidian/`) ou outros arquivos locais podem entrar no commit. Veja também o [guia de contribuição](CONTRIBUTING.md) para o padrão das notas e as regras de publicação.
