---
name: data-science-r
description: "Introdução a Data Science — Algoritmos de machine learning e métodos de análise (Casa do Código): processo de data science, linguagem R, estatística e álgebra linear básicas, pré-processamento, modelos de classificação (KNN, árvores, Naive Bayes, SVM), regressão, associação (Apriori) e agrupamento (k-means). Use para conduzir uma análise de dados/ML em R do problema à apresentação."
---

# Introdução a Data Science — Casa do Código

Livro-fonte: `LivrosDev/Introdução a data science - Algoritmos de machine learning e métodos de análise - Autor (Casa do Código).pdf`

## Processo
1. Problema, necessidade ou ideia.
2. Coleta e análise exploratória dos dados.
3. **Pré-processamento.**
4. Modelagem e inferência.
5. Pós-processamento (avaliação, interpretação).
6. Apresentação de resultados.
Dados → informação → conhecimento.

## R básico
- Vetores (`c()`), data frames, fatores, listas, `summary()`, `str()`, `table()`, gráficos básicos; pacotes (`install.packages`, `library`).

## Fundamentos
- Estatística descritiva (média, mediana, variância, desvio, correlação) e álgebra linear (vetores, matrizes, distâncias).

## Pré-processamento
- Limpeza (valores ausentes, outliers, duplicatas), integração, **normalização** (min-max, z-score), discretização, seleção de atributos, balanceamento de classes, divisão treino/teste.

## Modelos
- **Classificação:** KNN (tipo de distância, valor de k), árvores de decisão, Naive Bayes, SVM; avaliação com matriz de confusão, acurácia, precisão, recall, F1, validação cruzada.
- **Regressão:** linear simples e múltipla; métricas (RMSE, MAE, R²).
- **Associação:** Apriori (suporte, confiança, lift).
- **Agrupamento:** k-means (escolha de k, método do cotovelo), hierárquico.

## Checklist
- [ ] Pergunta de negócio clara
- [ ] Dados de teste nunca usados no treino/normalização
- [ ] Métrica alinhada ao custo dos erros
- [ ] Baseline simples para comparação
- [ ] Resultados comunicados em linguagem do negócio
