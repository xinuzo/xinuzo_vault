>[!tips] 8.2 generalized eigenvector
>Suppose $T \in \mathcal{L}(V)$ and $\lambda$ is an eigenvalue of $T$. A vector $v \in V$ is called a **generalized eigenvector** of $T$ corresponding to $\lambda$ if $v \neq 0$ and
>$$(T-\lambda I)^j v = 0$$
>for some positive integer $j$.

>[!tips] 8.9 generalized eigenspace, $G(\lambda, T)$
>Suppose $T \in \mathcal{L}(V)$ and $\lambda \in \mathbf{F}$. The **generalized eigenspace** of $T$ corresponding to $\lambda$, denoted $G(\lambda, T)$, is the set of all generalized eigenvectors of $T$ corresponding to $\lambda$, along with the 0 vector.
>$$G(\lambda, T) = \text{null}((T-\lambda I)^{\dim V})$$

>[!tips] 8.16 nilpotent
>An operator $N \in \mathcal{L}(V)$ is called **nilpotent** if some power of it equals 0.

>[!tips] 8.35 characteristic polynomial
>Suppose $V$ is a complex vector space and $T \in \mathcal{L}(V)$. Let $\lambda_1, \dots, \lambda_m$ denote the distinct eigenvalues of $T$, with multiplicities $d_1, \dots, d_m$. The **characteristic polynomial** of $T$ is the polynomial
>$$(z-\lambda_1)^{d_1} \dots (z-\lambda_m)^{d_m}$$

>[!tips] 8.46 minimal polynomial
>Suppose $T \in \mathcal{L}(V)$. The **minimal polynomial** of $T$ is the unique monic polynomial $p$ of smallest degree such that $p(T) = 0$.

>[!tips] 8.56 Jordan basis
>A basis of $V$ is called a **Jordan basis** for $T \in \mathcal{L}(V)$ if $T$ has a block diagonal matrix with respect to this basis, where each block is of the form
>$$\begin{pmatrix} \lambda & 1 & & 0 \\ & \ddots & \ddots & \\ & & \ddots & 1 \\ 0 & & & \lambda \end{pmatrix}$$