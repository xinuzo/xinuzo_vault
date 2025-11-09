

>[!tips] Theorem: Linear Independence of Eigenvectors
>If $v_1, v_2, \dots, v_k$ are eigenvectors of a matrix $A$ corresponding to **distinct** eigenvalues $\lambda_1, \lambda_2, \dots, \lambda_k$, then the set $\{v_1, v_2, \dots, v_k\}$ is linearly independent.

>[!success]- Proof
>The proof will proceed by induction on $k$, the number of eigenvectors.
>
>**1. Base Case (for k=1):**
>For $k=1$, we have the set $\{v_1\}$. By definition, an eigenvector cannot be the zero vector ($v_1 \neq \mathbf{0}$). Any set containing a single non-zero vector is automatically linearly independent, as the only solution to the equation $c_1v_1 = \mathbf{0}$ is $c_1=0$. Thus, the statement is true for $k=1$.
>
>**2. Induction Hypothesis:**
>Assume that the statement is true for $k-1$. That is, we assume that *any* set of $k-1$ eigenvectors corresponding to distinct eigenvalues is linearly independent.
>
>**3. Inductive Step (for k):**
>Now, we must prove that the statement is also true for $k$. Consider a set $\{v_1, v_2, \dots, v_k\}$ of $k$ eigenvectors with distinct eigenvalues $\lambda_1, \lambda_2, \dots, \lambda_k$.
>
>Suppose there is a linear combination of these vectors that equals the zero vector:
>$$c_1v_1 + c_2v_2 + \dots + c_kv_k = \mathbf{0} \quad \quad (*)$$
>
>Multiply both sides of equation $(*)$ by the matrix $A$ from the left:
>$A(c_1v_1 + c_2v_2 + \dots + c_kv_k) = A(\mathbf{0})$
>$c_1(Av_1) + c_2(Av_2) + \dots + c_k(Av_k) = \mathbf{0}$
>
>Since $Av_i = \lambda_i v_i$, we can substitute:
>$$c_1\lambda_1v_1 + c_2\lambda_2v_2 + \dots + c_k\lambda_kv_k = \mathbf{0} \quad \quad (**)$$
>
>Next, multiply both sides of the original equation $(*)$ by the scalar $\lambda_k$:
>$$c_1\lambda_kv_1 + c_2\lambda_kv_2 + \dots + c_k\lambda_kv_k = \mathbf{0} \quad \quad (***)$$
>
>Now, subtract equation $(***)$ from equation $(**)$:
>$(c_1\lambda_1v_1 - c_1\lambda_kv_1) + \dots + (c_{k-1}\lambda_{k-1}v_{k-1} - c_{k-1}\lambda_kv_{k-1}) + (c_k\lambda_kv_k - c_k\lambda_kv_k) = \mathbf{0}$
>
>By factoring, we obtain a linear combination of $k-1$ vectors:
>$$c_1(\lambda_1 - \lambda_k)v_1 + c_2(\lambda_2 - \lambda_k)v_2 + \dots + c_{k-1}(\lambda_{k-1} - \lambda_k)v_{k-1} = \mathbf{0}$$
>
>By our **Induction Hypothesis**, the set $\{v_1, v_2, \dots, v_{k-1}\}$ is linearly independent. The only way a linear combination of linearly independent vectors can equal zero is if all coefficients are zero. Thus:
>$c_1(\lambda_1 - \lambda_k) = 0$
>$c_2(\lambda_2 - \lambda_k) = 0$
>$\vdots$
>$c_{k-1}(\lambda_{k-1} - \lambda_k) = 0$
>
>Since all eigenvalues are **distinct**, we know that $(\lambda_i - \lambda_k) \neq 0$ for $i < k$. This forces all the scalars $c_i$ to be zero:
>$$c_1=0, \ c_2=0, \ \dots, \ c_{k-1}=0$$
>
>Substitute these zero values back into the original equation $(*)$:
>$(0)v_1 + (0)v_2 + \dots + (0)v_{k-1} + c_kv_k = \mathbf{0}$
>$c_kv_k = \mathbf{0}$
>
>Since $v_k$ is an eigenvector, $v_k \neq \mathbf{0}$. The only way for $c_kv_k = \mathbf{0}$ is if $c_k = 0$.
>
>We have shown that all scalars $c_1, c_2, \dots, c_k$ must be zero. By the definition of linear independence, this proves that the set $\{v_1, v_2, \dots, v_k\}$ is linearly independent.
>
>By the principle of mathematical induction, the theorem is proven.


>[!tips] Theorem: Eigenvalues, Trace, and Determinant
>For any $n \times n$ matrix $A$ with eigenvalues $\lambda_1, \lambda_2, \dots, \lambda_n$ (counted with multiplicity):
>1. The **determinant** of $A$ is the product of its eigenvalues: $\det(A) = \prod_{i=1}^{n} \lambda_i$.
>2. The **trace** of $A$ is the sum of its eigenvalues: $\text{tr}(A) = \sum_{i=1}^{n} \lambda_i$.

>[!tips] Theorem: The Diagonalization Theorem
>An $n \times n$ matrix $A$ is **diagonalizable** if and only if $A$ has $n$ linearly independent eigenvectors.
>
>Equivalently, $A$ is diagonalizable if and only if for every eigenvalue $\lambda$, the **geometric multiplicity** (dimension of the eigenspace) is equal to its **algebraic multiplicity** (multiplicity as a root of the characteristic polynomial).

>[!tips] Theorem: The Spectral Theorem for Real Symmetric Matrices
>If $A$ is a real symmetric matrix ($A = A^T$), then it is **orthogonally diagonalizable**. This means there exists an orthogonal matrix $P$ ($P^{-1} = P^T$) and a diagonal matrix $D$ such that $A = PDP^T$.
>
>This implies two major properties:
>1. All eigenvalues of a real symmetric matrix are **real numbers**.
>2. Eigenvectors corresponding to distinct eigenvalues are **orthogonal**.

>[!tips] Theorem: Eigenvalues of an Invertible Matrix
>A square matrix $A$ is **invertible** if and only if $\lambda = 0$ is **not** an eigenvalue of $A$.
>
>If $A$ is invertible with eigenvalue $\lambda$ and corresponding eigenvector $v$, then its inverse $A^{-1}$ has eigenvalue $\frac{1}{\lambda}$ with the same eigenvector $v$.

>[!tips] Theorem: The Cayley-Hamilton Theorem
>Every square matrix satisfies its own characteristic equation.
>
>If the characteristic polynomial of a matrix $A$ is $p(\lambda) = \det(A - \lambda I) = c_n \lambda^n + \dots + c_1 \lambda + c_0$, then substituting the matrix $A$ into the polynomial yields the zero matrix:
>$$p(A) = c_n A^n + \dots + c_1 A + c_0 I = \mathbf{0}$$
>This powerful theorem allows one to express high powers of a matrix in terms of lower powers, and it is fundamental in many areas of linear algebra.