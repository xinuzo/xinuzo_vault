>[!tips] 12.1 Stable Set / Clique
>A **stable set** (independent set) is a set of vertices no two of which are adjacent. $\alpha(G)$ is the stability number.
>A **clique** is a set of vertices where every pair is adjacent. $\omega(G)$ is the clique number.

>[!tips] 12.1 Kernel
>A **kernel** in a digraph is a stable set $S$ such that every vertex outside $S$ dominates at least one vertex in $S$.

>[!tips] 12.2 Turán Graph $T_{k,n}$
>The complete $k$-partite graph on $n$ vertices with parts of size $\lfloor n/k \rfloor$ or $\lceil n/k \rceil$.

>[!tips] 12.3 Ramsey Number $r(k, l)$
>The smallest integer $n$ such that every graph on $n$ vertices contains either a clique of size $k$ or a stable set of size $l$.

>[!tips] 12.4 Regular Pair
>A pair of disjoint subsets $(X, Y)$ is $\epsilon$-regular if for all large subsets $X' \subseteq X, Y' \subseteq Y$, the density $d(X', Y')$ differs from $d(X, Y)$ by at most $\epsilon$.