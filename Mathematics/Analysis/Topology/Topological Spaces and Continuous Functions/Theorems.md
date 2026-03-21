
> [!theorem] Lemma 13.2 (Basis Criterion)
> Let $X$ be a topological space. Suppose $\mathcal{C}$ is a collection of open sets of $X$ such that for each open set $U$ of $X$ and each $x \in U$, there is an element $C \in \mathcal{C}$ such that $x \in C \subset U$. Then $\mathcal{C}$ is a basis for the topology of $X$.

> [!theorem] Lemma 13.3 (Comparing Topologies)
> Let $\mathcal{B}$ and $\mathcal{B}'$ be bases for topologies $\mathcal{T}$ and $\mathcal{T}'$, respectively, on $X$. Then $\mathcal{T}'$ is finer than $\mathcal{T}$ if and only if for each $x \in X$ and each basis element $B \in \mathcal{B}$ containing $x$, there is a basis element $B' \in \mathcal{B}'$ such that $x \in B' \subset B$.

> [!theorem] Theorem 15.1
> If $\mathcal{B}$ is a basis for the topology of $X$ and $\mathcal{C}$ is a basis for the topology of $Y$, then the collection $\mathcal{D} = \{B \times C \mid B \in \mathcal{B}, C \in \mathcal{C}\}$ is a basis for the product topology on $X \times Y$.

> [!theorem] Theorem 16.1
> If $\mathcal{B}$ is a basis for the topology of $X$, then the collection $\mathcal{B}_Y = \{B \cap Y \mid B \in \mathcal{B}\}$ is a basis for the subspace topology on $Y$.

> [!theorem] Theorem 17.1 (Properties of Closed Sets)
> Let $X$ be a topological space.
> 1. $\emptyset$ and $X$ are closed.
> 2. Arbitrary intersections of closed sets are closed.
> 3. Finite unions of closed sets are closed.

> [!theorem] Theorem 17.5
> Let $A$ be a subset of the topological space $X$. Let $A'$ be the set of all limit points of $A$. Then $\overline{A} = A \cup A'$.

> [!theorem] Theorem 17.6
> A subset of a topological space is closed if and only if it contains all its limit points.

> [!theorem] Theorem 17.8
> Every finite point set in a Hausdorff space $X$ is closed.

> [!theorem] Theorem 17.10
> Let $X$ be a Hausdorff space. Then a sequence of points of $X$ converges to at most one point of $X$.

> [!theorem] Theorem 18.1 (Equivalent Definitions of Continuity)
> Let $f: X \to Y$. The following are equivalent:
> 4. $f$ is continuous.
> 5. For every subset $A$ of $X$, $f(\overline{A}) \subset \overline{f(A)}$.
> 6. For every closed set $B$ of $Y$, the set $f^{-1}(B)$ is closed in $X$.
> 7. For each $x \in X$ and each neighborhood $V$ of $f(x)$, there is a neighborhood $U$ of $x$ such that $f(U) \subset V$.

> [!theorem] Theorem 18.2 (Rules for Constructing Continuous Functions)
> Let $X, Y, Z$ be topological spaces.
> 8. **Constant function:** If $f(x) = y_0$ for all $x$, $f$ is continuous.
> 9. **Inclusion:** If $A \subset X$, the inclusion map $j: A \to X$ is continuous.
> 10. **Composites:** If $f: X \to Y$ and $g: Y \to Z$ are continuous, then $g \circ f$ is continuous.
> 11. **Restricting the domain:** If $f: X \to Y$ is continuous and $A \subset X$, then $f|A$ is continuous.
> 12. **Restricting or expanding the range:** If $f: X \to Y$ is continuous and $Z$ is a space containing $Y$ as a subspace, then $f$ as a map to $Z$ is continuous.

> [!theorem] Theorem 18.3 (The Pasting Lemma)
> Let $X = A \cup B$, where $A$ and $B$ are closed in $X$. Let $f: A \to Y$ and $g: B \to Y$ be continuous. If $f(x) = g(x)$ for every $x \in A \cap B$, then $f$ and $g$ combine to give a continuous function $h: X \to Y$ defined by $h(x) = f(x)$ if $x \in A$, and $h(x) = g(x)$ if $x \in B$.

> [!theorem] Theorem 19.6
> Let $f: A \to \prod X_\alpha$ be given by the equation $f(a) = (f_\alpha(a))_{\alpha \in J}$. Let $\prod X_\alpha$ have the product topology. Then the function $f$ is continuous if and only if each coordinate function $f_\alpha: A \to X_\alpha$ is continuous.

> [!theorem] Theorem 20.3 (Sequence Lemma in Metric Spaces)
> Let $X$ be a topological space; let $A \subset X$. If there is a sequence of points of $A$ converging to $x$, then $x \in \overline{A}$. The converse holds if $X$ is metrizable.