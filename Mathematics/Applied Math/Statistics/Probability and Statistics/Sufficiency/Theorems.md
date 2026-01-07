>[!tips] Theorem 7.1.1 Neyman Factorization Theorem
>The statistic $Y = u(\mathbf{X})$ is sufficient for $\theta$ if and only if the joint pdf/pmf can be factored as:
>$$f(\mathbf{x}; \theta) = k(y; \theta) h(\mathbf{x})$$
>where $k$ depends on $\mathbf{x}$ only through $y$, and $h(\mathbf{x})$ does not depend on $\theta$.

>[!tips] Theorem 7.3.1 Rao-Blackwell Theorem
>Let $\hat{\theta}$ be an unbiased estimator of $\theta$ and $Y$ be a sufficient statistic for $\theta$. Define $\phi(Y) = E(\hat{\theta} | Y)$. Then:
>1. $\phi(Y)$ is an unbiased estimator of $\theta$.
>2. $Var(\phi(Y)) \le Var(\hat{\theta})$.
>Structuring estimators based on sufficient statistics reduces (or maintains) variance.

>[!tips] Theorem 7.3.2 Lehmann-Scheffé Theorem
>If $Y$ is a complete sufficient statistic for $\theta$, and $\phi(Y)$ is an unbiased estimator of $\theta$, then $\phi(Y)$ is the unique Uniformly Minimum Variance Unbiased Estimator (UMVUE) of $\theta$.

>[!tips] Theorem 7.4.1 Basu's Theorem
>If $Y$ is a complete sufficient statistic for $\theta$, and $Z$ is an ancillary statistic, then $Y$ and $Z$ are independent.