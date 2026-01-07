> [!tips] (Definition) Hypergeometric Distribution
> Used when sampling $n$ items **without replacement** from a population of $N$ items consisting of $N_1$ "successes" and $N_2$ "failures" ($N=N_1+N_2$). $X$ is the number of successes in the sample.
> $$X \sim Hyp(N, N_1, n)$$
> **P.M.F.:**
> $$p(x) = \frac{\binom{N_1}{x}\binom{N-N_1}{n-x}}{\binom{N}{n}}, \quad x \le n, x \le N_1, n-x \le N_2$$
> **Mean & Variance:**
> $$\mu = n\left(\frac{N_1}{N}\right), \quad \sigma^2 = n\left(\frac{N_1}{N}\right)\left(\frac{N-N_1}{N}\right)\left(\frac{N-n}{N-1}\right)$$

> [!success]- Proof of $\mu$ and $\sigma^2$
> $$E[X] = \sum x \frac{\binom{N_1}{x}\binom{N-N_1}{n-x}}{\binom{N}{n}} = n\frac{N_1}{N} \sum \frac{\binom{N_1-1}{x-1}\binom{(N-1)-(N_1-1)}{(n-1)-(x-1)}}{\binom{N-1}{n-1}} = n\frac{N_1}{N}(1)$$
> $$E[X(X-1)] = \sum x(x-1) \frac{\binom{N_1}{x}\binom{N-N_1}{n-x}}{\binom{N}{n}} = n(n-1)\frac{N_1(N_1-1)}{N(N-1)} \sum (\dots) = \frac{n(n-1)N_1(N_1-1)}{N(N-1)}$$
> $$\sigma^2 = E[X(X-1)] + \mu - \mu^2 = \dots (\text{algebraic simplification}) \dots = n\frac{N_1}{N}\frac{N_2}{N}\frac{N-n}{N-1}$$