>[!tips] 5.6 equivalent conditions to be an invariant subspace
>Suppose $T \in \mathcal{L}(V)$ and $U$ is a subspace of $V$. Then the following are equivalent:
>- $U$ is invariant under $T$;
>- $T|_U$ is an operator on $U$;
>- $T$ maps $U$ into $U$.

>[!tips] 5.10 linearly independent eigenvectors
>Let $T \in \mathcal{L}(V)$. Suppose $\lambda_1, \dots, \lambda_m$ are distinct eigenvalues of $T$ and $v_1, \dots, v_m$ are corresponding eigenvectors. Then $v_1, \dots, v_m$ is linearly independent.

>[!tips] 5.13 number of eigenvalues
>Suppose $V$ is finite-dimensional. Then each operator on $V$ has at most $\dim V$ distinct eigenvalues.

>[!tips] 5.19 operators on complex vector spaces have an eigenvalue
>Every operator on a finite-dimensional, nonzero, complex vector space has an eigenvalue.

>[!tips] 5.27 conditions for upper-triangular matrix
>Suppose $T \in \mathcal{L}(V)$ and $v_1, \dots, v_n$ is a basis of $V$. The following are equivalent:
>- the matrix of $T$ with respect to $v_1, \dots, v_n$ is upper triangular;
>- $Tv_j \in \text{span}(v_1, \dots, v_j)$ for each $j = 1, \dots, n$;
>- $\text{span}(v_1, \dots, v_j)$ is invariant under $T$ for each $j = 1, \dots, n$.

>[!tips] 5.30 Upper-Triangular Matrix Theorem
>Suppose $V$ is a finite-dimensional complex vector space and $T \in \mathcal{L}(V)$. Then $T$ has an upper-triangular matrix with respect to some basis of $V$.

>[!tips] 5.32 determination of eigenvalues from upper-triangular matrix
>Suppose $T \in \mathcal{L}(V)$ has an upper-triangular matrix with respect to some basis of $V$. Then the eigenvalues of $T$ are precisely the entries on the diagonal of that upper-triangular matrix.

>[!tips] 5.41 conditions for diagonalizability
>Suppose $V$ is finite-dimensional and $T \in \mathcal{L}(V)$. Let $\lambda_1, \dots, \lambda_m$ denote the distinct eigenvalues of $T$. The following are equivalent:
>- $T$ is diagonalizable;
>- $V$ has a basis consisting of eigenvectors of $T$;
>- $V = E(\lambda_1, T) \oplus \dots \oplus E(\lambda_m, T)$;
>- $\dim V = \dim E(\lambda_1, T) + \dots + \dim E(\lambda_m, T)$.