---
name: caixa-de-ferramentas-devops
description: "Caixa de Ferramentas DevOps (Guto Carvalho, Casa do Código): Linux, SSH e Git; Vagrant + VirtualBox; Ansible (playbooks, YAML, refatoração em roles); WordPress em uma e duas máquinas com Nginx como proxy reverso; provisionamento na DigitalOcean e AWS; Cassandra. Use ao automatizar provisionamento e configuração de servidores com Vagrant e Ansible."
---

# Caixa de Ferramentas DevOps — Casa do Código

Livro-fonte: `LivrosDev/Caixa de Ferramentas DevOps - Um Guia para Construção, Administração e Arquitetura de Sistemas Modernos - Autor (Casa do Código).pdf`

## Ferramentas e ordem de aprendizado
1. **Linux, SSH e Git** — base de tudo (chaves SSH, `~/.ssh/config`, versionar infraestrutura).
2. **Vagrant + VirtualBox** — ambientes locais reproduzíveis (`Vagrantfile`, `vagrant up/ssh/destroy`, rede privada, múltiplas VMs).
3. **Ansible** — configuração sem agente via SSH: inventário, **playbooks em YAML**, módulos (apt, template, service, copy), handlers, variáveis, **roles** (refatoração), idempotência.
4. **Integração Ansible + Vagrant** (provisioner `ansible`).

## Projetos práticos
- **WordPress em uma máquina:** Nginx/Apache + PHP + MySQL via playbook.
- **WordPress em duas máquinas:** web separada do banco, **Nginx como proxy reverso**.
- **Nuvem:** mesmos playbooks provisionando na **DigitalOcean (API v2)** e na **AWS EC2**.
- **Cassandra:** cluster com Vagrant e depois na AWS.

## Princípios
- Infraestrutura como código, versionada e revisada.
- **Idempotência:** rodar o playbook N vezes leva ao mesmo estado.
- Mesmo código para dev (Vagrant) e produção (nuvem) → menos "na minha máquina funciona".
- Refatore playbooks em roles reutilizáveis.

## Checklist de playbook
- [ ] Usa módulos em vez de `shell` sempre que possível
- [ ] Templates (`.j2`) para configs, com handlers de restart
- [ ] Segredos fora do repositório (Ansible Vault)
- [ ] Testado em Vagrant antes da nuvem
