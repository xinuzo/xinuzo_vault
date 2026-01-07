>[!tips] Definition 2.1.1 (Random Vector). 
>Given a random experiment with a sample space $C$, consider two random variables $X_{1}$ and $X_{2}$, which assign to each element $c$ of $C$ **one and only one** ordered pair of numbers $X_{1}(c) = x_{1}$ , $X_{2}(c) = x_{2}$. Then  $(X_{1}, X_{2})$ is a random vector. The space of $(X_{}{1}, X_{2})$ is the set of ordered pairs $D = {(x_{1}, x_{2}) : x_{1} = X_{1}(c), x_{2} = X_{2}(c), c ∈ C}$.

> [!success]- Proof
> This is an application of the **Inclusion-Exclusion Principle** on the geometry of the probability plane.
> 
> Let the total region up to point $(b_1, b_2)$ be represented by $F(b_1, b_2)$. We want to find the probability of the rectangle defined by $a_1 < X_1 < b_1$ and $a_2 < X_2 < b_2$.
> 
> 1.  **Start** with the total area up to the top-right corner: $F(b_1, b_2)$.
> 2.  **Subtract** the area to the left of $a_1$: $F(a_1, b_2)$.
> 3.  **Subtract** the area below $a_2$: $F(b_1, a_2)$.
> 4.  **Add back** the bottom-left corner $F(a_1, a_2)$, because it was subtracted twice (once in step 2 and once in step 3).
> 
> $$P(\text{Rectangle}) = \text{Total} - \text{Left} - \text{Bottom} + \text{Overlap}$$
> $$P = F(b_1, b_2) - F(a_1, b_2) - F(b_1, a_2) + F(a_1, a_2)$$

> [!tips] Theorem: Linear Combinations of Random Variables
> Let $T = \sum_{i=1}^n a_i X_i$ be a linear combination of random variables.
> 
> **Linearity of Expectation:**
> Regardless of independence:
> $$E[T] = \sum_{i=1}^n a_i E[X_i]$$
> **Variance:**
> If $X_1, \dots, X_n$ are **independent**:
> $$Var(T) = \sum_{i=1}^n a_i^2 Var(X_i)$$

> [!success]- Derivation via Covariance
> Generally, $Var(\sum a_i X_i) = \sum a_i^2 Var(X_i) + 2 \sum_{i<j} a_i a_j Cov(X_i, X_j)$.
> If independent, $Cov(X_i, X_j) = 0$, leaving only the sum of variances.