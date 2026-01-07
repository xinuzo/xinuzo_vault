>[!tips] 3.1 linear map
>A **linear map** from $V$ to $W$ is a function $T: V \to W$ with the following properties:
>- **additivity**: $T(u+v) = Tu + Tv$ for all $u, v \in V$.
>- **homogeneity**: $T(\lambda v) = \lambda(Tv)$ for all $\lambda \in \mathbf{F}$ and all $v \in V$.

>[!tips] 3.2 $\mathcal{L}(V, W)$
>The set of all linear maps from $V$ to $W$ is denoted by $\mathcal{L}(V, W)$.

>[!tips] 3.5 operations on linear maps
>Suppose $S, T \in \mathcal{L}(V, W)$ and $\lambda \in \mathbf{F}$.
>- **addition**: The sum $S+T$ is the linear map defined by $(S+T)(v) = Sv + Tv$ for all $v \in V$.
>- **scalar multiplication**: The product $\lambda T$ is the linear map defined by $(\lambda T)(v) = \lambda(Tv)$ for all $v \in V$.

>[!tips] 3.8 product of linear maps
>If $T \in \mathcal{L}(U, V)$ and $S \in \mathcal{L}(V, W)$, then the product $ST \in \mathcal{L}(U, W)$ is defined by $(ST)(u) = S(Tu)$ for all $u \in U$.

>[!tips] 3.11 null space, $\text{null } T$
>For $T \in \mathcal{L}(V, W)$, the **null space** of $T$, denoted $\text{null } T$, is the subset of $V$ consisting of those vectors that $T$ maps to 0:
>$$\text{null } T = \{v \in V : Tv = 0\}$$

>[!tips] 3.13 injective
>A function $T: V \to W$ is called **injective** if $Tu = Tv$ implies $u = v$.

>[!tips] 3.15 range, $\text{range } T$
>For $T \in \mathcal{L}(V, W)$, the **range** of $T$, denoted $\text{range } T$, is the subset of $W$ consisting of those vectors that are of the form $Tv$ for some $v \in V$:
>$$\text{range } T = \{Tv : v \in V\}$$

>[!tips] 3.17 surjective
>A function $T: V \to W$ is called **surjective** if its range equals $W$.

>[!tips] 3.22 matrix, $A_{j,k}$
>Suppose $m$ and $n$ are positive integers. An $m \times n$ **matrix** $A$ is a rectangular array of elements of $\mathbf{F}$ with $m$ rows and $n$ columns:
>$$A = \begin{pmatrix} A_{1,1} & \dots & A_{1,n} \\ \vdots & & \vdots \\ A_{m,1} & \dots & A_{m,n} \end{pmatrix}$$
>The notation $A_{j,k}$ denotes the entry in row $j$, column $k$ of $A$.

>[!tips] 3.25 matrix of a linear map, $\mathcal{M}(T)$
>Suppose $T \in \mathcal{L}(V, W)$ and $v_1, \dots, v_n$ is a basis of $V$ and $w_1, \dots, w_m$ is a basis of $W$. The **matrix of $T$** with respect to these bases is the $m \times n$ matrix $\mathcal{M}(T)$ whose entries $A_{j,k}$ are defined by:
>$$Tv_k = A_{1,k}w_1 + \dots + A_{m,k}w_m$$
>If the bases are not clear from context, the notation $\mathcal{M}(T, (v_1, \dots, v_n), (w_1, \dots, w_m))$ is used.

>[!tips] 3.30 matrix addition
>The sum of two matrices of the same size is the matrix obtained by adding corresponding entries.

>[!tips] 3.32 matrix scalar multiplication
>The product of a scalar and a matrix is the matrix obtained by multiplying each entry by the scalar.

>[!tips] 3.34 matrix multiplication
>Suppose $A$ is an $m \times n$ matrix and $C$ is an $n \times p$ matrix. Then $AC$ is defined to be the $m \times p$ matrix whose entry in row $j$, column $k$ is given by
>$$(AC)_{j,k} = \sum_{r=1}^n A_{j,r} C_{r,k}$$

>[!tips] 3.53 invertible, inverse
>- A linear map $T \in \mathcal{L}(V, W)$ is called **invertible** if there exists a linear map $S \in \mathcal{L}(W, V)$ such that $ST$ equals the identity map on $V$ and $TS$ equals the identity map on $W$.
>- A linear map $S$ satisfying $ST = I$ and $TS = I$ is called an **inverse** of $T$.

>[!tips] 3.58 isomorphic, isomorphism
>- Two vector spaces $V$ and $W$ are called **isomorphic** if there exists an invertible linear map from $V$ onto $W$.
>- An invertible linear map is sometimes called an **isomorphism**.

>[!tips] 3.60 matrix of a vector, $\mathcal{M}(v)$
>Suppose $v \in V$ and $v_1, \dots, v_n$ is a basis of $V$. The **matrix of $v$** with respect to this basis is the $n \times 1$ matrix defined by
>$$\mathcal{M}(v) = \begin{pmatrix} c_1 \\ \vdots \\ c_n \end{pmatrix}$$
>where $v = c_1v_1 + \dots + c_nv_n$.

>[!tips] 3.62 operator, $\mathcal{L}(V)$
>- A linear map from a vector space to itself is called an **operator**.
>- The notation $\mathcal{L}(V)$ denotes the set of all operators on $V$. In other words, $\mathcal{L}(V) = \mathcal{L}(V, V)$.

>[!tips] 3.67 product of vector spaces
>Suppose $V_1, \dots, V_m$ are vector spaces over $\mathbf{F}$.
>- The **product** $V_1 \times \dots \times V_m$ is defined by
>$$V_1 \times \dots \times V_m = \{(v_1, \dots, v_m) : v_1 \in V_1, \dots, v_m \in V_m\}$$
>- Addition on $V_1 \times \dots \times V_m$ is defined by
>$$(u_1, \dots, u_m) + (v_1, \dots, v_m) = (u_1+v_1, \dots, u_m+v_m)$$
>- Scalar multiplication on $V_1 \times \dots \times V_m$ is defined by
>$$\lambda(v_1, \dots, v_m) = (\lambda v_1, \dots, \lambda v_m)$$

>[!tips] 3.73 affine subset
>- An **affine subset** of $V$ is a subset of $V$ of the form $v + U$ for some $v \in V$ and some subspace $U$ of $V$.
>- The affine subset $v+U$ is said to be **parallel** to $U$.

>[!tips] 3.76 quotient space, $V/U$
>Suppose $U$ is a subspace of $V$. Then the **quotient space** $V/U$ is the set of all affine subsets of $V$ parallel to $U$. In other words,
>$$V/U = \{v+U : v \in V\}$$

>[!tips] 3.79 addition and scalar multiplication on $V/U$
>Suppose $U$ is a subspace of $V$. Then addition and scalar multiplication are defined on $V/U$ by
>$$(v+U) + (w+U) = (v+w) + U$$
>$$\lambda(v+U) = (\lambda v) + U$$
>for all $v, w \in V$ and all $\lambda \in \mathbf{F}$.

>[!tips] 3.86 quotient map, $\pi$
>Suppose $U$ is a subspace of $V$. The **quotient map** $\pi$ is the linear map $\pi: V \to V/U$ defined by
>$$\pi(v) = v+U$$
>for all $v \in V$.

>[!tips] 3.91 dual space, $V'$
>The **dual space** of $V$, denoted $V'$, is the vector space of all linear functionals on $V$. In other words, $V' = \mathcal{L}(V, \mathbf{F})$.

>[!tips] 3.92 linear functional
>A **linear functional** on $V$ is a linear map from $V$ to the scalar field $\mathbf{F}$. In other words, it is an element of $\mathcal{L}(V, \mathbf{F})$.

>[!tips] 3.94 dual basis
>If $v_1, \dots, v_n$ is a basis of $V$, then the **dual basis** of $v_1, \dots, v_n$ is the list $\varphi_1, \dots, \varphi_n$ of elements of $V'$ defined by
>$$\varphi_j(v_k) = \begin{cases} 1 & \text{if } k=j \\ 0 & \text{if } k \neq j \end{cases}$$

>[!tips] 3.98 dual map, $T'$
>If $T \in \mathcal{L}(V, W)$, then the **dual map** of $T$ is the linear map $T' \in \mathcal{L}(W', V')$ defined by $T'(\varphi) = \varphi \circ T$ for all $\varphi \in W'$.

>[!tips] 3.103 annihilator, $U^0$
>For $U \subset V$, the **annihilator** of $U$, denoted $U^0$, is the subspace of $V'$ defined by
>$$U^0 = \{\varphi \in V' : \varphi(u) = 0 \text{ for all } u \in U\}$$

>[!tips] 3.111 matrix of dual map
>The transpose of a matrix $A$, denoted $A^t$, is the matrix obtained from $A$ by interchanging the rows and columns.