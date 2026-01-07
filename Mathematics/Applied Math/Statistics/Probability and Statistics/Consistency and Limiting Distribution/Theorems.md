>[!tips] Theorem 5.1.1 Weak Law of Large Numbers (WLLN)
>Let $X_1, \dots, X_n$ be iid random variables with mean $\mu$ and finite variance $\sigma^2$. Then the sample mean $\bar{X}_n$ converges in probability to $\mu$:
>$$\bar{X}_n \xrightarrow{P} \mu$$

>[!tips] Theorem 5.2.1 Relation of Convergences
>If $X_n \xrightarrow{P} X$, then $X_n \xrightarrow{D} X$.
>The converse is false in general, unless $X$ is a constant (degenerate distribution).

>[!tips] Theorem 5.2.4 Slutsky's Theorem
>Let $X_n \xrightarrow{D} X$ and $Y_n \xrightarrow{P} a$ (where $a$ is a constant). Then:
>1. $X_n + Y_n \xrightarrow{D} X + a$
>2. $X_n Y_n \xrightarrow{D} aX$
>3. $X_n / Y_n \xrightarrow{D} X/a$ (provided $a \ne 0$)

>[!tips] Theorem 5.3.1 Central Limit Theorem (CLT)
>Let $X_1, \dots, X_n$ be iid with mean $\mu$ and finite variance $\sigma^2 > 0$. Then the random variable $W_n = \frac{\bar{X}_n - \mu}{\sigma/\sqrt{n}}$ converges in distribution to a standard normal variable:
>$$W_n \xrightarrow{D} N(0, 1)$$

>[!tips] Theorem 5.3.2 Delta Method
>Let $Y_n$ be a sequence of random variables such that $\sqrt{n}(Y_n - \theta) \xrightarrow{D} N(0, \sigma^2)$. If $g(y)$ is a differentiable function at $\theta$ and $g'(\theta) \ne 0$, then:
>$$\sqrt{n}[g(Y_n) - g(\theta)] \xrightarrow{D} N(0, \sigma^2 [g'(\theta)]^2)$$