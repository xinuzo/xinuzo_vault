# Definitions - Chapter II: Completions

## §1. Definitions and Completions

>[!tips] 2.1 Absolute Value
>An **absolute value** on a field $K$ is a real-valued function $x \mapsto |x|_v$ satisfying:
>1. $|x|_v \ge 0$ and $|x|_v = 0 \iff x = 0$.
>2. $|xy|_v = |x|_v |y|_v$.
>3. $|x+y|_v \le |x|_v + |y|_v$.

>[!tips] 2.1 Valuation (Non-Archimedean)
>An absolute value is called a **valuation** (or non-archimedean) if it satisfies the stronger condition:
>$$|x+y|_v \le \max(|x|_v, |y|_v)$$

>[!tips] 2.1 Equivalence of Absolute Values
>Two absolute values are **dependent** (or equivalent) if they define the same topology. This holds if and only if there exists $\lambda > 0$ such that $|x|_1 = |x|_2^\lambda$ for all $x \in K$.

>[!tips] 2.1 Completion ($K_v$)
>A field $K$ is **complete** if every Cauchy sequence has a limit. The **completion** $K_v$ is the set of equivalence classes of Cauchy sequences from $K$.

>[!tips] 2.1 Canonical Set ($M_K$)
>For a number field $K$, the set $M_K$ consists of the $p$-adic absolute values (defined by prime ideals) and the absolute values induced by embeddings into $\mathbb{R}$ or $\mathbb{C}$ (archimedean).

## §3. Some Filtrations

>[!tips] 2.3 Units and Filtration ($U_i$)
>In a complete discrete valuation ring $\mathfrak{o}$, the units are $U = \mathfrak{o} \setminus \mathfrak{p}$.
>We define subgroups $U_i = 1 + \mathfrak{p}^i$ for $i \ge 1$, and $U_0 = U$.

## §4. Unramified Extensions

>[!tips] 2.4 Unramified Extension
>A finite extension $E/K$ is **unramified** if $[E:K] = [B/\mathfrak{P} : A/\mathfrak{p}]$ (residue class degree equals extension degree) and the residue field extension is separable. Equivalently, the ramification index $e=1$.

## §5. Tamely Ramified Extensions

>[!tips] 2.5 Totally Ramified
>An extension $E/K$ is **totally ramified** if $[E:K] = e$, meaning the residue degree $f=1$.

>[!tips] 2.5 Tamely Ramified
>An extension is **tamely ramified** if the characteristic $p$ of the residue field does not divide the ramification index $e$. If $p | e$, it is **strongly ramified**.