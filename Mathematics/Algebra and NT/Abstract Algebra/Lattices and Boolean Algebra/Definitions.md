>[!tips] 63.1 Partially Ordered Set (Poset)
>A set $S$ with a relation $\le$ that is reflexive ($a \le a$), antisymmetric ($a \le b$ and $b \le a \implies a=b$), and transitive ($a \le b$ and $b \le c \implies a \le c$).

>[!tips] 64.1 Lattice
>A poset in which every pair of elements $\{a, b\}$ has a least upper bound (join, $a \lor b$) and a greatest lower bound (meet, $a \land b$).

>[!tips] 65.1 Boolean Algebra
>A lattice with a minimum element 0 and maximum element 1 that is:
>1. **Distributive**: $a \land (b \lor c) = (a \land b) \lor (a \land c)$ (and dual).
>2. **Complemented**: For every $a$, there exists $a'$ such that $a \lor a' = 1$ and $a \land a' = 0$.

>[!tips] 66.1 Atom
>In a Boolean algebra, a nonzero element $a$ is an atom if $x \land a = x$ implies $x=0$ or $x=a$ (i.e., minimal nonzero elements).