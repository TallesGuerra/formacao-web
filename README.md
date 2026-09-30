# Discord Clone

Desafio 12 da formação web da Escola Nova Era. Reproduzi a página inicial do Discord usando só HTML e CSS. Também fiz uma versão da tela de dentro do app, que abre pelo botão "Abrir o Discord no navegador".

## Páginas

**index.html**: a página inicial, com navbar, hero, cards de recursos, uma chamada final e footer.

**app.html**: a tela do app, com barra de servidores, lista de canais e área do chat.

## Como fiz

A navbar usa `position: sticky` para continuar no topo quando a página rola. Os links do menu levam para as seções da própria página (`#baixar`, `#recursos`, `#rodape`), e o `scroll-behavior: smooth` faz a rolagem ficar suave.

O hero tem uma imagem de fundo (`img/hero-bg.svg`) aplicada com `background-image`, `background-size: cover` e `background-position: center bottom`, para as ondas ficarem sempre coladas embaixo. As imagens dos cards também são de fundo, cada card tem sua classe (`.card-img-1`, `.card-img-2`...). Desenhei os SVGs eu mesmo, porque as ilustrações originais do Discord têm direito autoral.

Os cards ficam num grid de duas colunas (`grid-template-columns: repeat(2, 1fr)`). O footer também usa grid, com a primeira coluna maior (`2fr 1fr 1fr 1fr`).

Na tela do app o container usa `display: flex` com `height: 100vh`. As colunas de servidores e de canais têm largura fixa e o chat ocupa o resto com `flex: 1`. Só a lista de canais e a de mensagens rolam.

As cores ficam em variáveis no `:root`.

## Responsivo

Abaixo de 900px os links do menu somem e os cards passam para uma coluna. Abaixo de 560px a imagem do card vai para cima do texto. Não fiz menu mobile com botão.

## Hover

Os botões ganham sombra, os cards sobem um pouco e os ícones dos servidores no app viram quadrado arredondado.

## Estrutura

```
index.html
app.html
css/
  style.css
  app.css
img/
  hero-bg.svg
  card-1.svg ... card-4.svg
README.md
```

## Como rodar

Abrir o `index.html` no navegador ou usar o Live Server do VS Code.