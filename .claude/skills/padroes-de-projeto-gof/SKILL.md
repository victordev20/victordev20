---
name: padroes-de-projeto-gof
description: "Padrões de Projeto — Soluções reutilizáveis de software orientado a objetos (Gamma, Helm, Johnson, Vlissides / GoF): o que é um padrão, princípios (programe para interface, composição sobre herança), estudo de caso do editor Lexi e os 23 padrões criacionais, estruturais e comportamentais com intenção e aplicabilidade. Use ao escolher, aplicar ou identificar padrões de projeto em código OO."
---

# Padrões de Projeto (GoF) — Gamma, Helm, Johnson, Vlissides

Livro-fonte: `LivrosDev/Padrões de Projetos - Soluções Reutilizáveis de Software Orientados a Objetos - Autor (Erich Gamma).pdf`

## Princípios
- **Programe para uma interface, não para uma implementação.**
- **Prefira composição de objetos a herança de classe.**
- Encapsule o que varia; projete para mudança.
- Padrão = nome + problema + solução + consequências.

## Criacionais
- **Abstract Factory:** famílias de objetos relacionados sem classes concretas.
- **Builder:** construção passo a passo de objeto complexo.
- **Factory Method:** subclasses decidem qual classe instanciar.
- **Prototype:** criar clonando um protótipo.
- **Singleton:** uma única instância com acesso global (use com parcimônia).

## Estruturais
- **Adapter:** converte interface em outra esperada.
- **Bridge:** separa abstração de implementação.
- **Composite:** árvores parte-todo tratadas uniformemente.
- **Decorator:** adiciona responsabilidades dinamicamente.
- **Facade:** interface simples para subsistema.
- **Flyweight:** compartilha objetos de granularidade fina.
- **Proxy:** substituto que controla acesso.

## Comportamentais
- **Chain of Responsibility**, **Command** (requisição como objeto, undo), **Interpreter**, **Iterator**, **Mediator**, **Memento** (estado para restaurar), **Observer** (notificação de dependentes), **State** (comportamento muda com o estado), **Strategy** (algoritmos intercambiáveis), **Template Method** (esqueleto com passos sobrescritos), **Visitor** (novas operações sem mudar classes).

## Como escolher (cap. 1.7)
1. Considere como padrões resolvem problemas de projeto.
2. Leia a seção **Intenção** de cada candidato.
3. Estude como os padrões se inter-relacionam.
4. Examine padrões com propósito semelhante.
5. Examine **causas de reprojeto** (dependência de classe concreta, de operações, de plataforma, de representação, de algoritmos; acoplamento forte; extensão por subclasses).
6. Considere **o que deve variar** no seu projeto.

## Mapa rápido sintoma → padrão
| Sintoma | Padrão |
|---|---|
| `if/switch` por tipo de algoritmo | Strategy |
| `if/switch` por estado do objeto | State |
| Muitas combinações de subclasses para adicionar recursos | Decorator |
| API externa incompatível | Adapter |
| Criação condicional espalhada | Factory Method / Abstract Factory |
| Ações que precisam de undo/fila | Command |
| Vários objetos reagindo a mudanças | Observer |
