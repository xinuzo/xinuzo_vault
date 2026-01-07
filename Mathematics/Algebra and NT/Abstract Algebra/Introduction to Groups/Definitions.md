>[!tips] 2.5 Group
>A group is a set $G$ together with an operation $*$ on $G$ such that each of the following axioms is satisfied:
>1. **Associativity**: $a*(b*c) = (a*b)*c$ for all $a, b, c \in G$.
>2. **Existence of an identity element**: There is an element $e \in G$ such that $a*e = e*a = a$ for each $a \in G$.
>3. **Existence of inverse elements**: For each $a \in G$ there is an element $b \in G$ such that $a*b = b*a = e$.

>[!tips] 2.5 Abelian
>A group $G$ is said to be Abelian if the group operation is commutative ($ab = ba$ for all $a, b \in G$). Non-Abelian means not Abelian.

>[!tips] 2.5 Order of a Group
>The number of elements in the set underlying a group is called the order of the group, denoted by $|G|$. A group is said to be finite or infinite depending on whether its order is finite or infinite.

>[!tips] 2.6 Permutation
>A permutation of a nonempty set $S$ is a one-to-one mapping from $S$ onto $S$.

>[!tips] 2.6 Symmetric Group
>The set of all permutations of a nonempty set $S$ is a group with respect to composition. This group is called the symmetric group on $S$, and is denoted $Sym(S)$. When $S = \{1, 2, ..., n\}$, the group is denoted $S_n$.

>[!tips] 2.6 Cycle (k-cycle)
>If $S$ is a set, and $a_1, a_2, ..., a_k \in S$, then $(a_1 a_2 ... a_k)$ denotes the permutation of $S$ for which
>$$a_1 \mapsto a_2, a_2 \mapsto a_3, ..., a_{k-1} \mapsto a_k, a_k \mapsto a_1$$
>and $x \mapsto x$ for all other $x \in S$. Such a permutation is called a cycle or a k-cycle.

>[!tips] 2.6 Disjoint Cycles
>Cycles $(a_1 a_2 ... a_m)$ and $(b_1 b_2 ... b_n)$ are disjoint if $a_i \neq b_j$ for all $i, j$.

>[!tips] 2.7 Subgroup
>A subset $H$ of a group $G$ is a subgroup of $G$ if $H$ is itself a group with respect to the operation on $G$.

>[!tips] 2.7 Transposition
>A transposition is a 2-cycle.

>[!tips] 2.7 Even and Odd Permutations
>A permutation is even or odd according to whether it can be written as a product of an even or an odd number of transpositions, respectively.

>[!tips] 2.7 Alternating Group
>The set of all even permutations in $S_n$ forms a subgroup of $S_n$ for each $n \ge 2$. This subgroup is called the alternating group of degree $n$, and is denoted by $A_n$.

>[!tips] 2.7 Invariant Subgroup $G_T$
>Assume that $G$ is a permutation group on a set $S$, and that $T$ is a subset of $S$. Let
>$$G_T = \{ \alpha \in G : \alpha(t) = t \text{ for each } t \in T \}$$
>The elements of $G_T$ are said to leave $T$ elementwise invariant.