>[!tips] 9.1 Quadratic Form
>Let $\mathbf{X}$ be an $n$-dimensional random vector and $\mathbf{A}$ be a symmetric $n \times n$ real matrix. The scalar random variable $Q = \mathbf{X}'\mathbf{A}\mathbf{X} = \sum_{i=1}^n \sum_{j=1}^n a_{ij} X_i X_j$ is called a quadratic form in $\mathbf{X}$.

>[!tips] 9.1 Noncentral Chi-square
>If $X_i \sim N(\mu_i, 1)$ are independent, then $Y = \sum X_i^2$ has a noncentral chi-square distribution $\chi^2(n, \theta)$ with noncentrality parameter $\theta = \frac{1}{2} \sum \mu_i^2$.

>[!tips] 9.2 One-Way ANOVA
>Analysis of Variance (ANOVA) tests the equality of means across $k$ independent normal populations.
>Model: $X_{ij} = \mu_i + e_{ij}$, where $e_{ij} \sim N(0, \sigma^2)$.
>$H_0: \mu_1 = \mu_2 = \dots = \mu_k$.

>[!tips] 9.2 Variation Decomposition
>$SST = SSB + SSW$
>- **SST (Total Sum of Squares)**: $\sum \sum (X_{ij} - \bar{X}_{..})^2$
>- **SSB (Between Group SS)**: $\sum n_i (\bar{X}_{i.} - \bar{X}_{..})^2$
>- **SSW (Within Group SS)**: $\sum \sum (X_{ij} - \bar{X}_{i.})^2$

>[!tips] 9.3 Multiple Comparisons
>Methods to determine which specific means differ after rejecting $H_0$ in ANOVA (e.g., Tukey-Kramer, Bonferroni).