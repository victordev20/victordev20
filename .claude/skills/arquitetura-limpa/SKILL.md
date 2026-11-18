---
name: arquitetura-limpa
description: "Arquitetura Limpa (Robert C. Martin): paradigmas, SOLID, princípios de componentes (REP, CCP, CRP, ADP, SDP, SAP), regra da dependência, entidades/casos de uso/adaptadores/frameworks, fronteiras e detalhes. Use ao projetar ou revisar a arquitetura de um sistema, organizar camadas/módulos ou isolar regras de negócio de frameworks e banco."
---

# Arquitetura Limpa — Robert C. Martin

Livro-fonte: `LivrosDev/Arquitetura Limpa - O Guia do Artesão para Estrutura e Design de Software - Autor (Robert C. Martin).pdf`

## Objetivo da arquitetura
Minimizar o esforço humano para construir e manter o sistema. Comportamento vs. estrutura: **estrutura (facilidade de mudar) é mais importante** a longo prazo.

## Paradigmas
- Estruturado: disciplina sobre transferência direta de controle (sem goto).
- OO: disciplina sobre transferência indireta → **polimorfismo permite inverter dependências**.
- Funcional: disciplina sobre atribuição → imutabilidade, segregar mutabilidade.

## SOLID (nível de módulo)
- **SRP:** um módulo responde a **um único ator**.
- **OCP:** estenda sem modificar; proteja componentes de alto nível.
- **LSP:** subtipos substituíveis (vale para interfaces e serviços REST também).
- **ISP:** não dependa do que não usa.
- **DIP:** dependa de abstrações estáveis; código concreto/volátil depende de abstrações.

## Componentes
- Coesão: **REP** (reuso/release), **CCP** (mudam juntos ficam juntos), **CRP** (não force dependência do que não usa).
- Acoplamento: **ADP** (sem ciclos), **SDP** (dependa na direção da estabilidade), **SAP** (estável = abstrato). Métricas I = Fan-out/(Fan-in+Fan-out), A, distância da sequência principal D = |A+I−1|.

## A Regra da Dependência
```
Frameworks & Drivers → Interface Adapters → Use Cases → Entities
```
Dependências de código-fonte apontam **somente para dentro**. Nada interno conhece nomes externos.
- **Entidades:** regras de negócio corporativas.
- **Casos de uso:** regras da aplicação; usam portas de entrada/saída (input/output boundaries).
- **Adaptadores:** controllers, presenters, gateways, view models.
- **Frameworks/drivers:** web, BD, UI — **são detalhes**.
- Cruzar fronteiras com **DTOs simples**; inverta com interfaces (DIP).

## Heurísticas
- **Arquitetura que grita:** a estrutura de pastas revela o domínio, não o framework.
- Adie decisões sobre detalhes (BD, web, framework) — mantenha opções abertas.
- **Humble Object** para testar lógica perto de fronteiras difíceis.
- Fronteiras parciais quando a completa for cara demais.
- Main é o componente mais sujo: monta tudo (injeção).
- Serviços não são arquitetura por si; fronteiras são.

## Checklist de revisão
- [ ] Entidades/casos de uso importam algo de framework, ORM ou HTTP? (não deveriam)
- [ ] Há ciclos entre módulos?
- [ ] Testes de casos de uso rodam sem BD/web?
- [ ] A estrutura de diretórios grita o domínio?
