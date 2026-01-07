>[!tips] 1.5 Order
>Let $S$ be a set. An order on $S$ is a relation, denoted by $<$, with the following two properties:
>(i) If $x \in S$ and $y \in S$ then one and only one of the statements $x < y$, $x = y$, $y < x$ is true.
>(ii) If $x, y, z \in S$, if $x < y$ and $y < z$, then $x < z$.

>[!tips] 1.6 Ordered Set
>An ordered set is a set $S$ in which an order is defined.

>[!tips] 1.7 Upper Bound, Lower Bound
>Suppose $S$ is an ordered set, and $E \subset S$. If there exists a $\beta \in S$ such that $x \le \beta$ for every $x \in E$, we say that $E$ is bounded above, and call $\beta$ an upper bound of $E$.
>Lower bounds are defined in the same way (with $\ge$ in place of $\le$).

>[!tips] 1.8 Least Upper Bound (Supremum)
>Suppose $S$ is an ordered set, $E \subset S$, and $E$ is bounded above. Suppose there exists an $\alpha \in S$ with the following properties:
>(i) $\alpha$ is an upper bound of $E$.
>(ii) If $\gamma < \alpha$ then $\gamma$ is not an upper bound of $E$.
>Then $\alpha$ is called the least upper bound of $E$ or the supremum of $E$, and we write $\alpha = \sup E$.

>[!tips] 1.8 Greatest Lower Bound (Infimum)
>The greatest lower bound, or infimum, of a set $E$ which is bounded below is defined in the same manner: The statement $\alpha = \inf E$ means that $\alpha$ is a lower bound of $E$ and that no $\beta$ with $\beta > \alpha$ is a lower bound of $E$.

>[!tips] 1.10 Least-upper-bound Property
>An ordered set $S$ is said to have the least-upper-bound property if the following is true: If $E \subset S$, $E$ is not empty, and $E$ is bounded above, then $\sup E$ exists in $S$.

>[!tips] 1.12 Field
>A field is a set $F$ with two operations, called addition and multiplication, which satisfy the following "field axioms" (A), (M), and (D):
>(A) Axioms for addition (Closure, Commutative, Associative, Identity 0, Inverse $-x$).
>(M) Axioms for multiplication (Closure, Commutative, Associative, Identity 1, Inverse $1/x$).
>(D) The distributive law: $x(y+z) = xy + xz$.

>[!tips] 1.17 Ordered Field
>An ordered field is a field $F$ which is also an ordered set, such that:
>(i) $x + y < x + z$ if $x, y, z \in F$ and $y < z$.
>(ii) $xy > 0$ if $x \in F, y \in F, x > 0$, and $y > 0$.

>[!tips] 1.23 Extended Real Number System
>The extended real number system consists of the real field $R$ and two symbols, $+\infty$ and $-\infty$. We preserve the original order in $R$, and define $-\infty < x < +\infty$ for every $x \in R$.

>[!tips] 1.24 Complex Number
>A complex number is an ordered pair $(a, b)$ of real numbers. $x = (a, b)$, $y = (c, d)$.
>$x + y = (a + c, b + d)$
>$xy = (ac - bd, ad + bc)$

>[!tips] 1.30 Conjugate
>If $a, b$ are real and $z = a + bi$, then the complex number $\bar{z} = a - bi$ is called the conjugate of $z$.

>[!tips] 1.32 Absolute Value
>If $z$ is a complex number, its absolute value $|z|$ is the non-negative square root of $z\bar{z}$; that is, $|z| = (z\bar{z})^{1/2}$.

>[!tips] 1.36 Euclidean k-space
>For each positive integer $k$, let $R^k$ be the set of all ordered k-tuples $x = (x_1, x_2, ..., x_k)$, where $x_i$ are real numbers (coordinates).
>Addition: $x + y = (x_1 + y_1, ..., x_k + y_k)$.
>Scalar multiplication: $\alpha x = (\alpha x_1, ..., \alpha x_k)$.
>Inner product: $x \cdot y = \sum_{i=1}^k x_i y_i$.
>Norm: $|x| = (x \cdot x)^{1/2} = (\sum_{1}^k x_i^2)^{1/2}$.