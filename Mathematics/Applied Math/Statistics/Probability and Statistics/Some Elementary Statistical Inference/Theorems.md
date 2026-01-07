>[!tips] Theorem 4.1.1 Unbiasedness of Sample Mean and Variance
>Let $X_1, ..., X_n$ be a random sample from a distribution with mean $\mu$ and variance $\sigma^2$.
>Then $E(\bar{X}) = \mu$ and $E(S^2) = \sigma^2$. (Sample variance $S^2$ is defined with divisor $n-1$)[cite_start]. [cite: 39]

>[!tips] Theorem 4.2.1 Confidence Interval for Mean (Normal, known $\sigma$)
>If $\bar{X}$ is the mean of a random sample of size $n$ from $N(\mu, \sigma^2)$ with known $\sigma$, a $(1-\alpha)100\%$ confidence interval for $\mu$ is:
>[cite_start]$$[\bar{x} - z_{\alpha/2}\frac{\sigma}{\sqrt{n}}, \bar{x} + z_{\alpha/2}\frac{\sigma}{\sqrt{n}}]$$ [cite: 92]

>[!tips] Theorem 4.4.1 pdf of Order Statistics
>For a random sample from a continuous distribution with pdf $f(x)$ and cdf $F(x)$, the pdf of the $k$-th order statistic $Y_k$ is:
>[cite_start]$$g_k(y) = \frac{n!}{(k-1)!(n-k)!} [F(y)]^{k-1} [1-F(y)]^{n-k} f(y)$$ [cite: 92]

>[!tips] Theorem 4.5.1 Power Function
>The power function of a test is the probability of rejecting $H_0$ as a function of the parameter $\theta$.
>Power($\theta$) = $P(\text{Reject } H_0 ; \theta)$.
>[cite_start]Ideally, Power($\theta$) should be small when $\theta \in H_0$ and large when $\theta \in H_1$. [cite: 92]