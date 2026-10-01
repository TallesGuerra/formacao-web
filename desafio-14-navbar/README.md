# NAVBAR# Desafio 14 - Navbar

Menu de navegação feito só com HTML e CSS, sem JavaScript. Faz parte dos desafios de front-end da Escola Nova Era.

## O que tem

- Logo e links principais alinhados com flexbox
- Submenu em "Serviços" e "Projetos", que abre no hover (e também com Tab, pelo `:focus-within`)
- Link ativo marcado com `aria-current="page"`, que o CSS usa como seletor
- Hover com mudança de cor e uma linha que cresce embaixo do link (`::after` com `scaleX`)
- Versão mobile com menu hambúrguer usando um checkbox escondido

## Como rodar

Basta abrir o `index.html` no navegador. Não tem dependência nenhuma.

## Estrutura

```
index.html
style.css
README.md
```

## Algumas decisões

Usei `aria-current` no lugar de uma classe `.active` porque ele já informa pro leitor de tela qual é a página atual, então resolve duas coisas com um atributo só.

O submenu abre com `opacity` e `visibility` em vez de `display: none`, porque `display` não anima. Tive um problema no começo em que o submenu fechava quando o mouse passava pelo espaço entre o link e a caixa; resolvi com um `::before` invisível que cobre esse vão.

No mobile o menu abre com o truque do checkbox: o `label` é o botão, e o seletor `:checked ~ .menu` mostra a lista. Funciona, mas num projeto real eu faria com um pouco de JavaScript e `aria-expanded`, que é mais acessível.

## Conceitos praticados

Flexbox, pseudo-classes (`:hover`, `:focus-within`, `:focus-visible`, `:checked`), pseudo-elementos, seletores de atributo, seletores de irmão (`~` e `+`), variáveis CSS, transições e media query.