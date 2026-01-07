>[!tips] Theorem 9.1.1 Distribution of Quadratic Forms
>Let $\mathbf{X} \sim N_n(\mathbf{0}, \mathbf{I})$. The quadratic form $\mathbf{X}'\mathbf{A}\mathbf{X}$ follows a $\chi^2(r)$ distribution if and only if $\mathbf{A}$ is idempotent ($\mathbf{A}^2 = \mathbf{A}$) and has rank $r$.

>[!tips] Theorem 9.1.2 Independence of Quadratic Forms
>Let $\mathbf{X} \sim N_n(\mathbf{\mu}, \mathbf{\Sigma})$. Quadratic forms $\mathbf{X}'\mathbf{A}\mathbf{X}$ and $\mathbf{X}'\mathbf{B}\mathbf{X}$ are independent if and only if $\mathbf{A}\mathbf{\Sigma}\mathbf{B} = \mathbf{0}$.
>(Craig's Theorem).

>[!tips] Theorem 9.2.1 ANOVA F-Test
>Under $H_0: \mu_1 = \dots = \mu_k$, the statistic:
>$$F = \frac{SSB / (k-1)}{SSW / (N-k)}$$
>follows an $F$-distribution with degrees of freedom $k-1$ and $N-k$.