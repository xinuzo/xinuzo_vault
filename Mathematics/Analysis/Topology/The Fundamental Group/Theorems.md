# Theorems.md

> [!theorem] Theorem 51.1
> The relations of homotopy $\simeq$ and path homotopy $\simeq_p$ are equivalence relations.

> [!theorem] Theorem 51.2 (Properties of Path Product)
> The operation $*$ on path-homotopy classes has the following properties:
> 1. **Associativity:** $([f] * [g]) * [h] = [f] * ([g] * [h])$.
> 2. **Right and Left Identities:** If $e_x$ is the constant path at $x$, then $[f] * [e_{x_1}] = [f]$ and $[e_{x_0}] * [f] = [f]$.
> 3. **Inverse:** If $\bar{f}$ is the reverse of $f$ (defined by $\bar{f}(s) = f(1-s)$), then $[f] * [\bar{f}] = [e_{x_0}]$ and $[\bar{f}] * [f] = [e_{x_1}]$.

> [!theorem] Theorem 52.1
> The fundamental group $\pi_1(X, x_0)$ is a group under the operation of path product.

> [!theorem] Theorem 52.4 (Functorial Properties)
> Let $h: (X, x_0) \to (Y, y_0)$ and $k: (Y, y_0) \to (Z, z_0)$ be continuous maps. Then:
> 4. $(k \circ h)_* = k_* \circ h_*$.
> 5. $(i_X)_*$ is the identity homomorphism on $\pi_1(X, x_0)$.

> [!theorem] Lemma 54.1 (Path Lifting Lemma)
> Let $p: E \to B$ be a covering map, and let $p(e_0) = b_0$. Any path $f: [0, 1] \to B$ beginning at $b_0$ has a unique lifting to a path $\tilde{f}$ in $E$ beginning at $e_0$.

> [!theorem] Lemma 54.2 (Homotopy Lifting Lemma)
> Let $p: E \to B$ be a covering map, and let $p(e_0) = b_0$. Any path homotopy $F: I \times I \to B$ beginning at $b_0$ has a unique lifting to a path homotopy $\tilde{F}$ in $E$ beginning at $e_0$.

> [!theorem] Theorem 54.5
> The fundamental group of the circle $\pi_1(S^1, x_0)$ is isomorphic to the additive group of integers $\mathbb{Z}$.

> [!theorem] Theorem 55.1 (No Retraction Theorem)
> There is no retraction of the solid disk $B^2$ onto the circle $S^1$.

> [!theorem] Theorem 55.6 (Brouwer Fixed-Point Theorem for $B^2$)
> Every continuous map $f: B^2 \to B^2$ has at least one fixed point (a point $x$ such that $f(x) = x$).

> [!theorem] Theorem 56.1 (The Fundamental Theorem of Algebra)
> Every polynomial equation $x^n + a_{n-1}x^{n-1} + \dots + a_0 = 0$ of degree $n \ge 1$ with real or complex coefficients has at least one root in the complex plane.

> [!theorem] Theorem 57.3 (The Borsuk-Ulam Theorem for $S^2$)
> If $f: S^2 \to \mathbb{R}^2$ is a continuous map, then there exists a point $x \in S^2$ such that $f(x) = f(-x)$.

> [!theorem] Theorem 58.7 (Homotopy Invariance of the Fundamental Group)
> If $X$ and $Y$ are path-connected spaces that have the same homotopy type, then their fundamental groups are isomorphic.

> [!theorem] Theorem 59.3
> For $n \ge 2$, the $n$-dimensional sphere $S^n$ is simply connected.