---
name: tdd-mundo-real
description: "Test-Driven Development — Teste e design no mundo real (Mauricio Aniche, Casa do Código): testes de unidade, ciclo do TDD, simplicidade e baby steps, TDD e design de classes (coesão, acoplamento, encapsulamento, herança), feedback dos testes sobre o design, mocks, testes de integração, qualidade dos testes, TDD em código legado e quando não usar. Use ao praticar TDD em projetos reais ou interpretar o que os testes dizem sobre o design."
---

# Test-Driven Development: Teste e Design no Mundo Real — Mauricio Aniche

Livro-fonte: `LivrosDev/Test-Driven Development - Teste e Design no Mundo Real - Autor (Casa do Código).pdf`

## Fundamentos
- Por que testar (e por que não testamos); testes automatizados vs TDD.
- **Teste de unidade:** testa uma classe isolada; cenário → ação → validação.
- Ciclo TDD com o problema dos **números romanos**; vantagens: foco, feedback, design.

## Simplicidade e baby steps
- Implementação mais simples possível (problema do cálculo de salário); passos pequenos quando incerto; maiores quando confiante.

## TDD e design (a parte central do livro)
- **Os testes dão feedback de design**: teste difícil de escrever = classe com problema.
  - Muitos mocks/setup grande → **acoplamento alto**.
  - Teste que precisa de muitos cenários para um método → **baixa coesão**.
  - Necessidade de testar métodos privados → responsabilidade escondida (extraia classe).
  - Necessidade de olhar estado interno → **encapsulamento** fraco (Tell, Don't Ask).
- Favoreça composição; cuidado com herança (testes duplicados entre subclasses).
- Dependências explícitas e injetadas; interfaces nas fronteiras.

## Mocks e integração
- **Mock objects** para isolar dependências (DAO, serviços externos); verifique interações relevantes, não tudo.
- **Testes de integração** para DAOs/banco reais e infraestrutura.

## Qualidade dos testes
- Nomes que descrevem o comportamento; um conceito por teste; **Test Data Builders**; evitar testes frágeis e lentos.

## Uso
Ao sentir dor no teste, pergunte "o que o teste está me dizendo sobre o design?" antes de forçar com mocks.
