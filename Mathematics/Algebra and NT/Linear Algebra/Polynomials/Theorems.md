>[!tips] 4.5 Division Algorithm for Polynomials
>Suppose $p, s \in \mathcal{P}(\mathbf{F})$ and $s \neq 0$. Then there exist unique polynomials $q, r \in \mathcal{P}(\mathbf{F})$ such that
>$$p = sq + r$$
>and $\deg r < \deg s$.

>[!tips] 4.7 each root of a polynomial corresponds to a factor of degree 1
>Suppose $p \in \mathcal{P}(\mathbf{F})$ and $\lambda \in \mathbf{F}$. Then $p(\lambda) = 0$ if and only if there is a polynomial $q \in \mathcal{P}(\mathbf{F})$ such that $p(z) = (z-\lambda)q(z)$ for every $z \in \mathbf{F}$.

>[!tips] 4.8 a polynomial has at most as many roots as its degree
>Suppose $p \in \mathcal{P}(\mathbf{F})$ is a nonzero polynomial. Then $p$ has at most $\deg p$ distinct roots in $\mathbf{F}$.

>[!tips] 4.12 Fundamental Theorem of Algebra
>Every nonconstant polynomial with complex coefficients has a root.

>[!tips] 4.14 Factorization of a polynomial over $\mathbf{C}$
>If $p \in \mathcal{P}(\mathbf{C})$ is a nonconstant polynomial, then $p$ has a unique factorization (except for the order of the factors) of the form
>$$p(z) = c(z-\lambda_1) \dots (z-\lambda_m)$$
>where $c, \lambda_1, \dots, \lambda_m \in \mathbf{C}$.

>[!tips] 4.17 Factorization of a polynomial over $\mathbf{R}$
>If $p \in \mathcal{P}(\mathbf{R})$ is a nonconstant polynomial, then $p$ has a unique factorization (except for the order of the factors) of the form
>$$p(x) = c(x-\lambda_1) \dots (x-\lambda_m)(x^2+b_1x+c_1) \dots (x^2+b_Mx+c_M)$$
>where $c, \lambda_j, b_j, c_j \in \mathbf{R}$ and $b_j^2 < 4c_j$ for each $j$.