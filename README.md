# The World Ends with You em português brasileiro

Tradução de fãs para a versão **USA (AWLE)** de *The World Ends with You* para Nintendo DS. A versão 1.0 inclui diálogos da campanha, capítulos extras, menus, tutoriais, descrições de itens e créditos.

## Instalação

1. Abra a página de [Releases do repositório](https://github.com/ggdrn/twewy-pt-br/releases), selecione a versão **1.0** e baixe `twewy-pt-br-1.0-usa.xdelta` em **Assets**.
2. Use uma cópia limpa, descompactada e sem cortes da ROM USA, em formato `.nds`. A base usada tem **128 MiB**, código **AWLE** e o SHA-256 abaixo.
3. No [Rom Patcher JS](https://www.marcrobledo.com/RomPatcher.js/), selecione a ROM original em **ROM file** e o arquivo `.xdelta` em **Patch file**. Clique em **Apply patch** e salve o novo `.nds`.
4. Abra o `.nds` gerado no seu emulador de Nintendo DS.

A release distribui o patch. Use sua própria cópia do jogo como base.

### Aplicação pelo terminal

Com o [xdelta3](https://jmacd.github.io/xdelta/) instalado, abra o terminal na pasta onde estão os arquivos e rode o comando abaixo. Ajuste os nomes se tiver renomeado os arquivos.

```sh
xdelta3 -d -s "World Ends with You, The (USA).nds" "twewy-pt-br-1.0-usa.xdelta" "TWEWY-PT-BR.nds"
```

Se o programa indicar erro de checksum, confira se a ROM é a versão USA, está descompactada e tem o SHA-256 da base abaixo. Use `shasum -a 256 "arquivo.nds"` no macOS, `sha256sum "arquivo.nds"` no Linux ou `Get-FileHash "arquivo.nds" -Algorithm SHA256` no PowerShell.

| Arquivo | SHA-256 |
| --- | --- |
| ROM USA original | `3129ce0d35f082eb37e53de1e454a1ff12c98787a93037f2351084e377e1d74d` |
| Patch 1.0 | `37c156398ca97a83ae51003280ba73cbedba4d0fe0fdb1c795c7acf61b4103b5` |
| ROM com o patch aplicado | `f1195dc06563623729f9bb172c09f8f2a7b23c3ee53781280537c2be5b3de55b` |

## Sobre a versão 1.0

O patch foi aplicado à ROM USA de referência. A reextração dos textos da ROM traduzida conferiu com os 45 arquivos da pasta `br/`, num total de 25.233 entradas. Parte da tradução foi feita com auxílio de um modelo local e revisada por amostragem. A revisão de falas, termos e encaixe de texto em jogo segue aberta.

Para relatar um problema, abra uma [issue](https://github.com/ggdrn/twewy-pt-br/issues) com o dia, o local da cena ou o nome do menu e, se possível, uma captura de tela.

## Arquivos do projeto

- `en/` contém os textos originais.
- `br/` contém os textos em português brasileiro.
- `twewy.py` é a ferramenta de extração e inserção de textos. A instalação pelo patch dispensa o Python.

## Créditos

- **alizor** pela ferramenta e pela tradução inicial.
- **ggdrn** pela continuação da tradução e organização deste projeto.

## Licença

Livre, mantenha os créditos.
