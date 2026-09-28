# FVM — Webpixum / XISDE Gamepad Skin

Skin Webpixum / XISDE para o Gamepad Viewer, gerada das camadas do arquivo `Webpixum_X-Box_Controller-Recuperado2.psd`.
Base, gatilhos LT/RT, ombros LB/RB, analógicos, direcional e botões ABXY são PNGs transparentes exportados do PSD e posicionados sobre o canvas do viewer.

## URLs públicas

Após a publicação do GitHub Pages:

- CSS recomendado por URL: `https://aledsst-ai.github.io/fvm/gamepadviewer.css?v=trigger-mask-stick-sockets-20260927a`
- CSS com imagens absolutas, indicado para copiar e colar: `https://aledsst-ai.github.io/fvm/gamepadviewer-absolute.css`
- Prévia: `https://aledsst-ai.github.io/fvm/`

## Versões preservadas

- `1065e25-rear`: `https://aledsst-ai.github.io/fvm/versions/1065e25-rear/gamepadviewer-absolute.css`

Os arquivos dentro de `versions/` incluem seus próprios assets e não são sobrescritos quando a skin principal é atualizada.

## Gamepad Viewer

Use o CSS como uma skin completa, pelo parâmetro `css=`:

```text
https://gamepadviewer.com/?p=1&css=https%3A%2F%2Faledsst-ai.github.io%2Ffvm%2Fgamepadviewer.css%3Fv%3Dtrigger-mask-stick-sockets-20260927a
```

Tamanho recomendado para a Fonte do navegador no OBS: **784 × 658 px**. O canvas inclui a altura completa dos gatilhos superiores do PSD.

## MyGamepads

Se o MyGamepads oferecer um campo **Custom CSS URL**, informe:

```text
https://aledsst-ai.github.io/fvm/gamepadviewer.css?v=trigger-mask-stick-sockets-20260927a
```

Se oferecer apenas um editor para colar CSS, copie o conteúdo de `gamepadviewer-absolute.css`, pois essa variante usa URLs completas para as imagens.

Esta skin depende da estrutura de classes do Gamepad Viewer (`.controller.custom`, `.button.pressed`, `.face.pressed` etc.). Se o MyGamepads usar nomes de elementos diferentes, será necessário adaptar os seletores ao HTML dele; hospedar o arquivo no GitHub, sozinho, não converte o formato.

O CSS público atualizado continua sendo o mesmo URL acima. Canvas atual: **784 × 658 px**. LT/RT usam `.triggers` com o recorte do PSD como máscara; a pressão gradual revela a cor sobre as peças brancas de repouso. LB/RB usam `.bumpers`. Os encaixes circulares dos analógicos cobrem as marcas irregulares que ficavam expostas durante o movimento.

## Mapa da migração

| Peça | Origem visual | Geometria/estado no novo modelo |
|---|---|---|
| Carcaça, grips e painel | grupos `Design` e `Texture` do PSD | canvas recortado 784 × 658 |
| LT / RT | `Camada 4` e `Camada 4 copiar` | imagens individuais `.trigger.left` e `.trigger.right` |
| LB / RB | metades esquerda/direita da camada `Top` | sobreposições `.bumper.left` e `.bumper.right` |
| A / B / X / Y | camadas `Buttons`, `A`, `B`, `X` e `Y` | PNGs individuais em `.abxy` |
| Analógicos | `Knobs` e `Joy Stick Bottom` | PNGs individuais em `.sticks` |
| Direcional | camada `D Pad` | PNG em `.dpad` |
| View / Menu e logo | logo do PSD e controles CSS | indicador e estados de entrada no painel central |

## Estrutura

```text
.
├── assets/
│   ├── v2-controller-base.png
│   ├── v2-controller-disconnected.png
│   ├── v2-trigger-left.png / v2-trigger-right.png
│   ├── v2-bumper-left.png / v2-bumper-right.png
│   ├── v2-stick-left.png / v2-stick-right.png
│   ├── v2-button-a.png / v2-button-b.png
│   ├── v2-button-x.png / v2-button-y.png
│   └── v2-dpad.png
├── gamepadviewer.css
├── gamepadviewer-absolute.css
└── index.html
```
