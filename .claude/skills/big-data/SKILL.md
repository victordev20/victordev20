---
name: big-data
description: "Big Data — Técnicas e tecnologias para extração de valor dos dados (Rosangela Marquesone, Casa do Código): Vs do Big Data, captura e armazenamento (NoSQL, governança), processamento (Hadoop/MapReduce, tempo real, nuvem), análise (preparação, modelagem, validação) e visualização. Use ao planejar pipelines de dados em larga escala ou explicar o ecossistema Big Data."
---

# Big Data — Rosangela Marquesone (Casa do Código)

Livro-fonte: `LivrosDev/Big Data - Técnicas e tecnologias para extração de valor dos dados - Autor (Casa do Código).pdf`

## Conceitos
- **Vs:** Volume, Velocidade, Variedade, Veracidade, Valor (e outros como Variabilidade, Visualização).
- Dados gerados por humanos (redes sociais, textos) e por máquinas (sensores, logs, IoT).
- **Mitos:** Big Data não é só volume, não substitui BI, não é só Hadoop, não dispensa pessoas.

## Ciclo de valor
1. **Captura e armazenamento** — APIs, crawlers, logs, streams; **NoSQL** (chave-valor, documento, colunar, grafo); **governança** (qualidade, segurança, privacidade, metadados). Prática: armazenar tweets no MongoDB.
2. **Processamento** — desafio de escalabilidade (escalar horizontalmente); **Hadoop** (HDFS + MapReduce + YARN) e ecossistema (Hive, Pig, HBase, Sqoop, Flume); **tempo real** (Storm, Spark Streaming); nuvem (EMR etc.). Prática: contagem de hashtags com MapReduce.
3. **Análise** — processo: entender problema → preparar dados (limpeza, transformação, integração) → construir modelo (classificação, regressão, agrupamento, associação) → validar → implantar. Tecnologias: R, Python, Mahout, Spark MLlib.
4. **Visualização** — escolha do gráfico pelo objetivo, dashboards, storytelling.

## Como aplicar
- Comece pela **pergunta de negócio**, não pela ferramenta.
- Defina governança e privacidade antes de coletar.
- Escolha batch vs streaming pela latência necessária.
- Valide modelos com dados não vistos e acompanhe-os em produção.
