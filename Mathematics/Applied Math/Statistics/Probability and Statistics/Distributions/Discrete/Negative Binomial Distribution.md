> [!tips] (Definition) Negative Binomial Distribution
> The number of independent Bernoulli trials ($X$) needed to achieve the **$r$-th** success.
> $$X \sim NB(r, p)$$
> **P.M.F.:**
> $$p(x) = \binom{x-1}{r-1}p^r(1-p)^{x-r}, \quad x = r, r+1, \dots$$
> **MGF:**
> $$M(t) = \left( \frac{pe^t}{1-(1-p)e^t} \right)^r$$
> **Mean & Variance:**
> $$\mu = \frac{r}{p}, \quad \sigma^2 = \frac{r(1-p)}{p^2}$$

> [!success]- Proof of $\mu$ and $\sigma^2$
> Let $X = Y_1 + \dots + Y_r$ where $Y_i \sim Geo(p)$ (independent).
> $$E[X] = \sum_{i=1}^r E[Y_i] = \sum_{i=1}^r \frac{1}{p} = \frac{r}{p}$$
> $$Var(X) = \sum_{i=1}^r Var(Y_i) = \sum_{i=1}^r \frac{1-p}{p^2} = \frac{r(1-p)}{p^2}$$