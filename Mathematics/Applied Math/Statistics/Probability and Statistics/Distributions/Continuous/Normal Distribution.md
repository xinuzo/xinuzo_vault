> [!tips] (Definition) Normal Distribution
> Describes many natural phenomena (via Central Limit Theorem). Bell-shaped, symmetric.
> $$X \sim N(\mu, \sigma^2)$$
> **P.D.F.:**
> $$f(x) = \frac{1}{\sigma\sqrt{2\pi}} e^{-(x-\mu)^2/2\sigma^2}, \quad -\infty < x < \infty$$
> **MGF:**
> $$M(t) = e^{\mu t + \frac{1}{2}\sigma^2 t^2}$$
> **Mean & Variance:**
> $$\mu = \mu, \quad \sigma^2 = \sigma^2$$

> [!success]- Proof of $\mu$ and $\sigma^2$
> Let $Z \sim N(0,1)$ where $X = \sigma Z + \mu$.
> $$E[Z] = \int_{-\infty}^{\infty} z \frac{1}{\sqrt{2\pi}}e^{-z^2/2} dz = 0 \quad \text{(odd function)} \implies E[X] = \sigma(0) + \mu = \mu$$
> $$Var(Z) = \int_{-\infty}^{\infty} z^2 \frac{1}{\sqrt{2\pi}}e^{-z^2/2} dz = \int z (-f'(z)) dz = [-zf(z)] + \int f(z) dz = 1$$
> $$Var(X) = Var(\sigma Z + \mu) = \sigma^2 Var(Z) = \sigma^2$$

> [!tips] Theorems: Sample Statistics (Normal)
> Let $X_1, \dots, X_n$ be a random sample from $N(\mu, \sigma^2)$.
> **Independence:**
> The sample mean $\bar{X}$ and sample variance $S^2$ are **independent**.
> **Distribution of Sample Mean:**
> $$\bar{X} \sim N(\mu, \sigma^2/n)$$
> **Distribution of Sample Variance:**
> $$\frac{(n-1)S^2}{\sigma^2} \sim \chi^2(n-1)$$

> [!tips] Theorems: Normal Distribution
> **Sum of Normals:**
> If $X_i \sim N(\mu_i, \sigma_i^2)$ are independent, $Y = \sum a_i X_i$ is Normal:
> $$\mu_Y = \sum a_i \mu_i, \quad \sigma_Y^2 = \sum a_i^2 \sigma_i^2$$
> **Square of Standard Normal:**
> If $Z \sim N(0, 1)$, then:
> $$Z^2 \sim \chi^2(1)$$
> **Sum of Squares:**
> If $Z_1, \dots, Z_n$ are i.i.d. $N(0, 1)$, then:
> $$\sum_{i=1}^n Z_i^2 \sim \chi^2(n)$$