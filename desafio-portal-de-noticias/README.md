# Portal de Notícias

Desafio 05 da Formação Web da Escola Nova Era. A proposta era montar um portal de notícias usando as tags semânticas do HTML: `header`, `nav`, `main`, `article`, `aside` e `footer`.

O portal se chama Nova Era Notícias e todas as notícias são inventadas, sobre uma cidade fictícia com o mesmo nome. Fiz assim pra não usar texto de jornal de verdade.

## Páginas

**index.html**: a capa, com a notícia em destaque, uma grade com mais cinco notícias e a sidebar.

**noticias/**: uma página pra cada notícia. É pra lá que o "Leia mais" leva.

## Estrutura

O `header` tem o nome do portal, a data e o `nav` com o menu. Os links do menu levam até a notícia de cada categoria na própria página, porque cada `article` tem um `id` (`#economia`, `#esportes`...). Nas páginas de notícia os mesmos links apontam pra `../index.html#economia`, então o menu funciona de qualquer lugar.

Dentro do `main` as notícias ficam separadas em duas `section`: a do destaque e a de "Mais notícias". Cada notícia é um `article` com categoria, título, resumo, data e o link "Leia mais". A data usa a tag `time` com o atributo `datetime`, que guarda a data num formato que programa consegue ler (`2026-10-01`), enquanto o texto aparece do jeito normal pra quem lê.

A sidebar é um `aside` com três blocos: as mais lidas (lista numerada com `ol`), os destaques da semana com miniatura e as categorias.

Coloquei o `aside` do lado do `main`, e não dentro dele. O `main` é o conteúdo principal da página e a sidebar é um complemento, então faz mais sentido ficarem separados.

## CSS

O layout da capa é um grid de duas colunas (`1fr 300px`): as notícias ocupam o espaço que sobra e a sidebar fica com largura fixa. A grade de notícias usa `repeat(auto-fill, minmax(230px, 1fr))`, então o número de colunas muda sozinho conforme o espaço.

Na notícia em destaque o texto fica por cima da foto, com `position: absolute` e um degradê escuro embaixo pra dar leitura.

As fontes são Merriweather nos títulos e Roboto no texto, do Google Fonts. As cores ficam em variáveis no `:root`.

## Responsivo

Abaixo de 860px a sidebar desce pra baixo das notícias. Abaixo de 560px o resumo do destaque some e o menu rola pro lado em vez de quebrar em várias linhas.

## Como abrir

Só abrir o `index.html` no navegador. As fotos são do Unsplash e estão na pasta `img`.