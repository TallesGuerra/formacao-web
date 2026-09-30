# Discord Clone

Desafio 12 da formação web da Escola Nova Era. A ideia foi reproduzir a tela principal do Discord (a de dentro do app, com servidores e canais) usando só HTML e CSS.

## O que tem na página

A tela é dividida em três colunas:

1. Barra de servidores à esquerda, com os ícones redondos que viram quadrado arredondado no hover e a barrinha branca indicando o servidor ativo.
2. Lista de canais, com o nome do servidor no topo, canais de texto e de voz separados por grupo e o painel do usuário embaixo.
3. Área do chat, com header mostrando o canal atual, as mensagens e o campo de digitar.

## Como fiz o layout

O container `.app` usa `display: flex` com `height: 100vh`, então a página ocupa sempre a altura inteira da janela. As duas primeiras colunas têm largura fixa (72px e 240px) e `flex-shrink: 0` pra não espremer. A área do chat usa `flex: 1` e pega o resto.

Dentro das colunas usei `flex-direction: column`. Só a lista de canais e a lista de mensagens têm `overflow-y: auto`, assim o header e o campo de mensagem ficam parados e só o meio rola.

As cores estão em variáveis no `:root`, peguei do tema escuro do Discord.

Abaixo de 700px a coluna de canais some. Não fiz menu mobile.

## Como rodar

Não precisa instalar nada. Abre o `index.html` no navegador ou usa a extensão Live Server no VS Code.

## Arquivos

```
index.html
style.css
README.md
```