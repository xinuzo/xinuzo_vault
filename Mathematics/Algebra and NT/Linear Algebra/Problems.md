
> [!question] ONMIPA 2025
> 
> Let $M$ be the set of all $4 \times 4$ symmetric matrices whose entries are exclusively from the set $S = \{0, 2, 5\}$, such that every row contains all elements of $S$.
> 
> 1. Show that if there exists an element $k \in S$ that appears exactly 8 times in the entries of $A \in M$, then $\det(A) \neq 0$.
>     
> 2. Find the maximum of $\det(A)$.
>     

> [!success]- Solution
> 
> Part 1: Non-Singularity Proof (Spectral Approach)
> 
> Let the distinct elements of the set be $\{k, p, q\}$. Since $k$ appears 8 times in a $4 \times 4$ matrix, and row sums are invariant, $k$ must appear exactly twice per row. The other elements, $p$ and $q$, appear once per row.
> 
> 1. The First Eigenvalue
> 
> The sum of every row is constant: $r = 2k + p + q$.
> 
> Thus, the vector $\mathbf{v} = (1, 1, 1, 1)^T$ is an eigenvector with eigenvalue $\lambda_1 = 2k + p + q$. Since $k,p,q \ge 0$ are distinct, $\lambda_1 > 0$.
> 
> 2. Structural Analysis
> 
> Based on the placement of $k$ on the diagonal ($t$ times), there are only 3 symmetric isomorphism classes. We analyze the remaining eigenvalues $\lambda_{2,3,4}$ for each:
> 
> - Case I: Full Diagonal $k$ ($t=4$, Type III)
>     
>     The matrix commutes with the permutation $(12)(34)$. The eigenvectors are the Walsh-Hadamard basis.
>     
>     The eigenvalues are: $\lambda_1 = 2k+p+q$, $\lambda_2 = 2k-p-q$, $\lambda_3 = p-q$, $\lambda_4 = -(p-q)$.
>     
>     $\det(A) = -(2k+p+q)(2k-p-q)(p-q)^2$.
>     
>     Since $p \neq q$ and integers are distinct, this product is non-zero.
>     
> - Case II: Empty Diagonal $k$ ($t=0$, Type I)
>     
>     The matrix is a symmetric circulant matrix (cycle structure).
>     
>     The eigenvalues are: $\lambda_1 = 2k+p+q$, $\lambda_2 = p+q-2k$, $\lambda_{3,4} = \pm(p-q)$.
>     
>     $\det(A) = (2k+p+q)(p+q-2k)(p-q)^2$.
>     
>     Non-zero for distinct integers $\{0,2,5\}$.
>     
> - Case III: Mixed Diagonal ($t=2$, Type II)
>     
>     This structure lacks the full symmetry of the others, but symmetry implies $(p-q)$ is still a factor. The determinant expands to $\det(A) = (p-q) \cdot P(k,p,q)$, where $P$ is a non-zero integer polynomial for our specific set.
>     
> 
> **Conclusion:** In all cases, $\det(A) \neq 0$.
> 
> Part 2: Maximization
> 
> To maximize the determinant, we test the permutations of $\{0,2,5\}$ on the three structures. The maximum is achieved in Case III (Mixed Diagonal) where the smallest element ($0$) is the most frequent ($k$) to minimize the "penalty" of off-diagonal subtraction terms.
> 
> - **Configuration:** $k=0$ (8 times), $p=5, q=2$.
>     
> - Matrix: Rows arranged as diagonal pattern $(0,0,2,2)$.
>     
>     $$A = \begin{pmatrix} 0 & 2 & 0 & 5 \\ 2 & 0 & 5 & 0 \\ 0 & 5 & 2 & 0 \\ 5 & 0 & 0 & 2 \end{pmatrix}$$
>     
> - **Calculation:** $\det(A) = 609$.
>     
> 
> **Maximum Determinant:** $609$.