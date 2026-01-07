>[!tips] 6.2 inner product
>An **inner product** on $V$ is a function that takes each ordered pair $(u, v)$ of elements of $V$ to a number $\langle u, v \rangle \in \mathbf{F}$ and has the following properties:
>- **positivity**: $\langle v, v \rangle \ge 0$ for all $v \in V$.
>- **definiteness**: $\langle v, v \rangle = 0$ if and only if $v = 0$.
>- **additivity in first slot**: $\langle u+v, w \rangle = \langle u, w \rangle + \langle v, w \rangle$ for all $u, v, w \in V$.
>- **homogeneity in first slot**: $\langle \lambda u, v \rangle = \lambda \langle u, v \rangle$ for all $\lambda \in \mathbf{F}, u, v \in V$.
>- **conjugate symmetry**: $\langle u, v \rangle = \overline{\langle v, u \rangle}$ for all $u, v \in V$.

>[!tips] 6.8 norm, $\|v\|$
>For $v \in V$, the **norm** of $v$, denoted $\|v\|$, is defined by
>$$\|v\| = \sqrt{\langle v, v \rangle}$$

>[!tips] 6.13 orthogonal
>Two vectors $u, v \in V$ are called **orthogonal** if $\langle u, v \rangle = 0$.

>[!tips] 6.23 orthonormal
>- A list of vectors is called **orthonormal** if each vector in the list has norm 1 and is orthogonal to all the other vectors in the list.
>- In other words, a list $e_1, \dots, e_m$ is orthonormal if $\langle e_j, e_k \rangle$ equals 1 if $j=k$ and 0 if $j \neq k$.

>[!tips] 6.46 orthogonal complement, $U^\perp$
>If $U$ is a subset of $V$, then the **orthogonal complement** of $U$, denoted $U^\perp$, is the set of all vectors in $V$ that are orthogonal to every vector in $U$:
>$$U^\perp = \{v \in V : \langle v, u \rangle = 0 \text{ for all } u \in U\}$$

>[!tips] 6.53 orthogonal projection, $P_U$
>Suppose $U$ is a finite-dimensional subspace of $V$. The **orthogonal projection** of $V$ onto $U$ is the operator $P_U \in \mathcal{L}(V)$ defined as follows: For $v \in V$, write $v = u+w$, where $u \in U$ and $w \in U^\perp$. Then $P_U v = u$.