# Definitions.md

> [!tip] 48.1 Baire Space
> A topological space $X$ is called a Baire space if the following condition holds: Given any countable collection $\{A_n\}$ of closed sets of $X$, each of which has empty interior in $X$, their union $\bigcup A_n$ also has empty interior in $X$.

> [!tip] 48.2 Category of a Set
> A subset $A$ of a topological space $X$ is said to be of the **first category** in $X$ if it is contained in a countable union of closed sets of $X$, each of which has empty interior in $X$. A subset $A$ is said to be of the **second category** in $X$ if it is not of the first category in $X$. (This implies that if $X$ is a Baire space, $X$ itself is of the second category).

> [!tip] 50.1 Order of a Covering
> A collection $\mathcal{A}$ of subsets of a space $X$ is said to have **order** $m+1$ if some point of $X$ lies in exactly $m+1$ elements of $\mathcal{A}$, and no point of $X$ lies in more than $m+1$ elements of $\mathcal{A}$.

> [!tip] 50.2 Topological Dimension (Lebesgue Covering Dimension)
> A space $X$ is said to be finite-dimensional if there is some integer $m$ such that for every open covering $\mathcal{A}$ of $X$, there is an open covering $\mathcal{B}$ of $X$ that refines $\mathcal{A}$ and has order at most $m+1$. The **topological dimension** of $X$ is defined to be the smallest such integer $m$.