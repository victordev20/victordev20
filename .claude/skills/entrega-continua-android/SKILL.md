---
name: entrega-continua-android
description: "Entrega contínua em Android (Rafael Toledo, Casa do Código): pipeline de deployment para apps, integração contínua, entrega x deployment contínuo, estratégias de branching, testes unitários, análise estática, testes de integração e funcionais (Espresso), Travis CI, GoCD, Jenkins, publicação automatizada no Google Play e distribuição over-the-air. Use ao automatizar build, teste e distribuição de apps Android."
---

# Entrega Contínua em Android — Casa do Código

Livro-fonte: `LivrosDev/Entrega contínua em Android - Como automatizar a distribuição de apps - Autor (Casa do Código).pdf`

## Conceitos
- **Pipeline de deployment** aplicado a apps; **integração contínua**; **entrega contínua** (sempre pronto para publicar) × **deployment contínuo** (publica automaticamente).

## Branching
- Integração frequente; estratégias: trunk-based, feature branches curtos, release branches; feature toggles para trabalho incompleto.

## Testes automatizados
- **Unitários** (JUnit, Mockito/Robolectric) — lógica isolada da plataforma.
- **Análise estática** (Lint, Checkstyle, PMD, FindBugs/SpotBugs).
- **Integração** em Android (instrumentação).
- **Funcionais/UI** (Espresso).

## Ferramentas de CI/CD
- **Travis CI**, **GoCD**, **Jenkins** — comparação; build com Gradle; assinatura do APK/AAB com chaves seguras.
- **Publicação no Google Play** automatizada (API de publicação / plugins Gradle, faixas alpha/beta/produção).

## Distribuição over-the-air
- Requisitos para OTA; **HockeyApp** (beta testers) e **Crashlytics** (relatórios de falhas). Hoje: Firebase App Distribution / Crashlytics.

## Pipeline sugerido
```
commit → build Gradle → lint/análise → unit tests → instrumentation tests
→ APK assinado → distribuição beta (OTA) → promoção para Play Store
```
## Checklist
- [ ] Keystore e senhas fora do repositório (secrets do CI)
- [ ] Versão (versionCode) incrementada automaticamente
- [ ] Testes de UI rodando em emulador no CI
- [ ] Relatório de crashes integrado antes do release
