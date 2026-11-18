---
name: oauth2-spring-security
description: "OAuth 2.0 — Proteja suas aplicações com o Spring Security OAuth2 (Adolfo Eloy, Casa do Código): como APIs são protegidas, antipadrão de repassar credenciais, delegação de acesso, papéis do OAuth (resource owner, client, authorization server, resource server), grant types (authorization code, implicit, password, client credentials), refresh tokens, escopos, validação de tokens (introspecção, JWT) e considerações de segurança. Use ao projetar autenticação/autorização com OAuth 2.0 ou implementar com Spring Security."
---

# OAuth 2.0 com Spring Security OAuth2 — Casa do Código

Livro-fonte: `LivrosDev/Oauth 2.0 Proteja Suas Aplicacoes Com O Spring Security Oauth2 - Autor (Casa do Código).pdf`

## Fundamentos
- **Antipadrão:** cliente pedindo usuário/senha do dono do recurso para acessar outra API.
- OAuth 2.0 = **delegação de acesso** a recursos protegidos sem compartilhar credenciais.
- **Papéis:** Resource Owner (usuário), Client (aplicação), Authorization Server (emite tokens), Resource Server (API).

## Grant types
| Grant | Quando usar |
|---|---|
| **Authorization Code** (+ PKCE) | Apps web com backend e apps nativos/SPAs (com PKCE) — padrão recomendado |
| Implicit | Legado de SPA — hoje desaconselhado (use Code + PKCE) |
| Resource Owner Password Credentials | Apenas apps de primeira parte muito confiáveis — evite |
| **Client Credentials** | Comunicação máquina-a-máquina |
| **Refresh Token** | Renovar access tokens curtos sem nova autenticação |

## Implementação com Spring
1. Proteger a aplicação com Spring Security (usuários, papéis).
2. Configurar Authorization Server (clientes, segredos, redirect URIs, escopos).
3. Configurar Resource Server (validar tokens, exigir escopos por endpoint).
4. Persistir clientes e tokens em banco.
5. Cliente com Spring Security OAuth2 (RestTemplate/WebClient com token).
6. **Validação de tokens:** introspecção (token opaco) ou **JWT** assinado (validação local).
(No Spring atual: Spring Authorization Server + `oauth2ResourceServer()` + `oauth2Login()`.)

## Segurança
- Sempre **HTTPS**; validar **redirect URI** exatamente; usar `state` contra CSRF; **PKCE** para clientes públicos.
- Access tokens curtos, refresh tokens rotacionados e revogáveis; **escopos mínimos**.
- Nunca colocar segredo de cliente em app público (SPA/mobile).
- OAuth é autorização; para identidade use **OpenID Connect**.
