---
name: agile-estimating-and-planning
description: "Agile Estimating and Planning (Mike Cohn): story points vs dias ideais, planning poker, velocidade, priorização por valor/risco/custo, planejamento de release e iteração, buffers, monitoramento e comunicação do plano. Use ao estimar backlog, prever datas de release ou explicar incerteza em planos ágeis."
---

# Agile Estimating and Planning — Mike Cohn

Livro-fonte: `LivrosDev/Agile Estimating and Planning - Autor (Mike Cohn).pdf`

## Por que planejar e por que planos falham
- Planejar serve para **reduzir risco e incerteza, apoiar decisões e comunicar**.
- Planos falham porque focam em atividades (não em funcionalidades), atrasos se propagam, multitarefa atrasa tudo, funcionalidades não são priorizadas, incerteza é ignorada e **estimativas viram compromissos**.
- O **cone da incerteza**: no início, uma estimativa varia de 0,25x a 4x.

## Estimando tamanho
- **Story points** (tamanho relativo) ou **dias ideais**; estime tamanho e derive duração pela **velocidade**.
- **Planning poker**: estimativa em grupo, sequência ~Fibonacci (1, 2, 3, 5, 8, 13, 20, 40, 100), discussão das divergências.
- Triangule estimativas; re-estime só quando o tamanho relativo mudou.

## Planejando por valor
- Priorize por: **valor financeiro**, **custo**, **conhecimento/risco reduzido**, **custo de esperar**.
- Ferramentas: análise financeira (NPV, IRR, payback), **Kano** (obrigatório, linear, encantador), priorização relativa de desejabilidade.
- Divida histórias grandes por fluxo de dados, operações (CRUD), casos de borda, requisitos não funcionais.

## Agendamento
- **Release:** defina condições de satisfação, estime, escolha duração de iteração, estime velocidade (histórico, rodar uma iteração ou previsão), selecione histórias, adicione **buffers** (de funcionalidade e de cronograma) para projetos com prazo crítico.
- **Iteração:** quebre histórias em tarefas, estime em horas, comprometa-se pela capacidade.
- Vários times: estabeleça base comum de pontos, lookahead planning, buffer de integração.

## Monitorar e comunicar
- **Burndown** de release e de iteração; gráficos de barras de release (scope change visível).
- Comunique intervalos ("entre 6 e 8 iterações"), não datas pontuais com falsa precisão.

## Checklist
- [ ] Estimei tamanho, não tempo?
- [ ] A velocidade usada vem de dados reais?
- [ ] O plano comunica faixa de incerteza?
- [ ] O backlog está priorizado por valor e risco?
