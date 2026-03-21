# Definitions.md

> [!tip] 79.1 Equivalence of Covering Spaces
> Let $p_1: E_1 \to B$ and $p_2: E_2 \to B$ be covering maps. They are said to be **equivalent** if there exists a homeomorphism $h: E_1 \to E_2$ such that $p_2 \circ h = p_1$. The homeomorphism $h$ is called an equivalence of covering spaces.

> [!tip] 79.2 Universal Covering Space
> A covering space $p: E \to B$ is called a **universal covering space** if the total space $E$ is simply connected. (It is called "universal" because it covers every other connected covering space of $B$).

> [!tip] 81.1 Covering Transformation (Deck Transformation)
> Let $p: E \to B$ be a covering map. A **covering transformation** (or deck transformation) is an equivalence of the covering space with itself. That is, it is a homeomorphism $h: E \to E$ such that $p \circ h = p$. The set of all covering transformations forms a group under composition, denoted $\mathcal{C}(E, p, B)$.

> [!tip] 81.2 Regular Covering Space
> A covering space $p: E \to B$ is called **regular** (or normal) if, for every point $b \in B$ and any two points $e_1, e_2$ in the fiber $p^{-1}(b)$, there exists a covering transformation $h$ such that $h(e_1) = e_2$. (Geometrically, the group of covering transformations acts transitively on each fiber).

> [!tip] 81.3 Properly Discontinuous Action
> A group $G$ of homeomorphisms of a space $X$ acts **properly discontinuously** on $X$ if for every $x \in X$, there is a neighborhood $U$ of $x$ such that the sets $g(U)$ for $g \in G$ are entirely disjoint from one another (i.e., $g_1(U) \cap g_2(U) \neq \emptyset \implies g_1 = g_2$).

> [!tip] 82.1 Semilocally Simply Connected
> A space $B$ is said to be **semilocally simply connected** if for each point $b \in B$, there exists a neighborhood $U$ of $b$ such that the homomorphism induced by inclusion, $i_*: \pi_1(U, b) \to \pi_1(B, b)$, is the trivial homomorphism. (This means every loop in $U$ can be shrunk to a point in the larger space $B$, even if it can't be shrunk within $U$ itself).