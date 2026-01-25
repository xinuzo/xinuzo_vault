
> [!question] 25/01/2026
> Let $A, B \in M_n(\mathbb{R})$ satisfy $A + B = I_n$ and $\operatorname{rank} A + \operatorname{rank} B = n$. Prove that $A^2 = A$, $B^2 = B$, and $AB = BA = O$.

> [!success]- Solution
> We first establish that the kernel of $A$ and the image of $B$ are the same subspace. By the Rank-Nullity Theorem, the dimension of $\ker A$ is $n - \operatorname{rank} A$. Using the given condition $\operatorname{rank} A + \operatorname{rank} B = n$, this equals $\operatorname{rank} B$, so $\dim(\ker A) = \dim(\operatorname{im} B)$. Next, for any vector $x \in \ker A$, we have $Ax=0$. Using the identity $x = (A+B)x = Ax + Bx = Bx$, we see that $x$ lies in the image of $B$. Since $\ker A \subseteq \operatorname{im} B$ and they have the same finite dimension, they must be equal.
> 
> To prove the product is zero, consider any vector $y$. The vector $By$ is in $\operatorname{im} B$, which we just proved is $\ker A$. Therefore, $A(By) = 0$ for all $y$, implying $AB = O$. Substituting $B = I - A$ into this equation gives $A(I - A) = 0$, which simplifies to $A = A^2$. By symmetry, $BA = O$ and $B = B^2$.
> 
> [Link to source discussion](https://artofproblemsolving.com/community/c7h3757255_matrix_problem)

#linear-algebra #matrix #rank-nullity