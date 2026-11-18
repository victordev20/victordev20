---
name: a-web-mobile
description: "Desenvolvimento web para muitos dispositivos (Sérgio Lopes, Casa do Código): estratégia mobile, design responsivo, mobile-first, viewport, media queries, imagens responsivas, progressive enhancement, gestos e formulários mobile. Use ao construir ou revisar front-end que precisa funcionar bem em celulares."
---

# A Web Mobile — Sérgio Lopes (Casa do Código)

Livro-fonte: `LivrosDev/A Web Mobile - Programe para um Mundo de Muitos Dispositivos - Autor (Casa do Código).pdf`

## Estratégia
- App nativo vs. web: compare alcance, custo, acesso a APIs, distribuição. Prefira **uma web única** e responsiva quando possível.
- **Mobile-first:** comece pelo contexto mais restrito e acrescente para telas maiores (força priorização de conteúdo).
- Teste em dispositivos reais; conheça o mercado de browsers.

## Programando a web moderna
- **Layouts fluidos** (%, em, rem, max-width) + **media queries**.
- Sempre: `<meta name="viewport" content="width=device-width, initial-scale=1">`.
- **Não remova o zoom** (`user-scalable=no` prejudica acessibilidade).
- Breakpoints **baseados no conteúdo**, não em aparelhos específicos.
- Prefira media queries `min-width` (mobile-first).
- Telas retina: pixel CSS ≠ pixel físico; use `srcset`, SVG, `resolution` em media queries.

## Web adaptativa
- **Progressive enhancement** e **feature detection** (não browser sniffing).
- **RESS:** componentes adaptados também no servidor.
- **Imagens responsivas:** `<picture>`, `srcset`/`sizes`, carregamento condicional e lazy loading.

## Gestos e entrada
- Eventos touch/pointer; áreas de toque ≥ ~44px; evite hover como único gatilho.
- Use input types semânticos do HTML5 (`email`, `tel`, `number`, `date`) para teclados adequados.
- Formulários mobile: menos campos, rótulos visíveis, autocomplete, validação clara.

## Performance mobile
- Reduza requisições e peso; cache; adie JS não essencial; otimize o caminho crítico.

## Checklist de revisão
- [ ] Viewport correto e sem bloquear zoom
- [ ] CSS mobile-first com breakpoints de conteúdo
- [ ] Imagens com `srcset`/`sizes`
- [ ] Alvos de toque adequados
- [ ] Inputs com tipos semânticos
- [ ] Funciona sem JS para o conteúdo essencial
