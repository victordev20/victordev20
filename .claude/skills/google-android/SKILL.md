---
name: google-android
description: "Google Android — Crie aplicações para celulares e tablets (João Bosco Monteiro, Casa do Código): ambiente, estrutura do projeto, Activities e ciclo de vida, Intents e Intent Filters, layouts (LinearLayout, RelativeLayout, TableLayout) e widgets, ListView/adapters, persistência (SQLite, SharedPreferences), Content Providers, serviços, BroadcastReceivers, notificações, threads/AsyncTask, rede, mapas e suporte a tablets (fragments). Use ao desenvolver ou explicar fundamentos de apps Android nativos."
---

# Google Android — Casa do Código

Livro-fonte: `LivrosDev/Google Android - crie aplicações para celulares e tablets - Autor (Casa do Código).pdf`

## Fundamentos
- Ambiente (SDK, IDE, emulador), Hello World e estrutura do projeto (`AndroidManifest.xml`, `res/`, `layout/`, `values/`, `R`).
- Execução de apps (processo, sandbox), **componentes**: Activity, Service, BroadcastReceiver, ContentProvider.
- **Intents** explícitas e implícitas, **Intent Filters** e como são resolvidas.
- **Ciclo de vida da Activity:** `onCreate → onStart → onResume → onPause → onStop → onDestroy`; salvar estado (`onSaveInstanceState`).

## Interface
- Layouts: LinearLayout, RelativeLayout, TableLayout (hoje também ConstraintLayout); widgets (Button, EditText, DatePicker, Spinner), temas e estilos; ListView + Adapter; menus e diálogos.

## Dados e integração
- **SharedPreferences**, arquivos, **SQLite** (SQLiteOpenHelper), **Content Providers**.
- **Services** e **BroadcastReceivers**, **notificações**, alarmes.
- **Threads:** nunca bloquear a UI thread (AsyncTask/Handler no livro; hoje coroutines/WorkManager).
- Rede/HTTP, JSON, mapas e localização.
- **Tablets:** Fragments e layouts por tamanho de tela.

## Boas práticas
- Respeitar o ciclo de vida para evitar vazamentos e crashes ao rotacionar.
- Recursos (strings, dimens) fora do código para internacionalização.
- Pedir só as permissões necessárias.
- Trabalho pesado fora da main thread.
