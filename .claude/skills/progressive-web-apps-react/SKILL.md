---
name: progressive-web-apps-react
description: "Progressive Web Apps — Construa aplicações progressivas com React (Fernando Monteiro, Casa do Código): requisitos de uma PWA, React (componentes, props, state, ciclo de vida), create-react-app, Pure.css, Nginx, componentes da app, Service Workers e estratégias de cache, App Shell, Web App Manifest, funcionamento offline, notificações push, Lighthouse e deploy com HTTPS. Use ao transformar um app web em PWA ou auditar requisitos de PWA."
---

# Progressive Web Apps com React — Casa do Código

Livro-fonte: `LivrosDev/Progressive web apps - Construa aplicações progressivas com React - Autor (Casa do Código).pdf`

## Requisitos de uma PWA
Progressiva, responsiva, independente de conectividade, semelhante a app, sempre atualizada, segura (**HTTPS**), descobrível, reengajável (push), instalável, linkável.

## Stack do livro
- **React** (componentes, JSX, props, state, ciclo de vida), **create-react-app**, **Pure.css**, **Node/NPM**, **Nginx** para servir em produção.

## Passos
1. Backlog com os requisitos de PWA.
2. Componentes: App, cabeçalho, lista, detalhes etc.
3. **App Shell:** estrutura mínima da UI cacheada para carregar instantaneamente.
4. **Service Worker:** registro, ciclo de vida (install, activate, fetch), estratégias de cache:
   - Cache first (assets estáticos), Network first (dados que mudam), Stale-while-revalidate.
5. **Web App Manifest** (`name`, `short_name`, `icons`, `start_url`, `display: standalone`, `theme_color`, `background_color`) → "Adicionar à tela inicial".
6. Offline e sincronização; **notificações push** (Push API + Notifications API).
7. Auditoria com **Lighthouse**; deploy com HTTPS (Nginx).

## Checklist PWA
- [ ] HTTPS em produção
- [ ] Manifest com ícones 192/512 e `start_url`
- [ ] Service Worker com fallback offline
- [ ] Versionamento e limpeza de caches antigos no `activate`
- [ ] Lighthouse PWA sem falhas
