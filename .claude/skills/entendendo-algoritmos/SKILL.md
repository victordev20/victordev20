---
name: entendendo-algoritmos
description: "Entendendo Algoritmos — Um guia ilustrado (Aditya Y. Bhargava): pesquisa binária, Big O, ordenação por seleção, recursão e pilha de chamadas, dividir para conquistar e quicksort, tabelas hash, pesquisa em largura, Dijkstra, algoritmos gulosos e NP-completos, programação dinâmica, k-vizinhos mais próximos. Use para explicar algoritmos de forma visual e didática ou escolher a abordagem certa para um problema."
---

# Entendendo Algoritmos — Aditya Y. Bhargava

Livro-fonte: `LivrosDev/Entendendo Algoritmos - Um Guia Ilustrado Para Programadores e Outros Curiosos - Autor (Aditya Y. Bhargava).pdf`

## Capítulos e ideias-chave
1. **Pesquisa binária** em lista ordenada: O(log n) (128 itens → 7 passos). **Big O** = crescimento do número de operações no pior caso.
2. **Ordenação por seleção** O(n²); arrays (acesso O(1), inserção cara) vs listas encadeadas (inserção O(1), acesso O(n)).
3. **Recursão:** caso base + caso recursivo; **pilha de chamadas**.
4. **Dividir para conquistar** e **quicksort** (médio O(n log n), pior O(n²)); escolher pivô aleatório.
5. **Tabelas hash:** O(1) médio; usos (busca, evitar duplicatas, cache); colisões, fator de carga (< 0,7), boa função hash.
6. **Pesquisa em largura (BFS)** em grafos: caminho com menos arestas; usa fila; O(V + E). Ordenação topológica, árvores.
7. **Dijkstra:** caminho de menor peso em grafos com pesos **não negativos** (para negativos: Bellman-Ford).
8. **Algoritmos gulosos:** ótimo local a cada passo; aproximação para **problemas NP-completos** (cobertura de conjuntos, caixeiro-viajante). Sinais de NP-completo: "todas as combinações", sequências, conjuntos.
9. **Programação dinâmica:** problema da mochila, maior substring/subsequência comum; monte a tabela de subproblemas.
10. **K-vizinhos mais próximos (KNN):** classificação e regressão; extração de características; distância.
11. **Próximos passos:** árvores, índices invertidos, Fourier, MapReduce, filtros de Bloom, HyperLogLog, SHA, Diffie-Hellman, programação linear.

## Guia de escolha
| Problema | Abordagem |
|---|---|
| Buscar em dados ordenados | Pesquisa binária |
| Busca/contagem rápida por chave | Tabela hash |
| Menor número de passos | BFS |
| Menor custo com pesos ≥ 0 | Dijkstra |
| Subproblemas que se repetem | Programação dinâmica |
| Exato é inviável | Guloso/aproximação |
