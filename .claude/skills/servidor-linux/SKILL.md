---
name: servidor-linux
description: "Guia prático do servidor Linux — Administração Linux para iniciantes (Casa do Código): terminal e shell, ajuda, comandos GNU, FHS, Vim, shell script, redes, pacotes, SSH, particionamento, quotas, kernel, hardening, NFS, RAID, LVM, Samba como controlador de domínio, Apache, proxy (Squid), DHCP, DNS, firewall. Use para configurar e endurecer servidores Linux (Debian)."
---

# Guia Prático do Servidor Linux — Casa do Código

Livro-fonte: `LivrosDev/Guia prático do servidor Linux - Administração Linux para iniciantes - Autor (Casa do Código).pdf`

## Capítulos
1. Ambiente de estudo (VMs Debian).
2. Primeiros passos: terminais virtuais, logon, shell, teclado, histórico.
3. Obtendo ajuda: `man`, `info`, `--help`, `apropos`.
4. Comandos GNU/Linux essenciais.
5. **FHS** — hierarquia de diretórios.
6. **Vim**.
7. **Shell script** básico.
8. **Redes:** interfaces (`/etc/network/interfaces`), IP, rotas, DNS cliente.
9. **Pacotes:** `apt`, `dpkg`, repositórios.
10. **SSH:** chaves, trocar porta padrão, desabilitar login de root e senha.
11. **Particionamento** (`fdisk`, sistemas de arquivos ext4/XFS/ReiserFS, `/etc/fstab`).
12. **Quotas de disco**.
13. **Kernel** e módulos.
14. **Hardening:** remover serviços desnecessários, atualizações, permissões, sudo, fail2ban, firewall, auditoria de logs.
15. **NFS** (compartilhamento).
16. **RAID** por software (`mdadm`).
17. **LVM** (PV, VG, LV, redimensionar).
18. **Samba** como controlador de domínio.
19. **Apache** (virtual hosts, módulos, HTTPS).
20. **Proxy** (Squid) e serviços adicionais (DHCP, DNS/Bind, iptables).

## Checklist de hardening
- [ ] SSH só com chave, sem root, porta e AllowUsers configurados
- [ ] Firewall com política padrão de negar
- [ ] Atualizações automáticas de segurança
- [ ] Serviços não usados desabilitados
- [ ] Logs monitorados e rotacionados
- [ ] Backups testados
