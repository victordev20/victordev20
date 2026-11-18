---
name: arquitetura-design-java
description: "Introdução à Arquitetura e Design de Software — Uma visão sobre a plataforma Java (Paulo Silveira, Guilherme Silveira e outros, Casa do Código): plataforma e JVM (GC, JIT, classloaders), OO (programar para interface, composição sobre herança, imutabilidade, evitar modelo anêmico, DDD), acoplamento e coesão, injeção de dependência, persistência e ORM (JPA/Hibernate, lazy loading, N+1, cache), web (MVC, REST), integração, testes e arquitetura. Use em decisões de design orientado a objetos e arquitetura de sistemas Java/JVM."
---

# Introdução à Arquitetura e Design de Software — Caelum / Casa do Código

Livro-fonte: `LivrosDev/Introdução à arquitetura de design de software - Autor (Paulo Silveira).pdf`

## Plataforma Java
- Java é plataforma além da linguagem; especificações ajudam e atrapalham; **use a linguagem certa para cada problema** (JVM poliglota).
- **JVM:** princípios de garbage collection (gerações), não dependa do GC para liberar recursos (feche conexões), **JIT**, classloaders e "classloader hell".

## Orientação a objetos
- **Programe voltado à interface**, não à implementação.
- **Componha comportamentos**; **evite herança, favoreça composição**.
- **Favoreça imutabilidade e simplicidade.**
- **Cuidado com o modelo anêmico**; considere **DDD**.

## Separação de responsabilidades
- **Baixo acoplamento e alta coesão.**
- **Injeção de dependência** (manual ou framework — Spring, CDI); fábricas e o mito do baixo acoplamento; proxies dinâmicos e geração de bytecode (AOP).

## Persistência
- JDBC → **JPA/Hibernate**; mapeamento, **lazy loading**, problema **N+1**, cache de primeiro/segundo nível, transações, Open Session in View e seus riscos; quando usar SQL direto.

## Web, integração e testes
- MVC action-based vs component-based; REST; serialização (JSON/XML).
- Integração entre sistemas: mensageria, web services, idempotência.
- Testes automatizados (unidade, integração, aceitação), TDD e design.

## Checklist de revisão de design
- [ ] Dependências por interfaces e injetadas
- [ ] Herança só para "é-um" verdadeiro
- [ ] Objetos de valor imutáveis
- [ ] Sem N+1 nas consultas críticas
- [ ] Regras de negócio nas entidades/serviços de domínio, não em controllers
