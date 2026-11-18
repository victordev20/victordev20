---
name: entrega-continua
description: "Entrega Contínua (Jez Humble & David Farley): antipadrões de release, princípios (automatize quase tudo, versione tudo, se dói faça com frequência, qualidade embutida, 'pronto' = em produção), gerência de configuração, integração contínua, estratégia de testes, pipeline de implantação (commit, aceitação, capacidade, manual, release), deploy e rollback, infraestrutura, dados e controle de versão avançado. Use ao desenhar ou melhorar pipelines de CI/CD."
---

# Entrega Contínua — Jez Humble & David Farley

Livro-fonte: `LivrosDev/Entrega Contínua - Como Entregar Software de Forma Rápida e Confiável - Auto (Jez Humble).pdf`

## Antipadrões
Implantar manualmente; implantar em ambiente similar a produção só no fim; gerência de configuração manual de produção.

## Princípios
1. Crie um processo **repetível e confiável** de entrega.
2. **Automatize quase tudo.**
3. **Mantenha tudo sob controle de versão** (código, testes, scripts, config, infra, docs).
4. **Se é difícil, faça com mais frequência.**
5. **Qualidade embutida** desde o início.
6. **Pronto = entregue** (em produção ou pronto para).
7. Todos são responsáveis pelo processo de entrega.
8. **Melhoria contínua.**
Toda mudança dispara feedback, o mais rápido possível, e o time age sobre ele. **Todo check-in é uma versão candidata.**

## Pipeline de implantação
```
Commit (compila, testes unitários, análise, artefato) → Testes de aceitação automatizados
→ Testes de capacidade/performance → Testes manuais/exploratórios → Release em produção
```
- **Construa os binários uma única vez** e promova o mesmo artefato.
- Implante do mesmo jeito em todos os ambientes; faça smoke test após o deploy.
- Se qualquer estágio falhar, **pare a linha**.

## Práticas
- **Integração contínua:** check-in frequente na mainline, build rápido (<10 min), não commitar sobre build quebrado, nunca ir para casa com build quebrado, corrigir ou reverter.
- **Estratégia de testes:** quadrantes de testes ágeis; testes de aceitação via camada de aplicação (não UI frágil); dublês de teste.
- **Gerência de configuração e dependências**; ambientes como código; gestão de dados (migrations versionadas, reversíveis).
- **Release:** blue-green, canário, feature toggles, **branch by abstraction**, rollback planejado e testado.
- Desenvolver na **mainline** (trunk-based) em vez de branches longos.

## Checklist de pipeline
- [ ] Um commit gera artefato versionado em < 10 min
- [ ] O mesmo artefato vai de teste até produção
- [ ] Deploy é um comando/um clique e é idempotente
- [ ] Rollback testado
- [ ] Migrações de banco versionadas e automatizadas
