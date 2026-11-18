---
name: html5-css3
description: "HTML5 e CSS3 — Domine a web do futuro (Lucas Mazza, Casa do Código): estado dos navegadores e prefixos, HTML semântico, novas tags e atributos (data-*), box model, posicionamento e float, seletores CSS3, web fonts, bordas arredondadas, sombras, gradientes, transições, transformações, animações e media queries. Use ao construir páginas com HTML semântico e CSS moderno."
---

# HTML5 e CSS3 — Lucas Mazza (Casa do Código)

Livro-fonte: `LivrosDev/HTML5 e CSS3 - domine a web do futuro - Autor (Casa do Código).pdf`

## Fundamentos
- Escreva HTML **de dentro para fora**: conteúdo e estrutura primeiro, depois estilo.
- Navegadores e **prefixos proprietários** (`-webkit-`, `-moz-`) — use autoprefixer hoje.

## HTML5
- Doctype simples, `meta charset`, menos código.
- **Tags semânticas:** `header`, `nav`, `main`, `section`, `article`, `aside`, `footer`, `figure/figcaption`, `time`.
- **Atributos personalizados** `data-*`.
- Formulários novos (`required`, `placeholder`, `type=email/url/number/date`), `audio`/`video`.
- Seja pragmático: semântica ajuda acessibilidade e SEO.

## CSS essencial
- **Box model** (`content`, `padding`, `border`, `margin`; `box-sizing: border-box`).
- Display, posicionamento (static, relative, absolute, fixed), float/clear (hoje: flexbox e grid).
- Seletores CSS3: atributo, `:nth-child`, `:not`, `::before/::after`.

## CSS3 visual
- `@font-face`/web fonts, `border-radius`, `box-shadow`, `text-shadow`, `rgba`/opacidade, **gradientes**, múltiplos backgrounds.
- **Transições**, **transformações** (translate, rotate, scale), **animações** com `@keyframes`.
- **Media queries** para design responsivo.

## Checklist
- [ ] Estrutura semântica (um `h1`, hierarquia de headings)
- [ ] `alt` em imagens e `label` em inputs
- [ ] CSS separado do HTML, sem estilos inline
- [ ] Animações respeitam `prefers-reduced-motion`
