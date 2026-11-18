---
name: metricas-ageis
description: "Métricas ágeis — Obtenha melhores resultados em sua equipe (Raphael Albino, Casa do Código): entendimento do fluxo, WIP e seus benefícios, lead time vs cycle time, eficiência de fluxo, throughput, diagrama de fluxo cumulativo (CFD), gráficos de controle, histogramas, previsões probabilísticas (Monte Carlo), burn-up/burn-down e métricas de qualidade. Use ao instrumentar, analisar ou prever entregas de um time ágil."
---

# Métricas Ágeis — Raphael Albino (Casa do Código)

Livro-fonte: `LivrosDev/Métricas ágeis - Obtenha melhores resultados em sua equipe - Autor (Casa do Código).pdf`

## Base
- Entenda a solução, o **fluxo de desenvolvimento** do time (etapas, filas) e as práticas de engenharia antes de medir.
- Crie seu processo de forma evolutiva.

## Métricas e como usá-las
- **WIP (Work In Progress):** limitar reduz troca de contexto, expõe gargalos e reduz lead time (Lei de Little: `Lead time = WIP / Throughput`).
- **Lead time:** do pedido à entrega; **cycle time:** do início do trabalho à entrega. Meça por tipo de item; analise percentis (50%, 85%, 95%), não médias.
- **Eficiência do fluxo:** tempo trabalhando ÷ lead time (quase sempre muito baixa → filas são o problema).
- **Throughput:** itens entregues por período; base para previsões.
- **CFD (Cumulative Flow Diagram):** faixas por etapa; alargamento = acúmulo/gargalo.
- **Gráfico de controle e histograma** de lead time: variabilidade e outliers.
- **Previsão probabilística:** simulação de Monte Carlo a partir do throughput histórico ("85% de chance de entregar 30 itens até dd/mm").
- **Burn-up / burn-down** e mudança de escopo.
- **Qualidade:** bugs escapados, retrabalho, tempo de correção.

## Dicas
- Métrica é para o time aprender, não para punir; evite metas sobre métricas (Lei de Goodhart).
- Visualize no quadro; discuta tendências nas retrospectivas.
- Comece com 2–3 métricas simples.

## Checklist
- [ ] Datas de início e fim registradas para cada item
- [ ] Limites de WIP explícitos por coluna
- [ ] Previsões comunicadas com probabilidade
- [ ] Outliers investigados nas retros
