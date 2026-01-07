>[!tips] 2.5 span is the smallest containing subspace
>The span of a list of vectors in $V$ is the smallest subspace of $V$ containing all the vectors in the list.

>[!tips] 2.12 $\mathcal{P}(\mathbf{F})$ is a subspace of $\mathbf{F}^\mathbf{F}$
>$\mathcal{P}(\mathbf{F})$ is a subspace of $\mathbf{F}^\mathbf{F}$.

>[!tips] 2.20 Linear Dependence Lemma
>Suppose $v_1, \dots, v_m$ is a linearly dependent list in $V$. Then there exists $j \in \{1, \dots, m\}$ such that:
>1. $v_j \in \text{span}(v_1, \dots, v_{j-1})$;
>2. if the $j^{\text{th}}$ term is removed from $v_1, \dots, v_m$, the span of the remaining list equals $\text{span}(v_1, \dots, v_m)$.

>[!tips] 2.22 length of linearly independent list $\le$ length of spanning list
>In a finite-dimensional vector space, the length of every linearly independent list of vectors is less than or equal to the length of every spanning list of vectors.

>[!tips] 2.23 finite-dimensional subspaces
>Every subspace of a finite-dimensional vector space is finite-dimensional.

>[!tips] 2.27 criterion for basis
>A list $v_1, \dots, v_n$ of vectors in $V$ is a basis of $V$ if and only if every $v \in V$ can be written uniquely in the form
>$$v = a_1v_1 + \dots + a_nv_n$$
>where $a_1, \dots, a_n \in \mathbf{F}$.

>[!tips] 2.28 spanning list contains a basis
>Every spanning list in a vector space can be reduced to a basis of the vector space.

>[!tips] 2.29 basis of finite-dimensional vector space
>Every finite-dimensional vector space has a basis.

>[!tips] 2.31 linearly independent list extends to a basis
>Every linearly independent list of vectors in a finite-dimensional vector space can be extended to a basis of the vector space.

>[!tips] 2.32 subspaces
>Suppose $V$ is finite-dimensional and $U$ is a subspace of $V$. Then $\dim U \le \dim V$.

>[!tips] 2.35 basis length does not depend on basis
>Any two bases of a finite-dimensional vector space have the same length.

>[!tips] 2.36 dimension of a subspace
>If $V$ is finite-dimensional and $U$ is a subspace of $V$, then $\dim U \le \dim V$.

>[!tips] 2.38 dimension of a direct sum
>If $U_1, \dots, U_m$ are finite-dimensional subspaces of $V$ such that $V = U_1 \oplus \dots \oplus U_m$, then
>$$\dim V = \dim U_1 + \dots + \dim U_m$$

>[!tips] 2.39 dimension of a sum
>If $U_1$ and $U_2$ are subspaces of a finite-dimensional vector space, then
>$$\dim(U_1 + U_2) = \dim U_1 + \dim U_2 - \dim(U_1 \cap U_2)$$