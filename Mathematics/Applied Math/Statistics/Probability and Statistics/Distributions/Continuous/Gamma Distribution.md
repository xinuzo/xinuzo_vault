> [!tips] (Definition) Gamma Distribution
> Generalization of the [[Exponential Distribution]]. Models waiting time until the $\alpha$-th event. Let $X$ be random variables that represents a **continuous waiting time** for an event to occur, such as the time until a certain number of events have happened
> $$X \sim \Gamma(\alpha, \theta)$$
> **P.D.F.:**
> $$f(x) = \frac{1}{\Gamma(\alpha)\theta^\alpha} x^{\alpha-1}e^{-x/\theta}, \quad 0 < x < \infty$$
> **MGF:**
> $$M(t) = (1-\theta t)^{-\alpha}, \quad t < 1/\theta$$
> **Mean & Variance:**
> $$\mu = \alpha\theta, \quad \sigma^2 = \alpha\theta^2$$

> [!success]- Proof of $\mu$ and $\sigma^2$
> $$\mu = M'(0) = \left[ -\alpha(1-\theta t)^{-\alpha-1}(-\theta) \right]_{t=0} = \alpha\theta$$
> $$E[X^2] = M''(0) = \left[ (-\alpha)(-\alpha-1)(-\theta)^2 (1-\theta t)^{-\alpha-2} \right]_{t=0} = \alpha(\alpha+1)\theta^2$$
> $$\sigma^2 = \alpha(\alpha+1)\theta^2 - (\alpha\theta)^2 = \alpha\theta^2$$

> [!tips] Theorems: Gamma & Chi-Square
> **Gamma Additivity:**
> If $X_i \sim \Gamma(\alpha_i, \theta)$ are independent (must have same scale $\theta$):
> $$\sum_{i=1}^n X_i \sim \Gamma\left(\sum \alpha_i, \theta\right)$$
> **Chi-Square Relation:**
> $\chi^2(r)$ is a special case of Gamma where $\alpha = r/2$ and $\theta = 2$.
> **Chi-Square Additivity:**
> If $X_i \sim \chi^2(r_i)$ are independent:
> $$\sum_{i=1}^n X_i \sim \chi^2\left(\sum r_i\right)$$

> [!success]- Proof via MGF
> $M_{X_i}(t) = (1-\theta t)^{-\alpha_i}$
> $M_{\sum X}(t) = \prod (1-\theta t)^{-\alpha_i} = (1-\theta t)^{-\sum \alpha_i}$
> For Chi-Square, substitute $\theta=2, \alpha_i = r_i/2$.