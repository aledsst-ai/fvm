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

O CSS público atualizado continua sendo o mesmo URL acima. O canvas permanece em 817 × 578 px. LT/RT mantêm seus hooks de estado, mas não exibem uma arte própria: quando acionados, reutilizam visualmente os elementos correspondentes de LB/RB. A implementação segue a mesma lógica do template padrão: cada grupo (`.sticks`, `.triggers`, `.bumpers`) é o contêiner e os controles são filhos posicionados dentro dele.

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
