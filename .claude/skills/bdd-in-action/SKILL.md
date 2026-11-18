---
name: bdd-in-action
description: "BDD in Action (John Ferguson Smart): Behavior-Driven Development de ponta a ponta — Feature Injection, impact mapping, exemplos concretos, Gherkin (Given/When/Then), automação de critérios de aceitação, documentação viva e BDD em testes unitários. Use ao levantar requisitos com exemplos, escrever cenários Gherkin ou estruturar testes de aceitação."
---

# BDD in Action — John Ferguson Smart

Livro-fonte: `LivrosDev/BDD in Action - Behavior-Driven Development for the Whole Software Lifecycle - Autor (John Ferguson Smart).pdf`

## Por que BDD
Dois problemas: **construir certo** (qualidade técnica) e **construir a coisa certa** (valor). BDD ataca a **restrição de conhecimento** com conversas sobre **exemplos concretos** entre negócio, dev e QA (os "Three Amigos").

## Fluxo
1. **Objetivos de negócio** (aumentar receita, reduzir custo, proteger receita, evitar custos futuros).
2. **Feature Injection / Impact Mapping:** objetivo → atores → impactos → entregáveis (features).
3. **Histórias** que entregam capacidades.
4. **Exemplos** que ilustram regras de negócio → **critérios de aceitação executáveis**.
5. Automação (Cucumber/JBehave/SpecFlow/Serenity) → **documentação viva** com relatórios.
6. BDD também no nível unitário: testes descrevem comportamento ("should …").

## Escrevendo bons cenários
```gherkin
Feature: Consultar próximo trem
  Scenario: Viajante consulta horários na linha principal
    Given a linha "Western" tem trens às 7:58, 8:00 e 8:02
    When eu quero ir de "Parramatta" para "Town Hall" às 7:55
    Then devo ver os horários 7:58, 8:00 e 8:02
```
- Linguagem do negócio, **declarativa** (o quê), não imperativa (cliques).
- Um comportamento por cenário; use **Scenario Outline + Examples** para tabelas.
- Background para contexto comum, sem exagero.

## Automação sustentável
- Camadas: cenário → step definitions → **objetos de domínio/tarefas** (Screenplay/Page Objects) → driver.
- Evite acoplamento a detalhes de UI; teste regras em níveis inferiores quando possível.
- Rode no CI; relatórios mostram features prontas/pendentes.

## Desvantagens a gerenciar
- Exige engajamento do negócio; cenários mal escritos geram custo de manutenção alto.
