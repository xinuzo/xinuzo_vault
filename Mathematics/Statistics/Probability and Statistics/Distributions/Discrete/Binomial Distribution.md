from [[Bernoulli Distribution]],
we can also build **Binomial Distribution**,

> [!tips] (Definition) Binomial Distribution
> Consider a sequence of $n$ independent **Bernoulli trials** with probability of success $p$. Let $X$ be the number of successes in these $n$ trials.
> $$X \sim b(n, p)$$
> **P.M.F.:**
> $$p(x) = \binom{n}{x}p^x(1-p)^{n-x}, \quad x = 0, 1, \dots, n$$
> **MGF:**
> $$M(t) = (1-p+pe^t)^n$$
> **Mean & Variance:**
> $$\mu = np, \quad \sigma^2 = np(1-p)$$

> [!success]- Proof of $\mu$ and $\sigma^2$
> $$\begin{aligned} E[X] &= \sum_{x=0}^n x \binom{n}{x} p^x (1-p)^{n-x} = np \sum_{x=1}^n \binom{n-1}{x-1} p^{x-1} (1-p)^{n-x} \\ &= np (p + (1-p))^{n-1} = np(1) = np \end{aligned}$$
> $$\begin{aligned} E[X(X-1)] &= \sum_{x=0}^n x(x-1) \binom{n}{x} p^x (1-p)^{n-x} = n(n-1)p^2 \sum_{x=2}^n \binom{n-2}{x-2} p^{x-2} (1-p)^{n-x} \\ &= n(n-1)p^2 \end{aligned}$$
> $$\sigma^2 = E[X(X-1)] + E[X] - (E[X])^2 = n(n-1)p^2 + np - (np)^2 = np(1-p)$$