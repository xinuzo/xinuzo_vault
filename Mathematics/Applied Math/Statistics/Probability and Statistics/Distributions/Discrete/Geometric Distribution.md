> [!tips] (Definition) Geometric Distribution
> Consider a sequence of independent Bernoulli trials with probability of success $p$. Let $X$ be the number of trials needed to observe the **first** success.
> $$X \sim Geo(p)$$
> **P.M.F.:**
> $$p(x) = p(1-p)^{x-1}, \quad x = 1, 2, 3, \dots$$
> **MGF:**
> $$M(t) = \frac{pe^t}{1-(1-p)e^t}, \quad t < -\ln(1-p)$$
> **Mean & Variance:**
> $$\mu = \frac{1}{p}, \quad \sigma^2 = \frac{1-p}{p^2}$$

> [!success]- Proof of $\mu$ and $\sigma^2$
> Let $q = 1-p$. Recall the geometric series $\sum_{x=0}^\infty q^x = (1-q)^{-1}$.
> Differentiate w.r.t $q$: $\sum_{x=1}^\infty x q^{x-1} = (1-q)^{-2}$.
> $$\mu = E[X] = \sum_{x=1}^\infty x p q^{x-1} = p(1-q)^{-2} = p(p^{-2}) = \frac{1}{p}$$
> Differentiate again: $\sum_{x=2}^\infty x(x-1) q^{x-2} = 2(1-q)^{-3}$.
> $$E[X(X-1)] = \sum_{x=1}^\infty x(x-1) p q^{x-1} = pq \sum_{x=2}^\infty x(x-1) q^{x-2} = pq(2p^{-3}) = \frac{2q}{p^2}$$
> $$\sigma^2 = E[X(X-1)] + E[X] - (E[X])^2 = \frac{2(1-p)}{p^2} + \frac{1}{p} - \frac{1}{p^2} = \frac{1-p}{p^2}$$