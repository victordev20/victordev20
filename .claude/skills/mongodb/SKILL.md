---
name: mongodb
description: "MongoDB — Construa novas aplicações com novas tecnologias (Fernando Boaglio, Casa do Código): por que NoSQL, JSON, CRUD no shell, operadores de busca, índices, capped collections, schema design (1-N, N-N, tudo em uma collection, embutir vs referenciar), aggregation framework, MapReduce, replica sets, sharding, GridFS, drivers e integração com linguagens. Use ao modelar dados ou otimizar consultas no MongoDB."
---

# MongoDB — Fernando Boaglio (Casa do Código)

Livro-fonte: `LivrosDev/MongoDB - Construa Novas Aplicações com Novas Tecnologias - Autor (Casa do Código).pdf`

## Básico
- Banco → collections → documentos BSON (JSON). Exemplo guia: resultados da Mega-Sena.
- CRUD: `insertOne/insertMany`, `find(filtro, projeção)`, `updateOne/updateMany` com `$set`, `$inc`, `$push`, `$unset`; `deleteOne/deleteMany`; criar/remover collections; renomear campos (`$rename`).
- Operadores: `$gt/$lt/$in/$nin/$and/$or/$exists/$regex`, ordenação, `limit`, `skip`.
- **Índices** (simples, compostos, únicos, TTL, texto) e `explain()`.
- **Capped collections** (tamanho fixo, ótimas para logs).

## Schema design
- Projete pelos **padrões de acesso**.
- **1-N:** embutir se "N" é pequeno e lido junto; referenciar se é grande/ilimitado.
- **N-N:** arrays de referências em um ou ambos os lados.
- **Tudo em uma collection** quando os dados são sempre lidos juntos.
- Limite de 16 MB por documento; evite arrays que crescem sem fim.

## Avançado
- **Aggregation framework:** `$match`, `$group`, `$project`, `$sort`, `$lookup`, `$unwind`.
- MapReduce (legado).
- **Replica sets** (alta disponibilidade, eleição, read preference).
- **Sharding** (escala horizontal; escolha da shard key é crítica).
- **GridFS** para arquivos grandes; drivers (Java, Node, Python...), backup (`mongodump/mongorestore`).

## Checklist
- [ ] Toda consulta frequente tem índice adequado (verificado com `explain`)
- [ ] Nenhum array ilimitado embutido
- [ ] Write concern/read preference adequados
- [ ] Shard key com alta cardinalidade e boa distribuição
