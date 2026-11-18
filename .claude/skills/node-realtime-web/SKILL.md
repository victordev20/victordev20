---
name: node-realtime-web
description: "Aplicações web real time com Node.js (Caio Ribeiro Pereira, Casa do Código): event loop, assincronismo, Express, sessões, MongoDB/Redis, Socket.IO, testes e deploy. Use ao construir apps Node.js com comunicação em tempo real (chat, notificações) ou explicar o modelo não bloqueante."
---

# Aplicações Web Real Time com Node.js — Casa do Código

Livro-fonte: `LivrosDev/Aplicações web real time com Node-js - Autor (Casa do Código).pdf`

## Fundamentos
- **Problema das arquiteturas bloqueantes:** uma thread por requisição desperdiça recursos esperando I/O.
- **Node.js:** single-thread + **event loop** + I/O não bloqueante (libuv). Ótimo para I/O intenso; ruim para CPU intensa na thread principal.
- **NPM e package.json** (dependências, scripts, semver), **CommonJS** (`require`/`module.exports`), escopo de módulos.

## Desenvolvimento web
- Servidor HTTP nativo, rotas manuais → depois **Express** (scaffold, organização em `models/controllers/routes/views`, `express-load`/consign).
- Views com template engine, sessões e cookies, middlewares.
- **Evitar callback hell:** funções nomeadas, módulos pequenos, async (no Node moderno: Promises/`async-await`).

## Tempo real
- **Socket.IO:** `io.on('connection')`, `socket.emit`, `socket.broadcast`, salas (rooms), compartilhar sessão Express com o socket.
- **Redis** para sessões e pub/sub entre múltiplas instâncias; **MongoDB/Mongoose** para persistência.

## Qualidade e produção
- Testes com Mocha + SuperTest/Should.
- Performance: cluster (usar todos os núcleos), gzip, cache de estáticos, Nginx na frente.
- Process manager (forever/PM2), variáveis de ambiente por ambiente.

## Checklist para uma feature realtime
- [ ] Nenhuma operação síncrona/pesada no handler
- [ ] Autenticação do socket ligada à sessão HTTP
- [ ] Eventos com nomes claros e payload validado
- [ ] Escala horizontal via adapter Redis
- [ ] Reconexão tratada no cliente
