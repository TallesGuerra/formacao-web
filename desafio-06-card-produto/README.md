# Desafio 06 - Card de Produto

Card de produto feito com HTML e CSS puro para o desafio 06 do curso de Formação Web da Escola Nova Era.

O produto escolhido foi um fone de ouvido bluetooth. O card tem imagem, categoria, nome, descrição, preço (com o preço antigo riscado e o parcelamento) e o botão de compra.

## Como rodar

Não precisa instalar nada. Basta clonar o repositório e abrir o `index.html` no navegador.

```bash
git clone https://github.com/TallesGuerra/Desafio-Card-de-Produto.git
```

## Estrutura

```
Desafio-Card-de-Produto/
├── index.html
├── img/
│   └── fone.jpg
├── css/
│   └── style.css
└── README.md
```

## O que foi aplicado

Box Model: usei `box-sizing: border-box` em todos os elementos para o padding não aumentar a largura do card. O espaçamento interno do card vem do `padding` do `.card-conteudo`, e a distância entre título, descrição e preço é feita com `margin-bottom`.

Bordas e sombra: o card tem `border: 1px solid`, `border-radius: 16px` e `box-shadow`. Coloquei `overflow: hidden` para a imagem respeitar o arredondamento dos cantos de cima.

Fontes e cores: a fonte é a Poppins, do Google Fonts. As cores ficam em variáveis no `:root`, assim dá para trocar o tema mudando só um lugar.

Imagem: `object-fit: cover` com altura fixa, para a foto não ficar esticada.

## Parte opcional

- Hover no botão (muda a cor e aumenta um pouco) e efeito de clique com `:active`
- O card sobe e a sombra aumenta quando o mouse passa por cima
- Selo de desconto posicionado com `position: absolute` em cima da imagem
- Media query para telas até 400px, diminuindo a imagem, o padding e as fontes
- `:focus-visible` no botão para quem navega pelo teclado

## Tecnologias

- HTML5
- CSS3
- Google Fonts (Poppins)

Foto do produto: Unsplash.