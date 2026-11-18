---
name: git-github
description: "Controlando Versões com Git e GitHub (Alexandre Aquiles & Rodrigo Ferreira, Casa do Código): repositório local (add, commit, log, diff, desfazer), remoto (push, pull, clone), GitHub, branches, merge vs rebase, conflitos, tags, fluxos de trabalho colaborativos (forks, pull requests) e boas práticas. Use em qualquer tarefa de versionamento com Git ou colaboração via GitHub."
---

# Controlando Versões com Git e GitHub — Casa do Código

Livro-fonte: `LivrosDev/Controlando Versões com Git e GitHub - Autor (Casa do Código).pdf`

## Repositório local
- `git init`, `git status`, `git add`, `git commit -m`, `git log --oneline --graph`, `git diff` / `git diff --staged`.
- `git rm`, `git mv`; `.gitignore`.
- **Desfazer:** `git checkout -- arq`/`git restore` (working tree), `git reset HEAD arq`/`git restore --staged` (stage), `git commit --amend`, `git revert <sha>` (seguro em histórico compartilhado), `git reset --hard` (destrutivo).

## Remoto
- `git remote add origin`, `git push -u origin main`, `git clone`, `git fetch`, `git pull`; protocolos HTTPS/SSH.

## GitHub
- Repositórios, issues, **forks e pull requests**, revisão de código, wikis/pages.

## Branches
- `git branch`, `git switch -c`/`checkout -b`, `git merge` (fast-forward vs merge commit), **`git rebase`** (histórico linear — nunca rebase de commits já publicados), resolução de conflitos, `git cherry-pick`, `git stash`.
- **Tags:** `git tag -a v1.0 -m`, `git push --tags`.

## Fluxos de trabalho
- Centralizado, feature branches, **Git Flow**, fluxo de fork + PR (open source).
- Integração frequente para evitar conflitos grandes.

## Boas práticas
- Commits pequenos, atômicos, mensagem no imperativo explicando o porquê.
- Nunca commitar segredos; revise com `git diff --staged` antes de commitar.
- Puxe/rebase antes de enviar; prefira `revert` a reescrever histórico público.
