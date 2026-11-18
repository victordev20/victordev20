---
name: typescript-pratico
description: "Guia prático de TypeScript — Melhore suas aplicações JavaScript (Thiago da Silva Adriano, Casa do Código): instalação e compilador (tsc, tsconfig), var/let/const, tipos básicos (boolean, number, string, array, ReadonlyArray, tuple, enum, any, unknown, void, never), funções, interfaces, classes, modificadores de acesso, generics, módulos, namespaces, decorators e uso com frameworks. Use ao escrever ou revisar código TypeScript ou migrar JS para TS."
---

# Guia Prático de TypeScript — Casa do Código

Livro-fonte: `LivrosDev/Guia prático de TypeScript - Melhore suas aplicações JavaScript - Autor (Casa do Código).pdf`

## Ambiente
- `npm i -g typescript`, `tsc arquivo.ts`, `tsc --init` → `tsconfig.json` (`target`, `module`, `strict`, `outDir`, `sourceMap`), modo watch.

## Tipos
- `let`/`const` (evite `var`).
- `boolean`, `number`, `string` (template strings), `T[]`/`Array<T>`, **`ReadonlyArray<T>`** (bloqueia push/pop/atribuição), **tuplas** `[string, number]`, **enum** (numérico e string), `any` (evite), `unknown` (seguro), `void`, `null`/`undefined`, `never`, type assertions.
- **Union** `A | B`, **intersection** `A & B`, **type aliases**, literal types, type guards (`typeof`, `instanceof`, `in`).

## Estruturas
- **Funções:** parâmetros opcionais/padrão/rest, tipos de retorno, overloads, arrow functions.
- **Interfaces:** propriedades opcionais e `readonly`, index signatures, extensão, implementação por classes.
- **Classes:** `public`/`private`/`protected`, `readonly`, parameter properties, getters/setters, `static`, classes abstratas, herança.
- **Generics:** funções, interfaces e classes genéricas, restrições `<T extends ...>`.
- **Módulos** (import/export), namespaces, **decorators** (Angular etc.).

## Boas práticas
- Ative `"strict": true`.
- Prefira `unknown` a `any`; tipar fronteiras (APIs, entrada do usuário).
- Interfaces/types para formas de dados; enums de string ou union de literais.
- Deixe a inferência trabalhar dentro de funções; anote assinaturas públicas.
