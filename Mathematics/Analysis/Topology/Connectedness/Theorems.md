# Theorems.md

> [!theorem] Theorem 23.1
> A space $X$ is connected if and only if the only subsets of $X$ that are both open and closed in $X$ are the empty set and $X$ itself.

> [!theorem] Lemma 23.2
> If the sets $C$ and $D$ form a separation of $X$, and if $Y$ is a connected subspace of $X$, then $Y$ lies entirely within either $C$ or $D$.

> [!theorem] Theorem 23.3
> The union of a collection of connected subspaces of $X$ that have a point in common is connected.

> [!theorem] Theorem 23.4
> Let $A$ be a connected subspace of $X$. If $A \subset B \subset \overline{A}$, then $B$ is also connected.

> [!theorem] Theorem 23.5
> The image of a connected space under a continuous map is connected.

> [!theorem] Theorem 23.6
> A finite cartesian product of connected spaces is connected.

> [!theorem] Theorem 24.1
> If $L$ is a linear continuum in the order topology, then $L$ is connected, and so are intervals and rays in $L$.

> [!theorem] Corollary 24.2
> The real line $\mathbb{R}$ is connected.

> [!theorem] Theorem 24.3 (Intermediate Value Theorem)
> Let $f: X \to Y$ be a continuous map, where $X$ is a connected space and $Y$ is an ordered set in the order topology. If $a$ and $b$ are two points of $X$ and if $r$ is a point of $Y$ lying between $f(a)$ and $f(b)$, then there exists a point $c$ of $X$ such that $f(c) = r$.

> [!theorem] Theorem 25.4
> A space $X$ is locally connected if and only if for every open set $U$ of $X$, each component of $U$ is open in $X$.

> [!theorem] Lemma 26.1
> Let $Y$ be a subspace of $X$. Then $Y$ is compact if and only if every covering of $Y$ by sets open in $X$ contains a finite subcollection covering $Y$.

> [!theorem] Theorem 26.2
> Every closed subspace of a compact space is compact.

> [!theorem] Theorem 26.3
> Every compact subspace of a Hausdorff space is closed.

> [!theorem] Theorem 26.5
> The image of a compact space under a continuous map is compact.

> [!theorem] Theorem 26.6
> Let $f: X \to Y$ be a bijective continuous function. If $X$ is compact and $Y$ is Hausdorff, then $f$ is a homeomorphism.

> [!theorem] Theorem 26.7
> The product of finitely many compact spaces is compact.

> [!theorem] Theorem 26.9
> Let $X$ be a topological space. Then $X$ is compact if and only if for every collection $\mathcal{C}$ of closed sets in $X$ having the finite intersection property, the intersection $\bigcap_{C \in \mathcal{C}} C$ of all the elements of $\mathcal{C}$ is nonempty.

> [!theorem] Theorem 27.1
> Every closed interval in $\mathbb{R}$ is compact.

> [!theorem] Theorem 27.3 (Extreme Value Theorem)
> Let $f: X \to Y$ be continuous, where $Y$ is an ordered set in the order topology. If $X$ is compact, then there exist points $c$ and $d$ in $X$ such that $f(c) \le f(x) \le f(d)$ for every $x \in X$.

> [!theorem] Theorem 27.4 (Heine-Borel Theorem)
> A subspace $A$ of $\mathbb{R}^n$ is compact if and only if it is closed and is bounded in the euclidean metric $d$ or the square metric $\rho$.

> [!theorem] Theorem 28.1
> Compactness implies limit point compactness, but not conversely.

> [!theorem] Theorem 28.2
> Let $X$ be a metrizable space. Then the following are equivalent:
> 1. $X$ is compact.
> 2. $X$ is limit point compact.
> 3. $X$ is sequentially compact.

> [!theorem] Theorem 29.1 (One-Point Compactification)
> Let $X$ be a space. Then $X$ is locally compact Hausdorff if and only if there exists a space $Y$ satisfying the following conditions:
> 4. $X$ is a subspace of $Y$.
> 5. The set $Y - X$ consists of a single point.
> 6. $Y$ is a compact Hausdorff space.
> If $Y$ and $Y'$ are two spaces satisfying these conditions, then there is a homeomorphism of $Y$ with $Y'$ that equals the identity map on $X$.