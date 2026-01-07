>[!tips] 1.1 Mapping, Domain, Codomain
>A mapping from a set $S$ to a set $T$ is a relationship (rule, correspondence) that assigns to each element of $S$ a uniquely determined element of $T$. The set $S$ is called the domain of the mapping, and the set $T$ is called the codomain.
>
>Written as $\alpha: S \to T$ or $S \to T$. If $x$ is an element of $S$, then $\alpha(x)$ denotes the unique element of $T$ assigned to $x$; $\alpha(x)$ is called the image of $x$ under the mapping $\alpha$.

>[!tips] 1.1 Equal Mappings
>Two mappings $\alpha$ and $\beta$ are said to be equal if their domains are equal, their codomains are equal, and $\alpha(x) = \beta(x)$ for every $x$ in their common domain.

>[!tips] 1.1 Identity Mapping
>The identity mapping on a set $S$, denoted by $\iota$ (or $\iota_S$), is defined by $\iota(x) = x$ for each $x \in S$.

>[!tips] 1.1 Image of a Set
>If $\alpha: S \to T$ and $A$ is a subset of $S$, then $\alpha(A)$ denotes the set of elements of $T$ that are images of elements of $A$ under the mapping $\alpha$.
>$$\alpha(A) = \{ \alpha(x) : x \in A \}$$
>The set $\alpha(A)$ is called the image of $A$ under the mapping $\alpha$. The set $\alpha(S)$ is called the image of $\alpha$.

>[!tips] 1.1 Onto Mapping
>A mapping $\alpha: S \to T$ is said to be onto if $\alpha(S) = T$. Thus $\alpha$ is onto if for each $y \in T$ there is at least one $x \in S$ such that $\alpha(x) = y$.

>[!tips] 1.1 One-to-one Mapping
>A mapping $\alpha: S \to T$ is said to be one-to-one if $x_1 \neq x_2$ implies $\alpha(x_1) \neq \alpha(x_2)$ ($x_1, x_2 \in S$).
>Equivalently: $\alpha$ is one-to-one iff $\alpha(x_1) = \alpha(x_2)$ implies $x_1 = x_2$.

>[!tips] 1.1 Infinite/Finite Set
>A set $S$ is infinite if there exists a mapping from $S$ to $S$ that is one-to-one but not onto. Otherwise, $S$ is finite.

>[!tips] 1.2 Composition
>If $\alpha: S \to T$ and $\beta: T \to U$, the composition (or composite) of $\alpha$ and $\beta$, denoted by $\beta \circ \alpha$, is the mapping from $S$ to $U$ defined by
>$$(\beta \circ \alpha)(x) = \beta(\alpha(x))$$
>for each $x \in S$.

>[!tips] 1.2 Inverse Mapping, Invertible
>A mapping $\beta: T \to S$ is an inverse of $\alpha: S \to T$ if both $\beta \circ \alpha = \iota_S$ and $\alpha \circ \beta = \iota_T$. A mapping is said to be invertible if it has an inverse.

>[!tips] 1.3 Operation
>An operation on a set $S$ is a relationship (rule, correspondence) that assigns to each ordered pair of elements of $S$ a uniquely determined element of $S$. (Often called a binary operation).

>[!tips] 1.3 Associative
>An operation $*$ on a set $S$ is said to be associative if it satisfies the condition
>$$a*(b*c) = (a*b)*c$$
>for all $a, b, c \in S$.

>[!tips] 1.3 Identity Element
>An element $e$ in a set $S$ is an identity (or identity element) for an operation $*$ on $S$ if
>$$e*a = a*e = a$$
>for each $a \in S$.

>[!tips] 1.3 Inverse Element
>Assume that $*$ is an operation on $S$, with identity $e$, and that $a \in S$. An element $b$ in $S$ is an inverse of $a$ relative to $*$ if
>$$a*b = b*a = e$$

>[!tips] 1.3 Commutative
>An operation $*$ on a set $S$ is said to be commutative if
>$$a*b = b*a$$
>for all $a, b \in S$.