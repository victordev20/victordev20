---
name: rest-apis
description: "REST — Construa APIs inteligentes de maneira simples (Alexandre Saudate, Casa do Código): por que REST, fundamentos do HTTP (métodos, parâmetros, cabeçalhos, media types, status codes), conceitos REST (recursos, interação por métodos, representações, HATEOAS), JAX-RS, segurança, versionamento, cache, documentação e testes de APIs. Use ao projetar, revisar ou documentar uma API REST."
---

# REST — Alexandre Saudate (Casa do Código)

Livro-fonte: `LivrosDev/REST - Construa API's inteligentes de maneira simples - Autor (Casa do Código).pdf`

## HTTP
- **Métodos:** GET (seguro, idempotente), POST (cria/processa), PUT (substitui, idempotente), PATCH (parcial), DELETE (idempotente), HEAD, OPTIONS.
- **Parâmetros:** path (`/clientes/42`), query (`?pagina=2`), headers, corpo.
- **Cabeçalhos:** `Content-Type`, `Accept` (negociação de conteúdo), `Location`, `ETag`/`If-None-Match`, `Cache-Control`, `Authorization`.
- **Media types:** `application/json`, `application/xml`, tipos customizados versionados.
- **Status:** 200, 201 (+Location), 202, 204, 301/304, 400, 401, 403, 404, 405, 409, 412, 415, 422, 429, 500, 503.

## Conceitos REST
1. **Semântica de recursos:** URIs identificam substantivos (`/pedidos/10/itens`), não verbos.
2. **Interação por métodos** uniformes.
3. **Representações distintas** do mesmo recurso (JSON/XML).
4. **Uso correto de status codes.**
5. **HATEOAS:** respostas trazem links para próximas ações.
- Stateless, cacheável, sistema em camadas.

## Implementação e operação
- JAX-RS (anotações `@Path`, `@GET`, `@Produces`...), clientes HTTP.
- **Segurança:** HTTPS, Basic/tokens/OAuth.
- **Versionamento:** na URI, no media type ou em header — escolha uma estratégia e documente.
- **Cache** com ETag e Cache-Control; **paginação**; tratamento de erros padronizado.
- Documentação (WADL/Swagger/OpenAPI) e testes automatizados.

## Checklist de design
- [ ] Recursos no plural, sem verbos na URI
- [ ] Métodos idempotentes respeitados
- [ ] 201 + Location ao criar
- [ ] Erros com corpo padronizado (código, mensagem, detalhes)
- [ ] Paginação e filtros consistentes
- [ ] Estratégia de versionamento definida
