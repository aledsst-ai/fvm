# FVM — Webpixum / XISDE Gamepad Skin

Skin customizada de Xbox para o Gamepad Viewer, criada a partir da arte original em PSD.
Os analógicos agora usam recortes móveis do PSD e a hierarquia de posicionamento do template padrão, em vez de duplicar um analógico estático do fundo.

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

Tamanho recomendado para a Fonte do navegador no OBS: **817 × 578 px**. Os gatilhos LT/RT ficam dentro desse canvas padrão, sem depender de altura extra.

## MyGamepads

Se o MyGamepads oferecer um campo **Custom CSS URL**, informe:

```text
https://aledsst-ai.github.io/fvm/gamepadviewer.css
```

Se oferecer apenas um editor para colar CSS, copie o conteúdo de `gamepadviewer-absolute.css`, pois essa variante usa URLs completas para as imagens.

Esta skin depende da estrutura de classes do Gamepad Viewer (`.controller.custom`, `.button.pressed`, `.face.pressed` etc.). Se o MyGamepads usar nomes de elementos diferentes, será necessário adaptar os seletores ao HTML dele; hospedar o arquivo no GitHub, sozinho, não converte o formato.

O CSS público atualizado continua sendo o mesmo URL acima. O canvas permanece em 817 × 578 px. A organização dos ombros segue o CSS de referência: LT/RT ficam no grupo superior `.triggers`, enquanto LB/RB ficam no grupo `.bumpers` logo abaixo. A implementação mantém a lógica padrão do GamePad Viewer, com estados analógicos e pressionados separados.

## Estrutura

```text
.
├── assets/
│   ├── controller-base.png
│   ├── controller-base-structure.png
│   ├── controller-body-disconnected.png
│   ├── trigger.svg
│   ├── bumper.svg
│   ├── stick.png
│   └── triggers-static.png
├── gamepadviewer.css
├── gamepadviewer-absolute.css
└── index.html
```
