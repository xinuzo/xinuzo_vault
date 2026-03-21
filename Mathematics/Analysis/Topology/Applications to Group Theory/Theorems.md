# Theorems.md

> [!theorem] Lemma 83.1
> Every connected graph contains a maximal tree.

> [!theorem] Theorem 83.2
> Let $X$ be a graph, and let $T$ be a subgraph that is a tree. Then $T$ is a maximal tree if and only if $T$ contains all the vertices of $X$.

> [!theorem] Theorem 84.1 (The Fundamental Group of a Graph)
> Let $X$ be a connected graph, and let $T$ be a maximal tree in $X$. Then the fundamental group $\pi_1(X, x_0)$ is a free group. Furthermore, there is a bijective correspondence between a set of free generators for $\pi_1(X, x_0)$ and the set of edges of $X$ that are not contained in the maximal tree $T$.

> [!theorem] Theorem 84.2
> Any covering space of a graph is itself a graph.

> [!theorem] Theorem 85.1 (The Nielsen-Schreier Theorem)
> Every subgroup of a free group is itself a free group.
> *(Proof Strategy: Represent the free group as the fundamental group of a wedge of circles (a graph). By the classification of covering spaces, the subgroup corresponds to a covering space. By Theorem 84.2, the covering space is a graph. By Theorem 84.1, the fundamental group of any graph is free. Therefore, the subgroup is free!)*

> [!theorem] Theorem 85.2 (Schreier's Index Formula)
> Let $F$ be a free group of finite rank $n$. Let $H$ be a subgroup of $F$ having finite index $k$. Then $H$ is a free group of finite rank $m$, and the ranks are related by the formula:
> $$m = k(n - 1) + 1$$