---
name: web-design-responsivo
description: "Web Design Responsivo — Páginas adaptáveis para todos os dispositivos (Tárcio Zemel, Casa do Código): estatísticas mobile, princípios do RWD (layout fluido, imagens flexíveis, media queries), medidas CSS e a fórmula alvo ÷ contexto = resultado, metatag viewport, converter layout fixo em fluido, imagens e recursos flexíveis, alta resolução, media queries, mobile first, tipografia, navegação responsiva e testes. Use ao tornar layouts responsivos ou converter sites fixos."
---

# Web Design Responsivo — Tárcio Zemel (Casa do Código)

Livro-fonte: `LivrosDev/Web Design Responsivo - Páginas adaptáveis para todos os dispositivos - Autor (Casa do Código).pdf`

## Princípios (Ethan Marcotte)
A trinca tecnológica: **layout fluido** + **imagens/recursos flexíveis** + **media queries**.

## Layout fluido
- Medidas relativas: `%`, `em`, `rem`, `vw/vh`.
- **Fórmula mágica:** `alvo ÷ contexto = resultado` (ex.: coluna de 300px em contêiner de 960px → 31.25%; fonte 24px com base 16px → 1.5em).
- `<meta name="viewport" content="width=device-width, initial-scale=1">`.
- Converter layout fixo em fluido aplicando a fórmula em larguras, margens e paddings.

## Imagens e recursos flexíveis
- `img, video, iframe { max-width: 100%; height: auto; }`.
- Embeds com proporção fixa (técnica do padding-bottom / `aspect-ratio`).
- Imagens responsivas: `srcset`, `sizes`, `<picture>`; alta resolução (2x).

## Media queries
- Sintaxe (`@media (min-width: 40em)`), breakpoints pelo **conteúdo**, em `em`.
- **Mobile first:** estilos base para telas pequenas e `min-width` para crescer.

## Outros tópicos
Tipografia fluida e legível · navegação responsiva (menu hambúrguer, off-canvas, prioridade de conteúdo) · tabelas responsivas · performance em mobile · testes em dispositivos reais e emuladores.

## Checklist
- [ ] Viewport configurado
- [ ] Sem larguras fixas em px no layout principal
- [ ] Mídia nunca extrapola o contêiner
- [ ] Breakpoints definidos pelo conteúdo
- [ ] Navegação utilizável no toque
