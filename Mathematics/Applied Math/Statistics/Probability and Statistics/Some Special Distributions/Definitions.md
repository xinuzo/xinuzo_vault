>[!tips] 3.1 Bernoulli and Binomial Distributions
>A Bernoulli trial has two outcomes: success (probability $p$) and failure ($1-p$).
>If $X$ is the number of successes in $n$ independent Bernoulli trials, $X$ has a Binomial distribution, $b(n, p)$.
>[cite_start]$$p(x) = \binom{n}{x} p^x (1-p)^{n-x}, \quad x = 0, 1, ..., n$$ [cite: 40]

>[!tips] 3.1 Geometric Distribution
>The number of failures $Y$ until the first success in a sequence of Bernoulli trials follows a Geometric distribution.
>[cite_start]$$p(y) = p(1-p)^y, \quad y = 0, 1, 2, ...$$ [cite: 40]

>[!tips] 3.2 Poisson Distribution
>A random variable $X$ has a Poisson distribution with parameter $\lambda > 0$ if:
>[cite_start]$$p(x) = \frac{\lambda^x e^{-\lambda}}{x!}, \quad x = 0, 1, 2, ...$$ [cite: 3]

>[!tips] 3.3 Gamma Distribution
>The pdf of a Gamma random variable with parameters $\alpha > 0$ and $\beta > 0$ is:
>[cite_start]$$f(x) = \frac{1}{\Gamma(\alpha)\beta^\alpha} x^{\alpha-1} e^{-x/\beta}, \quad 0 < x < \infty$$ [cite: 42]

>[!tips] 3.3 Chi-square Distribution
>A special case of the Gamma distribution where $\alpha = r/2$ and $\beta = 2$. [cite_start]It is denoted as $\chi^2(r)$, where $r$ is the degrees of freedom. [cite: 42]

>[!tips] 3.4 Normal Distribution
>A random variable $X$ has a Normal distribution $N(\mu, \sigma^2)$ if its pdf is:
>[cite_start]$$f(x) = \frac{1}{\sigma\sqrt{2\pi}} \exp\left[ -\frac{1}{2} \left( \frac{x-\mu}{\sigma} \right)^2 \right], \quad -\infty < x < \infty$$ [cite: 45]

>[!tips] 3.5 Bivariate Normal Distribution
>The pdf of a bivariate normal distribution involves means $\mu_1, \mu_2$, variances $\sigma_1^2, \sigma_2^2$, and correlation $\rho$.
>$$f(x, y) = \frac{1}{2\pi\sigma_1\sigma_2\sqrt{1-\rho^2}} \exp\left( -\frac{q}{2} \right)$$
>[cite_start]where $q$ is the quadratic form in the exponent. [cite: 48]

>[!tips] 3.6 t-Distribution
>[cite_start]If $W \sim N(0, 1)$ and $V \sim \chi^2(r)$ are independent, then $T = \frac{W}{\sqrt{V/r}}$ has a t-distribution with $r$ degrees of freedom. [cite: 53]

>[!tips] 3.6 F-Distribution
>[cite_start]If $U \sim \chi^2(r_1)$ and $V \sim \chi^2(r_2)$ are independent, then $F = \frac{U/r_1}{V/r_2}$ has an F-distribution with degrees of freedom $r_1$ and $r_2$. [cite: 53]