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