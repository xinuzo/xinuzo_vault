>[!tips] 9.1 Equivalence Relation
>A relation $\sim$ on a set $S$ is an equivalence relation on $S$ if it satisfies the following three properties for all $a, b, c \in S$:
>1. **Reflexive**: $a \sim a$.
>2. **Symmetric**: If $a \sim b$, then $b \sim a$.
>3. **Transitive**: If $a \sim b$ and $b \sim c$, then $a \sim c$.

>[!tips] 9.1 Equivalence Class
>If $\sim$ is an equivalence relation on $S$ and $a \in S$, the set $[a] = \{x \in S : x \sim a\}$ is called the equivalence class of $a$. Each element in $[a]$ is called a representative of the class.

>[!tips] 9.1 Partition
>A partition of a set $S$ is a collection of nonempty disjoint subsets of $S$ whose union is $S$.

>[!tips] 10.1 Congruence Modulo n
>Let $n$ be a positive integer. Integers $a$ and $b$ are said to be congruent modulo $n$, written $a \equiv b \pmod n$, if $n$ divides $a - b$ (i.e., $a - b = nk$ for some $k \in \mathbb{Z}$).

>[!tips] 11.1 Integers Modulo n, $\mathbb{Z}_n$
>The set of equivalence classes modulo $n$ is denoted by $\mathbb{Z}_n$.
>$\mathbb{Z}_n = \{[0], [1], [2], ..., [n-1]\}$.

>[!tips] 11.1 Operations on $\mathbb{Z}_n$
>Addition: $[a] \oplus [b] = [a + b]$.
>Multiplication: $[a] \odot [b] = [ab]$.

>[!tips] 12.1 Common Divisor, GCD
>An integer $d$ is a common divisor of integers $a$ and $b$ if $d | a$ and $d | b$. The greatest common divisor (gcd) is the largest such integer, denoted $(a, b)$.

>[!tips] 12.1 Relatively Prime
>Two integers $a$ and $b$ are relatively prime if $(a, b) = 1$.

>[!tips] 12.1 Units in $\mathbb{Z}_n$, $\mathbb{U}_n$
>An element $[a] \in \mathbb{Z}_n$ is invertible (a unit) if there exists $[b] \in \mathbb{Z}_n$ such that $[a] \odot [b] = [1]$. The set of all units in $\mathbb{Z}_n$ is denoted $\mathbb{U}_n$.
>$\mathbb{U}_n = \{[a] \in \mathbb{Z}_n : (a, n) = 1\}$.

>[!tips] 13.1 Prime and Composite
>An integer $p > 1$ is prime if its only positive divisors are $1$ and $p$. An integer $n > 1$ that is not prime is composite.

>[!tips] 13.1 Euler's Phi-Function
>For $n \ge 1$, $\phi(n)$ denotes the number of positive integers less than or equal to $n$ that are relatively prime to $n$. Also $\phi(n) = |\mathbb{U}_n|$.