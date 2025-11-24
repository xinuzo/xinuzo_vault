> [!tips] (Definition) Gamma Distribution
> Generalization of the Exponential. Models waiting time until the $\alpha$-th event.
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