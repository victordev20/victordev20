---
name: canivete-suico-node
description: "Canivete suíço do desenvolvedor Node (Casa do Código): performance no cliente (minificação, concatenação), tratamento de erros HTTP e logs, ambientes, validação com express-validator, GZIP, cache, cluster, segurança (helmet/CSRF), envio de e-mails e manter a app no ar. Use ao endurecer e otimizar uma aplicação Express para produção."
---

# Canivete Suíço do Desenvolvedor Node — Casa do Código

Livro-fonte: `LivrosDev/Canivete suico do desenvolvedor Node - Autor (Casa do Código).pdf`

## Receitas
1. **Performance do lado do cliente** — minificar e concatenar JS/CSS (Grunt/Gulp/bundlers), reduzir requisições.
2. **Erros e logs** — middlewares de erro 404/500 no Express; conhecer `req` (params, query, body, headers) e `res` (status, json, render); logging com histórico (morgan/winston) em arquivo; **ambientes** dev/test/prod via `NODE_ENV`.
3. **Validação** — `express-validator` para checar e sanitizar entradas antes da regra de negócio.
4. **Performance e segurança** — **GZIP** (`compression`), **cache de navegador** (headers `Cache-Control`/ETag para estáticos), favicon servido de forma eficiente, **cluster** nativo para usar todos os núcleos (ou PM2), **proteções**: helmet (headers), CSRF, limitar payload, esconder `X-Powered-By`.
5. **E-mails** — Nodemailer com SMTP/serviço transacional; templates.
6. **Manter a aplicação de pé** — gerenciador de processos (forever/PM2), reinício automático, logs.
7. **Migrar Express 3 → 4** — middlewares separados, `express.Router`.

## Checklist de produção Express
- [ ] `NODE_ENV=production`
- [ ] compression + cache de estáticos
- [ ] helmet + proteção CSRF onde há sessão
- [ ] validação de todas as entradas
- [ ] handler de erro central sem vazar stack trace
- [ ] logs estruturados e rotacionados
- [ ] cluster/PM2 com restart automático
