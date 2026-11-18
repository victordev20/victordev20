---
name: estatistica-wheelan
description: "Estatística — O que é, para que serve, como funciona (Charles Wheelan, 'Naked Statistics'): estatística descritiva, descrição enganosa, correlação, probabilidade e seus problemas, importância dos dados, teorema do limite central, inferência e testes de hipótese, pesquisas, regressão e seus erros comuns, avaliação de programas. Use para interpretar dados, desenhar experimentos/testes A/B ou explicar conceitos estatísticos de forma intuitiva."
---

# Estatística: O que é, para que serve, como funciona — Charles Wheelan

Livro-fonte: `LivrosDev/Estatistica - O que e, para que serve, como funciona .pdf`

## Capítulos
1. **Qual é o objetivo?** Resumir, inferir e avaliar — estatística é ferramenta para responder perguntas.
2. **Estatística descritiva:** média, mediana, percentis, desvio-padrão, distribuição normal.
3. **Descrição enganosa:** média vs mediana, nominal vs real (inflação), percentuais e pontos percentuais.
4. **Correlação:** coeficiente de -1 a 1; **não implica causalidade**.
5. **Probabilidade básica:** valor esperado, eventos independentes, lei dos grandes números.
6. **Problemas com probabilidade:** supor independência, eventos agrupados, falácia do apostador, regressão à média, viés de sobrevivência, discriminação estatística.
7. **A importância dos dados:** amostras aleatórias; vieses (seleção, publicação, memória, sobrevivência, usuário saudável). "Entra lixo, sai lixo".
8. **Teorema do limite central:** médias amostrais seguem distribuição normal → base da inferência. Erro padrão = σ/√n.
9. **Inferência:** hipótese nula, p-valor, nível de significância, erros Tipo I (falso positivo) e Tipo II (falso negativo).
10. **Pesquisas:** margem de erro, amostragem, viés de resposta e formulação das perguntas.
11. **Regressão:** reta de mínimos quadrados, coeficientes, R², variáveis de controle, regressão múltipla.
12. **Erros comuns de regressão:** relações não lineares, causalidade invertida, viés de variável omitida, variáveis altamente correlacionadas, extrapolação, mineração de dados (muitas variáveis → significâncias falsas).
13. **Avaliação de programas:** experimentos controlados randomizados, experimentos naturais, diferenças em diferenças, descontinuidade, grupo de controle.

## Checklist para analisar um resultado
- [ ] A amostra representa a população?
- [ ] Há grupo de controle/contrafactual?
- [ ] A diferença é estatisticamente e praticamente significativa?
- [ ] Testamos muitas hipóteses (risco de falso positivo)?
- [ ] Pode haver variável omitida ou causalidade reversa?
