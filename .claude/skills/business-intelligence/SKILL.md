---
name: business-intelligence
description: "Business Intelligence — Implementar do jeito certo e a custo zero (Ronaldo Braghittoni, Casa do Código): arquitetura de BI, modelagem dimensional de Data Warehouse (fatos e dimensões), ETL com ferramentas livres (Pentaho), cargas incrementais e consumo via OLAP/planilhas/dashboards. Use ao modelar um DW, desenhar ETL ou montar um BI com ferramentas open source."
---

# Business Intelligence a Custo Zero — Ronaldo Braghittoni (Casa do Código)

Livro-fonte: `LivrosDev/Business Intelligence - Implementar do jeito certo e a custo zero - Autor (Casa do Código).pdf`

## Arquitetura
```
Fontes (ERP, CSV, planilhas) → Staging (Data Stage) → ETL → Data Warehouse → OLAP/Relatórios/Dashboards
```
Projeto de BI = pessoas + processo + tecnologia; comece com escopo pequeno e de alto valor.

## Modelagem dimensional (Kimball)
- **Fato:** evento mensurável no grão definido (ex.: item de venda) com métricas aditivas.
- **Dimensões:** contexto (Data, Cliente, Geografia, Funcionário, Produto), com **chaves substitutas (surrogate keys)**.
- **Esquema estrela**; defina o **grão** antes de tudo.
- **Dimensão Data** pré-carregada com atributos (dia da semana, mês, trimestre, feriado).
- Mudanças lentas (SCD tipo 1 sobrescreve, tipo 2 versiona com vigência).

## ETL (ex.: Pentaho Data Integration)
1. Extrair para staging (manipulação de arquivos).
2. Carregar dimensões primeiro (lookup/insert-update), depois fatos (lookup das surrogate keys).
3. Fato de Venda e Fato de Detalhe de Venda.
4. **Agendar** cargas diárias incrementais; logs e reprocessamento.
5. **Revisar e testar:** contagens e somas batendo com a origem.

## Consumo
- Cubos OLAP (Mondrian), add-ins de planilha, ferramentas de relatório e dashboards (Pentaho/Saiku/Metabase etc.).

## Checklist
- [ ] Grão do fato documentado
- [ ] Surrogate keys em todas as dimensões
- [ ] Tratamento de membros "desconhecido"
- [ ] Reconciliação de totais origem × DW
- [ ] Carga idempotente e agendada
