>[!tips] 2.7 Sequence
>A function $f$ defined on the set $J$ of all positive integers. If $f(n) = x_n$, for $n \in J$, it is denoted by $\{x_n\}$.

>[!tips] 2.15 Metric Space
>A set $X$ is said to be a metric space if with any two points $p$ and $q$ of $X$ there is associated a real number $d(p, q)$, called the distance from $p$ to $q$, such that:
>(a) $d(p, q) > 0$ if $p \ne q$; $d(p, p) = 0$;
>(b) $d(p, q) = d(q, p)$;
>(c) $d(p, q) \le d(p, r) + d(r, q)$, for any $r \in X$.

>[!tips] 2.17 k-cell, Ball, Convex
>If $a_i < b_i$ for $i=1,...,k$, the set of all points $x = (x_1, ..., x_k)$ in $R^k$ such that $a_i \le x_i \le b_i$ is called a k-cell.
>Open ball $B$ with center $x$ and radius $r > 0$: $\{y \in R^k : |y - x| < r\}$.
>A set $E \subset R^k$ is convex if $\lambda x + (1 - \lambda)y \in E$ whenever $x \in E, y \in E$, and $0 < \lambda < 1$.

>[!tips] 2.18 Topological Properties
>Let $X$ be a metric space.
>(a) A neighborhood of $p$ is a set $N_r(p) = \{q : d(p, q) < r\}$.
>(b) $p$ is a limit point of $E$ if every neighborhood of $p$ contains a point $q \ne p$ such that $q \in E$.
>(c) If $p \in E$ and $p$ is not a limit point of $E$, then $p$ is an isolated point of $E$.
>(d) $E$ is closed if every limit point of $E$ is a point of $E$.
>(e) $p$ is an interior point of $E$ if there is a neighborhood $N$ of $p$ such that $N \subset E$.
>(f) $E$ is open if every point of $E$ is an interior point of $E$.
>(g) The complement of $E$ (denoted by $E^c$) is the set of all points $p \in X$ such that $p \notin E$.
>(h) $E$ is perfect if $E$ is closed and if every point of $E$ is a limit point of $E$.
>(i) $E$ is bounded if there is a real number $M$ and a point $q \in X$ such that $d(p, q) < M$ for all $p \in E$.
>(j) $E$ is dense in $X$ if every point of $X$ is a limit point of $E$, or a point of $E$ (or both).

>[!tips] 2.26 Closure
>If $E \subset X$, the closure of $E$ is the set $\bar{E} = E \cup E'$, where $E'$ is the set of all limit points of $E$.

>[!tips] 2.31 Open Cover
>By an open cover of a set $E$ in a metric space $X$ we mean a collection $\{G_\alpha\}$ of open subsets of $X$ such that $E \subset \bigcup_\alpha G_\alpha$.

>[!tips] 2.32 Compact
>A subset $K$ of a metric space $X$ is said to be compact if every open cover of $K$ contains a finite subcover.

>[!tips] 2.45 Separated, Connected
>Two subsets $A$ and $B$ of a metric space $X$ are said to be separated if both $A \cap \bar{B}$ and $\bar{A} \cap B$ are empty.
>A set $E \subset X$ is said to be connected if $E$ is not a union of two nonempty separated sets.