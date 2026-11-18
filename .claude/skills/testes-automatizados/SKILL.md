---
name: testes-automatizados
description: "Testes Automatizados de Software — Um guia prático (Mauricio Aniche, Casa do Código): testes de unidade com JUnit, convenções, classes de equivalência e casos especiais, Test Data Builders, @Before/@After, testando exceções, legibilidade com matchers (Hamcrest), cobertura, TDD, mock objects (Mockito), testes de integração com banco (DAO), testes de sistema com Selenium (Page Objects) e testes de serviços. Use ao escrever ou revisar testes automatizados."
---

# Testes Automatizados de Software — Mauricio Aniche

Livro-fonte: `LivrosDev/Testes Automatizados de Software - Um Guia Prático - Autor (Casa do Código).pdf`

## Testes de unidade
- Exemplo do leilão (maior/menor lance): implementar, quebrar, testar.
- **JUnit**: `@Test`, `assertEquals(esperado, calculado, delta)`, import estático.
- **Convenções:** nomes descritivos (`deveEntenderLancesEmOrdemDecrescente`), cenário/ação/validação.
- **Classes de equivalência** e **casos especiais** (vazio, um elemento, limites, ordem aleatória).
- **Test Data Builders** para criar cenários legíveis.
- `@Before`/`@After`/`@BeforeClass`/`@AfterClass` para setup.
- **Acoplamento entre teste e produção**: teste o comportamento, não a implementação.
- **Testar exceções** (`expected`, `assertThrows`).
- **Legibilidade** com matchers (Hamcrest/AssertJ).
- **100% de cobertura?** Cobertura é indicador, não meta; foque em cenários relevantes.

## TDD
Escreva o teste antes; feedback sobre o design; passos pequenos.

## Mocks
- **Mockito:** `mock()`, `when().thenReturn()`, `verify()`, `times()`, `never()`, captura de argumentos, simular exceções.
- Use para isolar infraestrutura (DAO, e-mail, serviços externos).

## Integração e sistema
- **DAOs** testados contra banco real (H2/container), com transação revertida ou dados limpos.
- **Selenium WebDriver** para testes de sistema; **Page Objects** para isolar a UI; dados preparados via API/banco.

## Checklist de um bom teste
- [ ] Nome descreve o comportamento
- [ ] Um motivo para falhar
- [ ] Independente da ordem de execução
- [ ] Sem lógica (if/loops) no teste
- [ ] Rápido (unidade) ou isolado em suíte própria (integração/sistema)
