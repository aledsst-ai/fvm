# FVM — Webpixum / XISDE Gamepad Skin

Skin customizada de Xbox para o Gamepad Viewer, criada a partir da arte original em PSD e reconstruída sobre a geometria do CSS S-Gaming fornecido como referência.
Base, controles e ombros foram separados: o PSD fornece a identidade visual, enquanto o segundo CSS fornece as posições e os estados de interação.

## URLs públicas

Após a publicação do GitHub Pages:

- CSS recomendado por URL: `https://aledsst-ai.github.io/fvm/gamepadviewer.css`
- CSS com imagens absolutas, indicado para copiar e colar: `https://aledsst-ai.github.io/fvm/gamepadviewer-absolute.css`
- Prévia: `https://aledsst-ai.github.io/fvm/`

## Gamepad Viewer

Use o CSS como uma skin completa, pelo parâmetro `css=`:

```text
https://gamepadviewer.com/?p=1&css=https%3A%2F%2Faledsst-ai.github.io%2Ffvm%2Fgamepadviewer.css
```

Tamanho recomendado para a Fonte do navegador no OBS: **784 × 558 px**. LT/RT e LB/RB ficam integralmente dentro desse canvas e não dependem de escala ou altura extra.

## MyGamepads

Se o MyGamepads oferecer um campo **Custom CSS URL**, informe:

```text
https://aledsst-ai.github.io/fvm/gamepadviewer.css
```

Se oferecer apenas um editor para colar CSS, copie o conteúdo de `gamepadviewer-absolute.css`, pois essa variante usa URLs completas para as imagens.

Esta skin depende da estrutura de classes do Gamepad Viewer (`.controller.custom`, `.button.pressed`, `.face.pressed` etc.). Se o MyGamepads usar nomes de elementos diferentes, será necessário adaptar os seletores ao HTML dele; hospedar o arquivo no GitHub, sozinho, não converte o formato.

O CSS público atualizado continua sendo o mesmo URL acima. O canvas agora segue o segundo modelo: **784 × 558 px**. LT/RT usam `.triggers`; LB/RB usam `.bumpers`; todos os estados continuam independentes e compatíveis com a estrutura padrão do GamePad Viewer.

## Mapa da migração

| Peça | Origem visual | Geometria/estado no novo modelo |
|---|---|---|
| Carcaça, grips e painel | grupos `Design` e `Texture` do PSD | base 784 × 558 do CSS S-Gaming |
| LT / RT | camada `Triger Buttons` e paleta azul do PSD | `.triggers`, silhuetas individuais do segundo CSS |
| LB / RB | camada `Triger Buttons` e paleta azul do PSD | `.bumpers`, silhuetas individuais do segundo CSS |
| A / B / X / Y | camadas `A`, `B`, `X`, `Y` e `Buttons` | coordenadas do bloco `.abxy` do segundo CSS |
| Analógicos | camadas `Knobs` e `Joy Stick Bottom` | bloco `.sticks` do segundo CSS |
| Direcional | camada `D Pad` | bloco `.dpad` do segundo CSS |
| View / Menu e logo | camadas centrais do PSD | centro e indicador do segundo CSS |

## Estrutura

```text
.
├── assets/
│   ├── controller-base.png
│   ├── controller-base-structure.png
│   ├── controller-body-disconnected.png
│   ├── controller-reference-base.png
│   ├── controller-reference-disconnected.png
│   ├── webpixum-trigger.png
│   ├── webpixum-bumper.png
│   └── webpixum-stick.png
├── gamepadviewer.css
├── gamepadviewer-absolute.css
└── index.html
```
