---
name: nosql
description: "NoSQL — Como armazenar os dados de uma aplicação moderna (David Paniz, Casa do Código): limitações do relacional, tipos de NoSQL (documento, chave-valor, colunar, grafo), MongoDB (CRUD, relacionamentos, N+1, documentos embutidos, desnormalização), teorema CAP, Riak (chave/valor), Cassandra (colunar), Neo4j (grafo) e persistência poliglota. Use para escolher o tipo de banco certo para cada problema ou modelar dados NoSQL."
---

# NoSQL — David Paniz (Casa do Código)

Livro-fonte: `LivrosDev/NoSQL - Como armazenar os dados de uma aplicação moderna - Autor (Casa do Código).pdf`

## Por que NoSQL
- Problemas do relacional em certos cenários: impedância objeto-relacional, esquema rígido, escala horizontal difícil.
- **Tipos:** documento (MongoDB), chave-valor (Riak, Redis), colunar/wide-column (Cassandra, HBase), grafo (Neo4j).

## Documentos (MongoDB)
- CRUD de documentos; relacionamentos por referência; **problema N+1** ao listar (ex.: álbuns e músicas); **documentos embutidos**; **desnormalização** consciente (duplicar para ler rápido, aceitar custo na escrita).

## Consistência × disponibilidade
- **Teorema CAP:** em partição de rede, escolha entre consistência e disponibilidade.
- Consistência eventual, quorum (N, R, W), vector clocks/resolução de conflitos.

## Outros modelos
- **Riak (chave/valor):** buckets, objetos, alta disponibilidade, consultas limitadas (busca por chave).
- **Cassandra (colunar):** keyspaces, column families/tabelas, modelagem por consulta, escrita muito rápida, escala linear.
- **Neo4j (grafo):** nós, relacionamentos, propriedades; Cypher; ideal para recomendações e redes.

## Persistência poliglota
Use o banco adequado a cada necessidade dentro do mesmo sistema.

## Guia de escolha
| Necessidade | Tipo |
|---|---|
| Agregados lidos inteiros, esquema flexível | Documento |
| Cache/sessão, acesso por chave | Chave-valor |
| Escrita massiva, séries temporais, multi-DC | Colunar |
| Relações profundas/caminhos | Grafo |
| Transações complexas e consultas ad hoc | Relacional |
