---
name: css-eficiente
description: "CSS Eficiente (Tárcio Zemel, Casa do Código): especificidade, interpretação de seletores, evitar IDs, OOCSS, SMACSS (base, layout, módulo, estado, tema), BEM, pré-processadores e organização/performance de estilos. Use ao arquitetar ou revisar CSS, nomear classes ou reduzir conflitos de especificidade."
---

# CSS Eficiente — Tárcio Zemel (Casa do Código)

Livro-fonte: `LivrosDev/CSS Eficiente - Técnicas e ferramentas que fazem a diferença nos seus estilos - Autor (Casa do Código).pdf`

## Seletores
- **Especificidade** (inline > ID > classe/atributo/pseudo-classe > elemento). Guerra de especificidade gera `!important` em cascata.
- Navegadores leem seletores **da direita para a esquerda** → o seletor-chave (mais à direita) deve ser específico; evite descendentes profundos.
- **Não use IDs como seletores CSS:** específicos demais, não reutilizáveis.

## OOCSS
- Separe **estrutura de aparência** (skin).
- Separe **contêiner de conteúdo** (um objeto se parece igual onde quer que esteja).
- Exemplos: media object, botões, caixas.

## SMACSS
- Categorias: **Base** (elementos), **Layout** (`l-`), **Módulo** (componentes reutilizáveis), **Estado** (`is-active`, `is-hidden`), **Tema**.
- Nomenclatura por prefixos; módulos com subclasses para variações.

## BEM
- `bloco__elemento--modificador` (ex.: `card__title--highlighted`).
- Especificidade plana (uma classe), independência de contexto.

## Pré-processadores
- Aninhamento (com moderação — máx. 3 níveis), variáveis, mixins, extend, imports, funções.
- Cuidado: aninhamento excessivo gera seletores longos e específicos.

## Outras boas práticas
- Organize arquivos por camada/componente; um guia de estilo vivo.
- Minifique, concatene e remova CSS morto; prefira classes utilitárias pequenas a regras duplicadas.

## Checklist de revisão
- [ ] Nenhum seletor por ID
- [ ] Seletores com no máximo 2–3 níveis
- [ ] Nomes seguem uma convenção (BEM ou SMACSS)
- [ ] Estados expressos por classes de estado
- [ ] Sem `!important` fora de utilitários
