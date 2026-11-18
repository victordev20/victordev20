---
name: expressoes-regulares
description: "Expressões Regulares — Uma abordagem divertida (Aurelio Marinho Jargas): metacaracteres representantes (. [] [^]), quantificadores (? * + {n,m}), âncoras (^ $ \\b), escape, alternância, grupos e retrovisores, gulosos vs não gulosos, classes POSIX, diferenças entre linguagens e ferramentas (grep, sed, editores) e receitas. Use ao escrever, explicar ou depurar regex."
---

# Expressões Regulares — Aurelio Marinho Jargas

Livro-fonte: `LivrosDev/Expressões Regulares - uma abordagem divertida - Autor (Aurelio Marinho).pdf`

## Metacaracteres (com os apelidos do livro)
| Tipo | Meta | Apelido | Significado |
|---|---|---|---|
| Representante | `.` | o necessitado | qualquer caractere |
| | `[...]` | a exigente | lista de permitidos |
| | `[^...]` | a experiente | lista negada |
| Quantificador | `?` | o opcional | 0 ou 1 |
| | `*` | o tanto-faz | 0 ou mais |
| | `+` | o tem-que-ter | 1 ou mais |
| | `{n,m}` | o controle | de n a m |
| Âncora | `^` | o início | começo da linha |
| | `$` | o fim | fim da linha |
| | `\b` | a limítrofe | borda de palavra |
| Outros | `\` | a criptonita | escape |
| | `|` | o alternativo | ou |
| | `(...)` | o pop | grupo |
| | `\1…\9` | o saudosista | retrovisor (backreference) |

## Mais conceitos
- **Gulosos** (`.*`) vs **não gulosos** (`.*?`) — quantificadores pegam o máximo possível por padrão.
- Classes POSIX (`[[:digit:]]`, `[[:alpha:]]`, `[[:space:]]`), atalhos `\d \w \s`, grupos não capturantes `(?:)`, lookahead/lookbehind (quando suportados).
- Básicas (BRE) vs estendidas (ERE) vs PCRE; diferenças entre grep, egrep, sed, awk, Vim, Python, JavaScript, PHP etc.

## Dicas do livro
- Seja específico: prefira `[^"]*` a `.*` entre delimitadores.
- Ancore quando possível (`^...$`) para evitar casamentos parciais.
- Escape metacaracteres literais (`\.`).
- Teste com casos que **devem** e que **não devem** casar.
- Não use regex para tudo (HTML aninhado, por exemplo).

## Receitas
- Data dd/mm/aaaa: `^[0-3][0-9]/[01][0-9]/[0-9]{4}$`
- Linha em branco: `^[[:space:]]*$`
- Palavra repetida: `\b(\w+)\s+\1\b`
- Número com sinal e decimal: `^[+-]?[0-9]+([.,][0-9]+)?$`
