> [!tips] (Definition) Chi-Square Distribution
> A special case of [[Gamma Distribution]] where $\alpha=r/2$ and $\theta=2$. If $Z_i \sim N(0,1)$, then $\sum_{i=1}^r Z_i^2 \sim \chi^2(r)$.
> $$X \sim \chi^2(r)$$
> **P.D.F.:**
> $$f(x) = \frac{1}{\Gamma(r/2)2^{r/2}}x^{r/2-1}e^{-x/2}, \quad 0 < x < \infty$$
> **MGF:**
> $$M(t) = (1-2t)^{-r/2}, \quad t < 1/2$$
> **Mean & Variance:**
> $$\mu = r, \quad \sigma^2 = 2r$$

> [!success]- Proof of $\mu$ and $\sigma^2$
> From Gamma moments with $\alpha=r/2, \theta=2$:
> $$\mu = \alpha\theta = (r/2)(2) = r$$
> $$\sigma^2 = \alpha\theta^2 = (r/2)(2^2) = 2r$$