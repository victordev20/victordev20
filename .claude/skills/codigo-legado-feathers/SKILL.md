---
name: codigo-legado-feathers
description: "Trabalho Eficaz com Código Legado (Michael C. Feathers): código legado = código sem testes; algoritmo de alteração (identificar pontos de mudança, encontrar pontos de teste, quebrar dependências, escrever testes, alterar e refatorar), seams (costuras), testes de caracterização, sprout/wrap method e class, efeitos e esboços de efeito, e o catálogo de técnicas de quebra de dependências. Use ao alterar código sem testes ou colocar código legado sob teste com segurança."
---

# Trabalho Eficaz com Código Legado — Michael C. Feathers

Livro-fonte: `LivrosDev/Trabalho Eficaz com Código Legado - Autor (Michael C. Feathers).pdf`

## Definição
**Código legado é código sem testes.** Sem testes, não sabemos se a mudança melhorou ou piorou.

## Algoritmo de alteração de código legado
1. Identifique os **pontos de alteração**.
2. Encontre os **pontos de teste** (esboços de efeito, pontos de interceptação, pinch points).
3. **Quebre dependências** (o dilema: para refatorar precisa de testes; para testar precisa refatorar → mudanças mínimas e seguras).
4. Escreva **testes** (de **caracterização**: documentam o comportamento atual, não o desejado).
5. Faça as alterações e **refatore**.

## Seams (costuras)
Lugar onde você altera o comportamento sem editar o código naquele lugar: **seam de objeto** (polimorfismo/injeção), **seam de link** (classpath/linker), **seam de pré-processamento**. Todo seam tem um **ponto de habilitação**.

## Técnicas para adicionar funcionalidade com segurança
- **Sprout Method / Sprout Class:** escreva o código novo em método/classe nova testada e chame-o do legado.
- **Wrap Method / Wrap Class:** envolva o método existente (decorator) para adicionar comportamento antes/depois.
- TDD para o código novo; "programação por diferença" com herança temporária.

## Problemas comuns (capítulos "Não consigo…")
Não consigo colocar a classe no teste (construtor pesado, dependências ocultas, globais/singletons) · não consigo rodar o método no teste (privado, efeitos colaterais) · preciso de muito tempo · não entendo o código (esboços, listagens marcadas, refatoração rascunho, apagar código não usado) · minha aplicação não tem estrutura · classe gigante (identificar responsabilidades) · mesmo código em todo lugar · método monstro.

## Catálogo de quebra de dependências (seleção)
Adapt Parameter · Break Out Method Object · Encapsulate Global References · Expose Static Method · **Extract and Override Call/Factory Method/Getter** · **Extract Interface** · Extract Implementer · Introduce Instance Delegator · Introduce Static Setter · Link Substitution · **Parameterize Constructor/Method** · Primitivize Parameter · Pull Up Feature · Push Down Dependency · Replace Function with Function Pointer · Replace Global Reference with Getter · **Subclass and Override Method** · Supersede Instance Variable · Template Redefinition · Text Redefinition.

## Regras de segurança
- Preserve assinaturas ao quebrar dependências; apoie-se no compilador ("lean on the compiler").
- Mudanças sem testes devem ser mínimas e mecânicas; uma de cada vez.
