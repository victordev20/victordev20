---
name: fragmentos-de-um-programador
description: "Fragmentos de um programador — Artigos e insights da carreira de um profissional (Phil Calçado, Casa do Código): guia para freelancers, design by contract (invariantes, pré e pós-condições), evitar VOs/BOs e modelo anêmico, MVC e camadas, fantoches (objetos sem comportamento), DDD e outros ensaios sobre arquitetura e carreira. Use ao discutir design OO, contratos ou modelagem rica de domínio."
---

# Fragmentos de um Programador — Phil Calçado (Casa do Código)

Livro-fonte: `LivrosDev/Fragmentos de um programador - Artigos e insights da carreira de um profissional - Autor (Casa do Código).pdf`

## Ensaios principais
1. **Guia de guerra para freelancers:** organize o ambiente, metodologia de trabalho, seja compromissado, conheça o cliente, seja ágil (entregas pequenas), tenha um advogado, cuidado com contratos abertos.
2. **Contratos nulos (Design by Contract):** **invariantes** de classe, **pré-condições** (dever do cliente) e **pós-condições** (dever do fornecedor); subclasses não podem fortalecer pré-condições nem enfraquecer pós-condições (LSP); trate contratos quebrados com falha rápida; documente os contratos.
3. **Evitando VOs e BOs:** a separação "Value Object com getters/setters + Business Object com lógica" vem de limitações antigas (EJB); gera **modelo de objetos anêmico**. Use objetos com dados **e** comportamento; Transfer Objects só nas fronteiras.
4. **MVC e camadas:** camadas tratam de **separação entre componentes**; MVC trata da **interação** entre eles — conceitos diferentes e complementares.
5. **Fantoches:** objetos que só são manipulados por outros (sem comportamento) — sinal de design procedural disfarçado; "Tell, don't ask".
6. Outros: DDD na prática, arquitetura, linguagens, carreira e ensino.

## Como aplicar em revisões de design
- [ ] As classes de domínio têm comportamento ou só getters/setters?
- [ ] Regras de negócio estão em "services" procedurais que manipulam fantoches?
- [ ] Pré e pós-condições estão explícitas (validação, asserções, testes)?
- [ ] DTOs aparecem só nas bordas (API, persistência)?
