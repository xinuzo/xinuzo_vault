>[!tips] Theorem 12.3 Turán's Theorem
>If a simple graph $G$ contains no $K_k$, then $e(G) \le e(T_{k-1, n})$. Equality holds iff $G \cong T_{k-1, n}$.

>[!tips] Theorem 12.6 Ramsey's Theorem
>For any positive integers $k, l$, the Ramsey number $r(k, l)$ exists.
>$$r(k, l) \le r(k-1, l) + r(k, l-1)$$

>[!tips] Theorem 12.8 Ramsey Lower Bound
>$$r(k, k) \ge 2^{k/2}$$
>(Proved using the probabilistic method).

>[!tips] Theorem 12.11 Schur's Theorem
>For any partition of $\{1, ..., r_n\}$ into $n$ subsets, one subset contains $x, y, z$ such that $x + y = z$.

>[!tips] Theorem 12.12 Szemerédi's Regularity Lemma
>Every sufficiently large graph admits a regular partition of its vertex set into a bounded number of parts.

>[!tips] Theorem 12.14 Erdős-Stone Theorem
>Every graph with $n$ vertices and sufficiently many edges (more than $e(T_{k-1, n}) + \epsilon n^2$) contains a copy of the Turán graph $T_{k, t}$ (for any fixed $t$).