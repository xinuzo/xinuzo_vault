

> [!tip] 1.1 Subset and Inclusion
> A set $A$ is a subset of $B$, denoted $A \subset B$, if every element of $A$ is also an element of $B$. If $A \subset B$ and $A \neq B$, $A$ is a proper subset of $B$, denoted $A \subsetneq B$.

> [!tip] 1.2 Union of Sets
> The union of $A$ and $B$ is the set $A \cup B = \{x \mid x \in A \text{ or } x \in B\}$. For an arbitrary collection $\mathcal{A}$, the union is $\bigcup_{A \in \mathcal{A}} A = \{x \mid x \in A \text{ for at least one } A \in \mathcal{A}\}$.

> [!tip] 1.3 Intersection of Sets
> The intersection of $A$ and $B$ is the set $A \cap B = \{x \mid x \in A \text{ and } x \in B\}$. For an arbitrary collection $\mathcal{A}$, the intersection is $\bigcap_{A \in \mathcal{A}} A = \{x \mid x \in A \text{ for every } A \in \mathcal{A}\}$.

> [!tip] 1.4 Disjoint Sets
> Sets $A$ and $B$ are disjoint if they have no elements in common, expressed as $A \cap B = \emptyset$.

> [!tip] 1.5 Difference of Sets
> The difference of two sets, $A - B$, is the set of elements of $A$ that are not in $B$: $A - B = \{x \mid x \in A \text{ and } x \notin B\}$.

> [!tip] 1.6 Power Set
> The power set of $A$, denoted $\mathcal{P}(A)$, is the set of all subsets of $A$.

> [!tip] 1.7 Cartesian Product
> The cartesian product $A \times B$ is the set of all ordered pairs $(a,b)$ where $a \in A$ and $b \in B$. For an indexed family $\{A_\alpha\}_{\alpha \in J}$, the cartesian product $\prod_{\alpha \in J} A_\alpha$ is the set of all functions $x: J \to \bigcup A_\alpha$ such that $x(\alpha) \in A_\alpha$ for each $\alpha$.

> [!tip] 1.8 Rule of Assignment
> A rule of assignment is a subset $r \subset C \times D$ where each element of $C$ appears as the first coordinate of at most one ordered pair in $r$.

> [!tip] 1.9 Function
> A function $f$ is a rule of assignment $r$, together with a set $B$ that contains the image set of $r$. We write $f: A \to B$, where $A$ is the domain and $B$ is the range.

> [!tip] 1.10 Restriction of a Function
> If $f: A \to B$ and $A_0 \subset A$, the restriction $f|A_0$ is the function mapping $A_0$ into $B$ whose rule is $\{(a, f(a)) \mid a \in A_0\}$.

> [!tip] 1.11 Composite Function
> Given $f: A \to B$ and $g: B \to C$, the composite $g \circ f: A \to C$ is defined by $(g \circ f)(a) = g(f(a))$.

> [!tip] 1.12 Injective, Surjective, Bijective
> * **Injective (One-to-one):** $f(a) = f(a') \implies a = a'$.
> * **Surjective (Onto):** For every $b \in B$, there exists at least one $a \in A$ such that $f(a) = b$.
> * **Bijective:** A function that is both injective and surjective.

> [!tip] 1.13 Image and Preimage
> For $A_0 \subset A$, the image is $f(A_0) = \{b \mid b = f(a) \text{ for at least one } a \in A_0\}$. For $B_0 \subset B$, the preimage is $f^{-1}(B_0) = \{a \mid f(a) \in B_0\}$.

> [!tip] 1.14 Relation and Equivalence Relation
> A relation on a set $A$ is a subset $C \subset A \times A$. An equivalence relation $\sim$ must be reflexive ($x \sim x$), symmetric ($x \sim y \implies y \sim x$), and transitive ($x \sim y \text{ and } y \sim z \implies x \sim z$).

> [!tip] 1.15 Order Relation (Simple Order)
> A relation $<$ is an order relation if it satisfies comparability (for $x \neq y$, either $x < y$ or $y < x$), nonreflexivity ($x \not< x$), and transitivity ($x < y$ and $y < z \implies x < z$).

> [!tip] 1.16 Bounds and Supremum/Infimum
> * **Upper Bound:** An element $b$ such that $x \le b$ for all $x \in A_0$.
> * **Least Upper Bound (Supremum):** The smallest element of the set of all upper bounds, denoted $\sup A_0$.
> * **Infimum:** The greatest lower bound, denoted $\inf A_0$.

> [!tip] 1.17 Cardinality Basics
> * **Finite:** A set in bijective correspondence with a section of positive integers $\{1, \dots, n\}$.
> * **Countably Infinite:** A set in bijective correspondence with the positive integers $\mathbb{Z}_+$.
> * **Countable:** A set that is either finite or countably infinite.
> * **Uncountable:** A set that is not countable.