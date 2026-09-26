# FVM — Webpixum / XISDE Gamepad Skin

Skin customizada de Xbox para o Gamepad Viewer, criada a partir da arte original em PSD.

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

Tamanho recomendado para a Fonte do navegador no OBS: **817 × 578 px**.

## MyGamepads

Se o MyGamepads oferecer um campo **Custom CSS URL**, informe:

```text
https://aledsst-ai.github.io/fvm/gamepadviewer.css
```

Se oferecer apenas um editor para colar CSS, copie o conteúdo de `gamepadviewer-absolute.css`, pois essa variante usa URLs completas para as imagens.

Esta skin depende da estrutura de classes do Gamepad Viewer (`.controller.custom`, `.button.pressed`, `.face.pressed` etc.). Se o MyGamepads usar nomes de elementos diferentes, será necessário adaptar os seletores ao HTML dele; hospedar o arquivo no GitHub, sozinho, não converte o formato.

## Estrutura

```text
.
├── assets/
│   ├── controller-base.png
│   └── controller-disconnected.png
├── gamepadviewer.css
├── gamepadviewer-absolute.css
└── index.html
```
