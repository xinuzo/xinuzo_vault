>[!tips] 18.1 Hamiltonian Graph
>A graph containing a Hamilton cycle (a cycle passing through every vertex exactly once).

>[!tips] 18.2 Toughness
>A graph $G$ is $t$-tough if for every vertex cut $S$, the number of components $c(G-S) \le |S|/t$. Hamiltonian graphs are necessarily 1-tough.

>[!tips] 18.3 Closure
>The closure of $G$, denoted $cl(G)$, is the graph obtained by recursively joining pairs of non-adjacent vertices $u, v$ such that $d(u) + d(v) \ge n$.