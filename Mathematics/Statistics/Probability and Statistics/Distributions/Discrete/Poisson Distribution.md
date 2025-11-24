> [!tips] (Definition) Poisson Distribution
> Represents the number of events occurring in a fixed interval of time or space if these events occur with a known constant mean rate $\lambda$ and independently of the time since the last event. It is a limiting form of the Binomial where $n \to \infty, p \to 0, np = \lambda$.
> $$X \sim Poisson(\lambda)$$
> **P.M.F.:**
> $$p(x) = \frac{\lambda^x e^{-\lambda}}{x!}, \quad x = 0, 1, 2, \dots$$
> **MGF:**
> $$M(t) = e^{\lambda(e^t - 1)}$$
> **Mean & Variance:**
> $$\mu = \lambda, \quad \sigma^2 = \lambda$$

> [!success]- Proof of $\mu$ and $\sigma^2$
> $$E[X] = \sum_{x=0}^\infty x \frac{\lambda^x e^{-\lambda}}{x!} = \lambda e^{-\lambda} \sum_{x=1}^\infty \frac{\lambda^{x-1}}{(x-1)!} = \lambda e^{-\lambda} (e^\lambda) = \lambda$$
> $$E[X(X-1)] = \sum_{x=0}^\infty x(x-1) \frac{\lambda^x e^{-\lambda}}{x!} = \lambda^2 e^{-\lambda} \sum_{x=2}^\infty \frac{\lambda^{x-2}}{(x-2)!} = \lambda^2$$
> $$\sigma^2 = E[X^2] - \mu^2 = E[X(X-1)] + E[X] - \mu^2 = \lambda^2 + \lambda - \lambda^2 = \lambda$$