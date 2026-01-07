>[!tips] 7.5 properties of the adjoint
>Suppose $T \in \mathcal{L}(V, W)$.
>- The adjoint $T^*$ is a linear map from $W$ to $V$.
>- $(S+T)^* = S^* + T^*$ for all $S \in \mathcal{L}(V, W)$.
>- $(\lambda T)^* = \overline{\lambda} T^*$ for all $\lambda \in \mathbf{F}$.
>- $(T^*)^* = T$.
>- $(ST)^* = T^*S^*$ for all $T \in \mathcal{L}(V, W)$ and $S \in \mathcal{L}(W, U)$.

>[!tips] 7.13 eigenvalues of self-adjoint operators
>Every eigenvalue of a self-adjoint operator is real.

>[!tips] 7.24 Complex Spectral Theorem
>Suppose $\mathbf{F} = \mathbf{C}$ and $T \in \mathcal{L}(V)$. The following are equivalent:
>- $T$ is normal.
>- $V$ has an orthonormal basis consisting of eigenvectors of $T$.
>- $T$ has a diagonal matrix with respect to some orthonormal basis of $V$.

>[!tips] 7.29 Real Spectral Theorem
>Suppose $\mathbf{F} = \mathbf{R}$ and $T \in \mathcal{L}(V)$. The following are equivalent:
>- $T$ is self-adjoint.
>- $V$ has an orthonormal basis consisting of eigenvectors of $T$.
>- $T$ has a diagonal matrix with respect to some orthonormal basis of $V$.

>[!tips] 7.35 positive operators have unique positive square roots
>Every positive operator on $V$ has a unique positive square root.

>[!tips] 7.42 characterization of isometries
>Suppose $S \in \mathcal{L}(V)$. The following are equivalent:
>- $S$ is an isometry.
>- $\langle Su, Sv \rangle = \langle u, v \rangle$ for all $u, v \in V$.
>- $S^*S = I$.
>- $\{Se_1, \dots, Se_n\}$ is an orthonormal list for every orthonormal list $e_1, \dots, e_n$ of $V$.

>[!tips] 7.45 Polar Decomposition
>Suppose $T \in \mathcal{L}(V)$. Then there exists an isometry $S \in \mathcal{L}(V)$ such that
>$$T = S\sqrt{T^*T}$$

>[!tips] 7.51 Singular Value Decomposition
>Suppose $T \in \mathcal{L}(V)$ has singular values $s_1, \dots, s_n$. Then there exist orthonormal bases $e_1, \dots, e_n$ and $f_1, \dots, f_n$ of $V$ such that
>$$Tv = s_1\langle v, e_1 \rangle f_1 + \dots + s_n\langle v, e_n \rangle f_n$$
>for every $v \in V$.