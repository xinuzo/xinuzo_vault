# Definitions.md

> [!tip] 51.1 Homotopy
> Two continuous maps $f, f': X \to Y$ are said to be **homotopic** if there exists a continuous map $F: X \times I \to Y$ such that $F(x, 0) = f(x)$ and $F(x, 1) = f'(x)$ for all $x \in X$. The map $F$ is called a homotopy between $f$ and $f'$.

> [!tip] 51.2 Path Homotopy
> Two paths $f, f': I \to X$ from $x_0$ to $x_1$ are **path homotopic** if there is a continuous map $F: I \times I \to X$ such that $F(s, 0) = f(s)$ and $F(s, 1) = f'(s)$ for all $s \in I$, and additionally $F(0, t) = x_0$ and $F(1, t) = x_1$ for all $t \in I$. 

> [!tip] 51.3 Product of Paths
> If $f$ is a path in $X$ from $x_0$ to $x_1$, and $g$ is a path in $X$ from $x_1$ to $x_2$, the **product** $f * g$ is the path from $x_0$ to $x_2$ defined by traversing $f$ at twice the normal speed, followed by $g$ at twice the normal speed. Formally: $(f * g)(s) = f(2s)$ for $s \in [0, 1/2]$ and $(f * g)(s) = g(2s - 1)$ for $s \in [1/2, 1]$.

> [!tip] 52.1 The Fundamental Group
> The set of path-homotopy classes of loops based at $x_0$, equipped with the operation of path product $[f] * [g] = [f * g]$, is called the **fundamental group** of $X$ relative to the base point $x_0$. It is denoted by $\pi_1(X, x_0)$.

> [!tip] 52.2 Simply Connected Space
> A topological space $X$ is said to be **simply connected** if it is path-connected and its fundamental group $\pi_1(X, x_0)$ is the trivial group (consisting only of the identity element) for some, and hence every, $x_0 \in X$.

> [!tip] 52.3 Induced Homomorphism
> Let $h: (X, x_0) \to (Y, y_0)$ be a continuous map. The map $h$ induces a homomorphism $h_*: \pi_1(X, x_0) \to \pi_1(Y, y_0)$ defined by $h_*([f]) = [h \circ f]$. This is called the **homomorphism induced by $h$**.

> [!tip] 53.1 Covering Map and Covering Space
> Let $p: E \to B$ be a continuous surjective map. An open set $U \subset B$ is said to be **evenly covered** by $p$ if $p^{-1}(U)$ can be written as a union of disjoint open sets $V_\alpha$ in $E$, such that for each $\alpha$, the restriction of $p$ to $V_\alpha$ is a homeomorphism onto $U$. If every point $b \in B$ has an evenly covered neighborhood, $p$ is called a **covering map**, and $E$ is called a **covering space** of $B$.

> [!tip] 54.1 Lifting
> Let $p: E \to B$ be a map. If $f$ is a continuous map from a space $X$ to $B$, a **lifting** of $f$ is a continuous map $\tilde{f}: X \to E$ such that $p \circ \tilde{f} = f$.

> [!tip] 55.1 Retraction and Retract
> Let $A \subset X$. A continuous map $r: X \to A$ is called a **retraction** if $r(a) = a$ for every $a \in A$. If such a map exists, $A$ is said to be a **retract** of $X$.

> [!tip] 58.1 Deformation Retraction
> A continuous map $H: X \times I \to X$ is a **deformation retraction** of $X$ onto $A$ if $H(x, 0) = x$, $H(x, 1) \in A$, and $H(a, t) = a$ for all $x \in X, a \in A$, and $t \in I$. 

> [!tip] 58.2 Homotopy Equivalence (Homotopy Type)
> Two spaces $X$ and $Y$ are said to be **homotopy equivalent** (or to have the same **homotopy type**) if there exist continuous maps $f: X \to Y$ and $g: Y \to X$ such that $g \circ f$ is homotopic to the identity map $i_X$, and $f \circ g$ is homotopic to the identity map $i_Y$.