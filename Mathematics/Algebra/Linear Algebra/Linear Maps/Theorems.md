>[!tips] 3.4 linear maps and basis of domain
>Suppose $v_1, \dots, v_n$ is a basis of $V$ and $w_1, \dots, w_n \in W$. Then there exists a unique linear map $T: V \to W$ such that
>$$Tv_j = w_j$$
>for each $j = 1, \dots, n$.

>[!tips] 3.6 $\mathcal{L}(V, W)$ is a vector space
>The set of all linear maps from $V$ to $W$ is a vector space with respect to the operations of addition and scalar multiplication.

>[!tips] 3.9 algebraic properties of linear maps
>- **associativity**: $(T_1T_2)T_3 = T_1(T_2T_3)$ whenever $T_1, T_2, T_3$ are linear maps such that the products make sense.
>- **identity**: $TI = T$ and $IT = T$ whenever $T \in \mathcal{L}(V, W)$.
>- **distributive properties**: $(S_1 + S_2)T = S_1T + S_2T$ and $S(T_1 + T_2) = ST_1 + ST_2$ whenever $T, S_1, S_2 \in \mathcal{L}(U, V)$ and $S, T_1, T_2 \in \mathcal{L}(V, W)$.

>[!tips] 3.12 null space is a subspace
>If $T \in \mathcal{L}(V, W)$, then $\text{null } T$ is a subspace of $V$.

>[!tips] 3.14 injectivity is equivalent to null space equals $\{0\}$
>Let $T \in \mathcal{L}(V, W)$. Then $T$ is injective if and only if $\text{null } T = \{0\}$.

>[!tips] 3.16 range is a subspace
>If $T \in \mathcal{L}(V, W)$, then $\text{range } T$ is a subspace of $W$.

>[!tips] 3.19 Fundamental Theorem of Linear Maps
>Suppose $V$ is finite-dimensional and $T \in \mathcal{L}(V, W)$. Then $\text{range } T$ is finite-dimensional and
>$$\dim V = \dim \text{null } T + \dim \text{range } T$$

>[!tips] 3.20 linear map to a smaller dimensional space is not injective
>Suppose $V$ and $W$ are finite-dimensional vector spaces such that $\dim V > \dim W$. Then no linear map from $V$ to $W$ is injective.

>[!tips] 3.21 linear map to a larger dimensional space is not surjective
>Suppose $V$ and $W$ are finite-dimensional vector spaces such that $\dim V < \dim W$. Then no linear map from $V$ to $W$ is surjective.

>[!tips] 3.36 matrix multiplication corresponds to map composition
>Suppose $T \in \mathcal{L}(U, V)$ and $S \in \mathcal{L}(V, W)$. Then
>$$\mathcal{M}(ST) = \mathcal{M}(S)\mathcal{M}(T)$$

>[!tips] 3.40 $\dim \mathcal{L}(V, W)$
>Suppose $V$ and $W$ are finite-dimensional. Then $\mathcal{L}(V, W)$ is finite-dimensional and
>$$\dim \mathcal{L}(V, W) = (\dim V)(\dim W)$$

>[!tips] 3.56 invertibility is equivalent to isomorphism
>A linear map is invertible if and only if it is both injective and surjective.

>[!tips] 3.59 dimension shows whether vector spaces are isomorphic
>Two finite-dimensional vector spaces over $\mathbf{F}$ are isomorphic if and only if they have the same dimension.

>[!tips] 3.61 $\mathcal{L}(V)$ and $\mathcal{M}(T)$ have identity
>If $v_1, \dots, v_n$ is a basis of $V$, then $\mathcal{M}(I)$ is the $n \times n$ identity matrix.

>[!tips] 3.65 matrix of product of linear maps
>Suppose $T \in \mathcal{L}(U, V)$ and $S \in \mathcal{L}(V, W)$. If bases are chosen for $U, V, W$, then $\mathcal{M}(ST) = \mathcal{M}(S)\mathcal{M}(T)$.

>[!tips] 3.69 injectivity and surjectivity in $\mathcal{L}(V)$
>Suppose $V$ is finite-dimensional and $T \in \mathcal{L}(V)$. Then the following are equivalent:
>- $T$ is invertible;
>- $T$ is injective;
>- $T$ is surjective.

>[!tips] 3.77 quotient space is a vector space
>Suppose $U$ is a subspace of $V$. Then $V/U$ is a vector space with the operations of addition and scalar multiplication defined in 3.79.

>[!tips] 3.89 dimension of a quotient space
>Suppose $V$ is finite-dimensional and $U$ is a subspace of $V$. Then
>$$\dim V/U = \dim V - \dim U$$

>[!tips] 3.95 dimension of dual space
>Suppose $V$ is finite-dimensional. Then $V'$ is also finite-dimensional and $\dim V' = \dim V$.

>[!tips] 3.99 properties of dual map
>Suppose $T \in \mathcal{L}(V, W)$. Then
>- $(S+T)' = S' + T'$ for all $S \in \mathcal{L}(V, W)$.
>- $(\lambda T)' = \lambda T'$ for all $\lambda \in \mathbf{F}$.
>- $(ST)' = T'S'$ for all $T \in \mathcal{L}(U, V)$ and $S \in \mathcal{L}(V, W)$.

>[!tips] 3.106 annihilator of a subspace
>Suppose $V$ is finite-dimensional and $U$ is a subspace of $V$. Then
>$$\dim U + \dim U^0 = \dim V$$

>[!tips] 3.107 null space of dual map
>Suppose $V$ and $W$ are finite-dimensional and $T \in \mathcal{L}(V, W)$. Then
>- $\text{null } T' = (\text{range } T)^0$
>- $\dim \text{null } T' = \dim \text{null } T + \dim W - \dim V$

>[!tips] 3.109 range of dual map
>Suppose $V$ and $W$ are finite-dimensional and $T \in \mathcal{L}(V, W)$. Then
>- $\text{range } T' = (\text{null } T)^0$
>- $\dim \text{range } T' = \dim \text{range } T$

>[!tips] 3.113 transpose of the matrix of a linear map
>Suppose $V$ and $W$ are finite-dimensional and $T \in \mathcal{L}(V, W)$. Then $\mathcal{M}(T') = (\mathcal{M}(T))^t$.

>[!tips] 3.114 rank of a matrix
>The row rank of a matrix equals the column rank of a matrix.