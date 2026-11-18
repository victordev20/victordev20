---
name: algoritmos-cormen
description: "Algoritmos — Teoria e Prática (Cormen, Leiserson, Rivest, Stein / CLRS): análise assintótica, recorrências, ordenação, estruturas de dados, programação dinâmica, algoritmos gulosos, grafos, fluxos, NP-completude. Use para projetar e analisar algoritmos, provar corretude/complexidade ou escolher estrutura de dados."
---

# Algoritmos: Teoria e Prática (CLRS)

Livro-fonte: `LivrosDev/Algoritmos - Teoria e Prática - Autor (Thomas Cormen).pdf`

## Fundamentos
- **Corretude via invariante de laço:** inicialização, manutenção, término.
- **Notação assintótica:** O (limite superior), Ω (inferior), Θ (justo), o, ω.
- **Recorrências:** substituição, árvore de recursão, **teorema mestre** para `T(n) = aT(n/b) + f(n)`.
- **Análise probabilística** e algoritmos aleatorizados (problema da contratação, aniversário, bolas e caixas).
- **Análise amortizada:** agregada, contábil, potencial.

## Catálogo por parte
- **Ordenação:** inserção Θ(n²), merge sort Θ(n lg n), heapsort, quicksort (esperado Θ(n lg n)), limite inferior Ω(n lg n) para comparação; counting/radix/bucket sort em tempo linear; estatísticas de ordem (seleção em tempo linear).
- **Estruturas de dados:** pilhas, filas, listas, **tabelas hash** (encadeamento, endereçamento aberto, hash universal), **árvores binárias de busca**, **rubro-negras**, aumento de estruturas (árvores de intervalo), B-trees, heaps de Fibonacci, van Emde Boas, conjuntos disjuntos (union-find com união por rank + compressão de caminho).
- **Técnicas de projeto:** **programação dinâmica** (subestrutura ótima + subproblemas sobrepostos: corte de hastes, cadeia de matrizes, LCS, BST ótima), **gulosos** (seleção de atividades, Huffman, matroides).
- **Grafos:** BFS, DFS (ordenação topológica, componentes fortemente conexas), **árvore geradora mínima** (Kruskal, Prim), **caminhos mínimos** (Bellman-Ford, DAG, Dijkstra, Floyd-Warshall, Johnson), **fluxo máximo** (Ford-Fulkerson, Edmonds-Karp, emparelhamento bipartido).
- **Tópicos:** multithread, matrizes, programação linear, FFT, teoria dos números (RSA), casamento de cadeias (KMP, Rabin-Karp), geometria computacional, **NP-completude** (reduções), algoritmos de aproximação.

## Como usar ao resolver um problema
1. Modele entrada/saída formalmente.
2. Reconheça a família (ordenação, grafo, DP, guloso, fluxo...).
3. Prove corretude (invariante ou escolha gulosa/subestrutura ótima).
4. Analise tempo e espaço; compare com limite inferior conhecido.
5. Se for NP-difícil, considere aproximação, heurística ou casos especiais.
