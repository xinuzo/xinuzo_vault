>[!tips] 6.11 basic properties of the norm
>Suppose $v \in V$.
>- $\|v\| = 0$ if and only if $v = 0$.
>- $\|\lambda v\| = |\lambda| \|v\|$ for all $\lambda \in \mathbf{F}$.

>[!tips] 6.14 Pythagorean Theorem
>Suppose $u, v$ are orthogonal vectors in $V$. Then
>$$\|u+v\|^2 = \|u\|^2 + \|v\|^2$$

>[!tips] 6.15 Cauchy-Schwarz Inequality
>Suppose $u, v \in V$. Then
>$$|\langle u, v \rangle| \le \|u\| \|v\|$$
>This inequality is an equality if and only if one of $u, v$ is a scalar multiple of the other.

>[!tips] 6.18 Triangle Inequality
>Suppose $u, v \in V$. Then
>$$\|u+v\| \le \|u\| + \|v\|$$

>[!tips] 6.22 Parallelogram Equality
>Suppose $u, v \in V$. Then
>$$\|u+v\|^2 + \|u-v\|^2 = 2(\|u\|^2 + \|v\|^2)$$

>[!tips] 6.31 Gram-Schmidt Procedure
>Suppose $v_1, \dots, v_m$ is a linearly independent list of vectors in $V$. There exists an orthonormal list $e_1, \dots, e_m$ in $V$ such that
>$$\text{span}(v_1, \dots, v_j) = \text{span}(e_1, \dots, e_j)$$
>for $j = 1, \dots, m$.

>[!tips] 6.34 Schur's Theorem
>Suppose $V$ is a finite-dimensional complex vector space and $T \in \mathcal{L}(V)$. Then $T$ has an upper-triangular matrix with respect to some orthonormal basis of $V$.

>[!tips] 6.47 basic properties of orthogonal complement
>Suppose $U$ is a subspace of $V$.
>- $U^\perp$ is a subspace of $V$.
>- $U \cap U^\perp = \{0\}$.
>- If $V$ is finite-dimensional, then $V = U \oplus U^\perp$.
>- If $V$ is finite-dimensional, then $(U^\perp)^\perp = U$.

>[!tips] 6.58 Riesz Representation Theorem
>Suppose $V$ is finite-dimensional and $\varphi$ is a linear functional on $V$. Then there is a unique vector $u \in V$ such that
>$$\varphi(v) = \langle v, u \rangle$$
>for every $v \in V$.