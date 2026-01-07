>[!tips] Theorem 6.2 BFS Properties
>In a BFS-tree $T$:
>(a) $\ell(v) = d_T(r, v)$ is the level of $v$.
>(b) Every edge of $G$ joins vertices on the same or consecutive levels ($|\ell(u) - \ell(v)| \le 1$).

>[!tips] Theorem 6.3 BFS Correctness
>Values returned by BFS are true distances: $\ell(v) = d_G(r, v)$.

>[!tips] Theorem 6.6 DFS Properties
>In a DFS-tree $T$, every edge of $G$ joins vertices which are related in $T$ (one is an ancestor of the other). Nontree edges are called back edges.

>[!tips] Theorem 6.7 Cut Vertices via DFS
>The root of a DFS-tree is a cut vertex iff it has at least two children. Any other vertex $v$ is a cut vertex iff it has a child with no back edge to a proper ancestor of $v$.