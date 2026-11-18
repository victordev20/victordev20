---
name: tdd-kent-beck
description: "TDD — Desenvolvimento Guiado por Testes (Kent Beck, 'Test-Driven Development: By Example'): ciclo vermelho-verde-refatorar, exemplo do dinheiro multimoeda, exemplo xUnit, passos de bebê, lista de testes, padrões de teste (teste isolado, teste primeiro, asserção primeiro, dados de teste), padrões de barra vermelha e verde (fingir, triangular, implementação óbvia), dublês, refatoração e quando usar TDD. Use ao escrever código guiado por testes ou ensinar TDD."
---

# TDD — Desenvolvimento Guiado por Testes — Kent Beck

Livro-fonte: `LivrosDev/TDD - Desenvolvimento Guiado por Testes - Autor (Ken Beck).pdf`

## O ritmo
1. **Vermelho:** escreva um pequeno teste que falha (nem compila, às vezes).
2. **Verde:** faça-o passar rapidamente, cometendo os pecados necessários.
3. **Refatore:** elimine duplicação (inclusive entre teste e código).
Objetivo: **código limpo que funciona**; reduzir medo.

## Parte I — Dinheiro multimoeda
Lista de testes (`$5 + 10 CHF = $10 se a taxa for 2:1`), `Dollar`/`Franc`, igualdade, objetos de valor, degenerar objetos, generalizar com `Money`, `Expression`, `Bank`, `Sum` — mostrando passos pequenos e design emergente.

## Parte II — Exemplo xUnit
Construir um framework de testes com TDD: `TestCase`, `setUp`, `tearDown`, contagem de resultados, `TestSuite`.

## Parte III — Padrões
- **Desenvolvimento:** teste isolado, **lista de testes**, teste primeiro, **asserção primeiro**, dados de teste e dados evidentes.
- **Barra vermelha:** teste de um passo, teste inicial, teste explicativo, teste de aprendizado, outro teste, teste de regressão, pausa, comece de novo.
- **Dublês/testes:** objeto simulado (mock), auto-shunt, string de log, crash test dummy, teste quebrado (deixe um teste falhando para retomar), check-in limpo.
- **Barra verde:** **fingir** (retornar constante), **triangular** (generalizar só com 2+ exemplos), **implementação óbvia**, um para muitos.
- Padrões de projeto e refatoração úteis em TDD (Command, Value Object, Null Object, Template Method, Composite...; reconciliar diferenças, isolar mudança, migrar dados, extrair método...).

## Quando acelerar ou desacelerar
- Confiante → implementação óbvia; incerto → fingir e triangular; perdido → passos menores.

## Checklist
- [ ] Mantenho uma lista de testes?
- [ ] Cada teste falhou antes de passar?
- [ ] Refatorei com todos os testes verdes?
- [ ] Os testes são isolados e rápidos?
