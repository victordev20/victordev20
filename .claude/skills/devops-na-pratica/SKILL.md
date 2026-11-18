---
name: devops-na-pratica
description: "DevOps na Prática — Entrega de software confiável e automatizada (Danilo Sato, Casa do Código): ambiente de produção, monitoramento com Nagios, infraestrutura como código com Puppet, pipeline de entrega com Jenkins, integração contínua, testes, deploy na nuvem (AWS) e tópicos avançados. Use ao montar do zero monitoramento, IaC e pipeline de deploy para uma aplicação."
---

# DevOps na Prática — Danilo Sato (Casa do Código)

Livro-fonte: `LivrosDev/DevOps na Prática - Entrega de Software Confiável e Automatizada - Autor (Casa do Código).pdf`

## Abordagem
Contrasta a abordagem tradicional (silos dev × ops, deploys raros e manuais) com **DevOps e entrega contínua** usando uma loja virtual de exemplo.

## Passos
1. **Tudo começa em produção:** instalar servidores (web + banco), dependências, build e deploy manual — para entender o que automatizar.
2. **Monitoramento:** servidor Nagios, verificações de hosts e serviços, checagens específicas (HTTP, banco), **alertas**; o que fazer quando um problema atinge produção.
3. **Infraestrutura como código:** provisionamento vs configuração vs deploy; **Puppet** (recursos, provedores, manifestos, dependências); reinstalar banco e web por código.
4. **Puppet além do básico:** classes, tipos definidos, módulos, separação infraestrutura × aplicação, Puppet Forge.
5. **Integração contínua:** práticas (commit frequente, build rápido, testes automatizados), Jenkins.
6. **Pipeline de entrega:** estágios (commit → testes → empacotamento → deploy), artefatos versionados, promoção entre ambientes, deploy com um clique.
7. **Nuvem:** provisionar na AWS com as mesmas receitas.
8. **Tópicos avançados:** deploy contínuo, feature toggles, blue/green, canário, segurança, métricas.

## Princípios
- Automatize o repetível, versione tudo, monitore antes de precisar.
- Mesmo artefato em todos os ambientes; configuração externa.
- Feedback rápido e pequenas mudanças reduzem risco.
