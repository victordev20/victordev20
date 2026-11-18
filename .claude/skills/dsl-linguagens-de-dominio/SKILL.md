---
name: dsl-linguagens-de-dominio
description: "DSL — Quebre a barreira entre desenvolvimento e negócios (Leonardo Otero, Casa do Código): modelo de domínio vs modelo semântico, DSLs internas e externas, encadeamento de métodos, interfaces fluentes/progressivas, Composite, sequência de funções, funções aninhadas, closures, BNF e quando usar uma DSL (exemplos em Java e Scala). Use ao projetar APIs fluentes ou linguagens específicas de domínio."
---

# DSL — Linguagens Específicas de Domínio (Casa do Código)

Livro-fonte: `LivrosDev/DSL - Quebre a barreira entre desenvolvimento e negócios - Autor (Casa do Código).pdf`

## Conceitos
- **Modelo de domínio** representa o negócio; **modelo semântico** é o que a DSL popula; a DSL é uma camada fina sobre ele.
- **DSL interna** (dentro de uma linguagem hospedeira — Java, Scala) vs **externa** (gramática própria, parser).
- **Devo usar uma DSL?** Quando especialistas de negócio precisam ler/validar regras, quando há muitas configurações repetitivas ou quando a legibilidade do código de alto nível é crítica. Evite se o custo de manutenção for maior que o ganho.

## Técnicas para DSLs internas
1. **Encadeamento de métodos** (method chaining) → interfaces fluentes (`partida().entre("A").e("B").placar(2,1)`).
2. **Interfaces progressivas:** cada método retorna um tipo que só expõe os próximos passos válidos (guia o usuário e o compilador).
3. **Composite** para estruturas hierárquicas.
4. **Sequência de funções** e **funções aninhadas** (`regra(quando(...), entao(...))`).
5. Closures/lambdas, literais de coleção, sobrecarga de operadores (Scala), parâmetros nomeados.
6. Exemplo: Game of Life e Copa do Mundo dos programadores.

## DSLs externas
- Gramática em **BNF**/EBNF; parser (ANTLR ou similar); geração do modelo semântico.

## Diretrizes
- Projete primeiro o modelo semântico e teste-o sem a DSL.
- A DSL deve ler como uma frase do domínio; nomes vêm da linguagem ubíqua.
- Mantenha mensagens de erro compreensíveis para o usuário da DSL.
