---
name: api-rest-node
description: "Construindo APIs REST com Node.js (Caio Ribeiro Pereira, Casa do Código): Node e NPM, Express, Sequelize + SQLite/MySQL, CRUD de recursos, autenticação JWT com Passport, testes (Mocha/Chai/SuperTest), documentação (ApiDoc), CORS, logs, cluster, compressão, HTTPS e um cliente. Use ao construir ou revisar uma API REST em Node.js/Express."
---

# Construindo APIs REST com Node.js — Casa do Código

Livro-fonte: `LivrosDev/Construindo API REST com Node JS - Autor (Casa do Código).pdf`

## Passos do livro
1. Setup: Node (instalação convencional ou **NVM**), NPM (comandos, `package.json`, scripts).
2. **Express:** projeto piloto, recurso estático, carregamento modular (consign) com `models/`, `routes/`, `libs/`.
3. **Banco relacional:** Sequelize + SQLite3 (dev) / MySQL; modelos e associações.
4. **CRUD:** rotas organizadas por recurso; middleware simples; `GET /tasks`, `POST /tasks`, `GET /tasks/:id`, `PUT /tasks/:id`, `DELETE /tasks/:id` com status corretos (200, 201, 204, 404, 412).
5. **Usuários e autenticação:** **JWT** com Passport (`passport-jwt`), rota `/token`, proteger rotas, `bcrypt` para senhas.
6. **Testes:** Mocha + Chai + SuperTest; banco de teste separado; testar rotas autenticadas.
7. **Documentação:** ApiDoc a partir de comentários.
8. **Produção:** CORS, logs (winston + morgan), **cluster**, compressão GZIP, helmet, **HTTPS**.
9. Cliente web consumindo a API.

## Boas práticas de API destacadas
- Recursos no plural, verbos HTTP corretos, status codes semânticos.
- Validação e mensagens de erro consistentes.
- Configuração por ambiente (dev/test/prod).
- Tokens com expiração; nunca retornar senha.

## Checklist
- [ ] Rotas protegidas exigem JWT válido
- [ ] Usuário só acessa os próprios recursos
- [ ] Testes de integração para todas as rotas
- [ ] CORS restrito às origens necessárias
- [ ] Logs sem dados sensíveis
