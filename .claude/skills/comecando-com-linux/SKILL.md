---
name: comecando-com-linux
description: "Começando com o Linux — Comandos, serviços e administração (Daniel Romero, Casa do Código): shell, diretórios e arquivos, Vim/Nano, cat/head/tail, tar/gzip/zip, FHS, usuários e permissões, processos, pacotes, rede, serviços e shell script básico. Use para ensinar ou executar tarefas básicas de administração em Linux (Ubuntu)."
---

# Começando com o Linux — Casa do Código

Livro-fonte: `LivrosDev/Começando com o Linux - Comandos, serviços e administração - Autor (Casa do Código).pdf`

## Trilha
1. **O que é Linux e Ubuntu**, instalação e navegação.
2. **Shell:** `pwd`, `ls -la`, `cd`, `mkdir -p`, `cp -r`, `mv`, `rm -r`, `touch`; ajuda com `man`, `--help`, `whatis`; localizar com `find`, `locate`, `which`.
3. **Editores:** Vim (modos normal/inserção/comando: `i`, `Esc`, `:w`, `:q!`, `dd`, `yy`, `p`, `/busca`) e Nano.
4. **Visualizar arquivos:** `cat`, `less`, `head -n`, `tail -f`.
5. **Compactação:** `tar -czvf arq.tar.gz dir/`, `tar -xzvf`, `gzip/gunzip`, `zip/unzip`.
6. **Estrutura de diretórios (FHS):** `/bin`, `/etc`, `/home`, `/var`, `/usr`, `/opt`, `/tmp`, `/proc`, `/sys`.
7. **Usuários e permissões:** `adduser`, `usermod -aG`, `passwd`, `sudo`; `chmod 755`/`u+x`, `chown user:group`; rwx para dono/grupo/outros.
8. **Processos:** `ps aux`, `top/htop`, `kill`, `jobs`, `bg/fg`, `&`.
9. **Pacotes:** `apt update`, `apt install`, `apt remove`, `dpkg -i`.
10. **Rede e serviços:** `ip a`, `ping`, `ssh`, `scp`, `systemctl start/stop/status/enable`.
11. **Shell script:** shebang, variáveis, `if`, `for`, `while`, parâmetros `$1`, `$#`, exit codes.

## Boas práticas
- Use `sudo` só quando necessário; evite logar como root.
- Princípio do menor privilégio em permissões (nada de `chmod 777`).
- Faça backup antes de editar arquivos em `/etc`.
