>[!tips] 5.2 invariant subspace
>Suppose $T \in \mathcal{L}(V)$. A subspace $U$ of $V$ is called **invariant** under $T$ if $u \in U$ implies $Tu \in U$.

>[!tips] 5.5 eigenvalue
>Suppose $T \in \mathcal{L}(V)$. A number $\lambda \in \mathbf{F}$ is called an **eigenvalue** of $T$ if there exists $v \in V$ such that $v \neq 0$ and $Tv = \lambda v$.

>[!tips] 5.7 eigenvector
>Suppose $T \in \mathcal{L}(V)$ and $\lambda \in \mathbf{F}$ is an eigenvalue of $T$. A vector $v \in V$ is called an **eigenvector** of $T$ corresponding to $\lambda$ if $Tv = \lambda v$ and $v \neq 0$.

>[!tips] 5.15 restriction operator, $T|_U$
>Suppose $T \in \mathcal{L}(V)$ and $U$ is an invariant subspace of $V$. The **restriction operator** $T|_U \in \mathcal{L}(U)$ is defined by $T|_U(u) = Tu$ for all $u \in U$.

>[!tips] 5.21 quotient operator, $T/U$
>Suppose $T \in \mathcal{L}(V)$ and $U$ is an invariant subspace of $V$. The **quotient operator** $T/U \in \mathcal{L}(V/U)$ is defined by $(T/U)(v+U) = Tv + U$ for all $v \in V$.

>[!tips] 5.25 diagonal of a matrix
>The **diagonal** of a square matrix consists of the entries along the line from the upper left corner to the bottom right corner.

>[!tips] 5.26 upper-triangular matrix
>A matrix is called **upper triangular** if all the entries below the diagonal equal 0.

>[!tips] 5.36 diagonal matrix
>A **diagonal matrix** is a square matrix that is 0 everywhere except possibly along the diagonal.

>[!tips] 5.38 diagonalizable
>An operator $T \in \mathcal{L}(V)$ is called **diagonalizable** if the operator has a diagonal matrix with respect to some basis of $V$.

>[!tips] 5.39 eigenspace, $E(\lambda, T)$
>Suppose $T \in \mathcal{L}(V)$ and $\lambda \in \mathbf{F}$. The **eigenspace** of $T$ corresponding to $\lambda$, denoted $E(\lambda, T)$, is defined by
>$$E(\lambda, T) = \text{null}(T - \lambda I) = \{v \in V : Tv = \lambda v\}$$