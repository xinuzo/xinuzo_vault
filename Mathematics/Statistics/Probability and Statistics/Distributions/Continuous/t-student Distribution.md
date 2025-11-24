> [!tips] (Definition) Student's t Distribution
> Arises when estimating the mean of a normally distributed population when the sample size is small and $\sigma$ is unknown. Let $Z \sim N(0,1)$ and $V \sim \chi^2(r)$.
> $$T = \frac{Z}{\sqrt{V/r}} \sim t(r)$$
> **P.D.F.:**
> $$f(t) = \frac{\Gamma((r+1)/2)}{\sqrt{\pi r}\Gamma(r/2)} (1+t^2/r)^{-(r+1)/2}, \quad -\infty < t < \infty$$
> **Mean & Variance:**
> $$\mu = 0 \text{ (if } r>1), \quad \sigma^2 = \frac{r}{r-2} \text{ (if } r>2)$$

> [!success]- Proof of $\mu$ and $\sigma^2$
> $$E[T] = E[Z]E[V^{-1/2}] = 0 \cdot E[V^{-1/2}] = 0$$
> $$E[T^2] = E[Z^2]E[r V^{-1}] = 1 \cdot r \cdot E[V^{-1}] \text{ (using inv-Chi-sq prop)} = r \frac{1}{r-2} = \frac{r}{r-2}$$
> $$\sigma^2 = E[T^2] - E[T]^2 = \frac{r}{r-2}$$

> [!tips] Theorems: Derived Distributions
> **Student's t Definition:**
> If $W \sim N(0, 1)$ and $V \sim \chi^2(r)$ are independent:
> $$T = \frac{W}{\sqrt{V/r}} \sim t(r)$$
> **F-Distribution Definition:**
> If $U \sim \chi^2(r_1)$ and $V \sim \chi^2(r_2)$ are independent:
> $$F = \frac{U/r_1}{V/r_2} \sim F(r_1, r_2)$$
> **Beta from Gamma:**
> If $X_1 \sim \Gamma(\alpha, 1)$ and $X_2 \sim \Gamma(\beta, 1)$ are independent:
> $$Y = \frac{X_1}{X_1 + X_2} \sim Beta(\alpha, \beta)$$