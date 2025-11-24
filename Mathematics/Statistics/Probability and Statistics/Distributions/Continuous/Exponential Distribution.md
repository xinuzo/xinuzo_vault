> [!tips] (Definition) Exponential Distribution
> Models waiting time between events in a Poisson process. It is the only continuous distribution with the "memoryless" property. Note: Hogg uses $\theta$ as the mean.
> $$X \sim Exp(\theta)$$
> **P.D.F.:**
> $$f(x) = \frac{1}{\theta}e^{-x/\theta}, \quad 0 < x < \infty$$
> **MGF:**
> $$M(t) = (1-\theta t)^{-1}, \quad t < 1/\theta$$
> **Mean & Variance:**
> $$\mu = \theta, \quad \sigma^2 = \theta^2$$

> [!success]- Proof of $\mu$ and $\sigma^2$
> $$\mu = M'(0) = \left[ -1(1-\theta t)^{-2}(-\theta) \right]_{t=0} = \theta(1)^{-2} = \theta$$
> $$E[X^2] = M''(0) = \left[ -2\theta(1-\theta t)^{-3}(-\theta) \right]_{t=0} = 2\theta^2$$
> $$\sigma^2 = 2\theta^2 - (\theta)^2 = \theta^2$$