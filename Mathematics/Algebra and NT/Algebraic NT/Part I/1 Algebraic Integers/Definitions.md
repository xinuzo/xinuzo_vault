## §1. Localization

>[!tips] 1.1 Multiplicative Subset
>A **multiplicative subset** $S$ of a ring $A$ is a subset containing $1$ such that whenever $x, y \in S$, the product $xy \in S$. We assume $0 \notin S$.

>[!tips] 1.1 Localization ($S^{-1}A$)
>Let $K$ be the quotient field of $A$, and $S$ a multiplicative subset. The ring **$S^{-1}A$** is the set of quotients $x/s$ with $x \in A$ and $s \in S$. $A$ has a canonical inclusion in $S^{-1}A$.

>[!tips] 1.1 Local Ring
>A **local ring** is a ring which has a unique maximal ideal.
>If $\mathfrak{o}$ is a local ring with maximal ideal $\mathfrak{m}$, then any element not in $\mathfrak{m}$ is a unit.

>[!tips] 1.1 Localization at a Prime ($A_{\mathfrak{p}}$)
>If $\mathfrak{p}$ is a prime ideal of $A$, let $S = A - \mathfrak{p}$. We denote $S^{-1}A$ by **$A_{\mathfrak{p}}$**. It is a local ring with maximal ideal $\mathfrak{m}_{\mathfrak{p}} = \mathfrak{p}A_{\mathfrak{p}}$.

## §2. Integral Closure

>[!tips] 1.2 Integral Element
>An element $x$ of a field $L$ containing $A$ is **integral over $A$** if it satisfies a monic polynomial with coefficients in $A$:
>$$x^n + a_{n-1}x^{n-1} + \dots + a_0 = 0, \quad a_i \in A$$
>Equivalently, there exists a finitely generated non-zero $A$-module $M \subset L$ such that $xM \subset M$.

>[!tips] 1.2 Integral Ring Extension
>A ring $B$ containing $A$ is **integral over $A$** if every element of $B$ is integral over $A$.

>[!tips] 1.2 Integral Closure
>Let $A \subset L$. The set of elements of $L$ which are integral over $A$ forms a ring called the **integral closure** of $A$ in $L$.

>[!tips] 1.2 Integrally Closed
>A ring $A$ is **integrally closed** if it is integrally closed in its quotient field.

>[!tips] 1.2 Number Field & Algebraic Integers
>A **number field** $K$ is a finite extension of the rational numbers $\mathbb{Q}$.
>The integral closure of $\mathbb{Z}$ in $K$ is called the ring of **algebraic integers** of $K$, denoted $\mathfrak{o}_K$.

## §3. Prime Ideals

>[!tips] 1.3 Lying Above ($\mathfrak{P} | \mathfrak{p}$)
>Let $A \subset B$. A prime ideal $\mathfrak{P}$ of $B$ is said to **lie above** a prime ideal $\mathfrak{p}$ of $A$ if $\mathfrak{P} \cap A = \mathfrak{p}$. We write $\mathfrak{P} | \mathfrak{p}$.

## §5. Galois Extensions

>[!tips] 1.5 Decomposition Group ($G_{\mathfrak{P}}$)
>Let $L/K$ be Galois with group $G$. Let $\mathfrak{P}$ be a prime of $B$ lying above $\mathfrak{p}$. The **decomposition group** $G_{\mathfrak{P}}$ is the subgroup of automorphism $\sigma \in G$ such that $\sigma \mathfrak{P} = \mathfrak{P}$.

>[!tips] 1.5 Decomposition Field ($L^d$)
>The fixed field of $G_{\mathfrak{P}}$, denoted $L^d$. It is the smallest subfield $E$ such that $\mathfrak{P}$ is the only prime lying above $\mathfrak{P} \cap E$.

>[!tips] 1.5 Inertia Group ($T_{\mathfrak{P}}$)
>The kernel of the homomorphism $G_{\mathfrak{P}} \to \text{Gal}((B/\mathfrak{P}) / (A/\mathfrak{p}))$. It consists of $\sigma \in G_{\mathfrak{P}}$ that induce the trivial automorphism on the residue class field.

>[!tips] 1.5 Frobenius Automorphism
>If $T_{\mathfrak{P}}$ is trivial, there exists a unique element $(\mathfrak{P}, K/k) \in G_{\mathfrak{P}}$ satisfying:
>$$\sigma \alpha \equiv \alpha^{N\mathfrak{p}} \pmod{\mathfrak{P}}$$
>for all $\alpha \in \mathfrak{o}_K$, where $N\mathfrak{p}$ is the size of the residue field.

>[!tips] 1.5 Splitting Completely
>A prime $\mathfrak{p}$ of $k$ **splits completely** in $E$ (degree $N$) if there are exactly $N$ different primes of $E$ lying above $\mathfrak{p}$.

## §6. Dedekind Rings

>[!tips] 1.6 Fractional Ideal
>A **fractional ideal** of $A$ in $K$ is an $A$-module $\mathfrak{a} \subset K$ such that there exists $c \in A, c \neq 0$ with $c\mathfrak{a} \subset A$.

>[!tips] 1.6 Dedekind Ring
>A ring which is:
>1. Noetherian
>2. Integrally closed
>3. Every non-zero prime ideal is maximal

>[!tips] 1.6 Order of an Ideal ($v_{\mathfrak{p}}$)
>If $\mathfrak{a} = \prod_{\mathfrak{p}} \mathfrak{p}^{r_{\mathfrak{p}}}$, then $r_{\mathfrak{p}}$ is the **order** of $\mathfrak{a}$ at $\mathfrak{p}$.

## §7. Discrete Valuation Rings

>[!tips] 1.7 Discrete Valuation Ring (DVR)
>A **discrete valuation ring** is a principal ideal ring having a unique non-zero prime ideal. It is a local Dedekind ring.

>[!tips] 1.7 Ramification Index ($e$)
>If $\mathfrak{p}B = \mathfrak{P}_1^{e_1} \dots \mathfrak{P}_r^{e_r}$, the integer $e_i$ is the **ramification index** of $\mathfrak{P}_i$ over $\mathfrak{p}$, denoted $e(\mathfrak{P}_i/\mathfrak{p})$.

>[!tips] 1.7 Residue Class Degree ($f$)
>The degree of the field extension $[B/\mathfrak{P} : A/\mathfrak{p}]$ is the **residue class degree**, denoted $f(\mathfrak{P}/\mathfrak{p})$.