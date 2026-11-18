---
name: codigo-limpo
description: "Código Limpo (Robert C. Martin): nomes significativos, funções pequenas, comentários, formatação, objetos vs estruturas de dados, tratamento de erros, limites, testes unitários (F.I.R.S.T.), classes coesas, sistemas, emergência, concorrência, refinamento sucessivo e catálogo de 'cheiros' e heurísticas. Use ao escrever, revisar ou refatorar código para legibilidade e manutenção."
---

# Código Limpo — Robert C. Martin

Livro-fonte: `LivrosDev/Código limpo - Habilidades práticas do Agile Software - Autor (Robert C. Martin).pdf`

## Regras por tema
- **Nomes:** revelam intenção, evitam desinformação, distinções significativas, pronunciáveis e buscáveis; classes = substantivos, métodos = verbos; uma palavra por conceito.
- **Funções:** pequenas, **fazem uma coisa**, um nível de abstração (regra decrescente), poucos parâmetros (ideal 0–2), sem argumentos booleanos (flag), sem efeitos colaterais, **separação comando-consulta**, exceções em vez de códigos de erro, DRY.
- **Comentários:** não compensam código ruim; explique-se no código. Bons: legais, informativos, intenção, alerta, TODO. Ruins: redundantes, enganosos, obrigatórios, código comentado.
- **Formatação:** metáfora do jornal; conceitos relacionados próximos; consistência do time.
- **Objetos e estruturas:** objetos escondem dados e expõem comportamento; **Lei de Demeter** (evite `a.getB().getC().do()`).
- **Erros:** exceções não verificadas, contexto na exceção, não retorne nem passe `null` (Special Case/Null Object).
- **Limites:** encapsule APIs de terceiros; **learning tests**.
- **Testes:** três leis do TDD; um conceito por teste; **F.I.R.S.T.** (Fast, Independent, Repeatable, Self-validating, Timely); testes limpos são tão importantes quanto o código.
- **Classes:** pequenas, **SRP**, alta coesão, organizadas para mudança (OCP/DIP).
- **Sistemas:** separe construção de uso (DI), aspectos transversais, decisões adiadas.
- **Emergência (4 regras do design simples de Kent Beck):** roda todos os testes; sem duplicação; expressa intenção; mínimo de classes e métodos.
- **Concorrência:** separe código concorrente, limite escopo de dados compartilhados, cópias, threads independentes.

## Heurísticas (cap. 17) mais úteis
C (comentários): obsoletos, redundantes, código comentado. F (funções): muitos argumentos, flags, funções mortas. G (geral): duplicação, nível de abstração errado, feature envy, condicionais negativas, números mágicos, encapsular condicionais, funções que fazem mais de uma coisa. N (nomes): descritivos, no nível de abstração certo. T (testes): insuficientes, ignorados, lentos.

## Regra do escoteiro
Deixe o código mais limpo do que encontrou.

## Checklist de revisão
- [ ] Cada função cabe na tela e faz uma coisa
- [ ] Nomes dispensam comentários
- [ ] Sem duplicação e sem números mágicos
- [ ] Erros tratados com exceções, sem `null` circulando
- [ ] Testes legíveis e rápidos cobrindo o comportamento
