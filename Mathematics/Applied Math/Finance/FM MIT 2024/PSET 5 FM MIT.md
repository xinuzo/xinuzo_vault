## 18.642 Problem Set 5 Solutions

### Problem 1. Brownian Motion as a Levy Process
**(a) Prove that $\{W(t)\}$ is a Levy Process.**

Let $W(t) = \mu t + \sigma B(t)$, where $B(t)$ is a standard Brownian Motion. [cite_start]We verify the four conditions of the definition [cite: 1109-1115]:

1.  **$L(0)=0$:**
    $W(0) = \mu(0) + \sigma B(0) = 0 + 0 = 0$. Condition satisfied.

2.  **Stationary Increments:**
    For $s \le t$, consider the increment $W(t) - W(s) = \mu(t-s) + \sigma(B(t) - B(s))$.
    Since $B(t) - B(s) \sim N(0, t-s)$, the increment follows a Normal distribution:
    $$W(t) - W(s) \sim N(\mu(t-s), \sigma^2(t-s))$$
    This distribution depends only on the time difference $\tau = t-s$. Thus, $W(t) - W(s) \stackrel{d}{=} W(t-s)$. Condition satisfied.

3.  **Independent Increments:**
    Let $(s, t)$ and $(u, v)$ be disjoint intervals. The increments of $W$ are linear transformations of the increments of $B$:
    $W(t) - W(s) = \mu(t-s) + \sigma(B(t) - B(s))$
    $W(v) - W(u) = \mu(v-u) + \sigma(B(v) - B(u))$
    Since standard Brownian Motion $B(t)$ has independent increments on disjoint intervals, the increments of $W(t)$ are also independent. Condition satisfied.

4.  **Continuity in Probability:**
    We need to show $\lim_{s \to t} P(|W(t) - W(s)| > \epsilon) = 0$.
    Recall that Brownian Motion paths are continuous almost surely. Almost sure continuity implies convergence in probability.
    Explicitly, using Chebyshev's inequality:
    $$P(|W(t) - W(s)| > \epsilon) \le \frac{E[(W(t)-W(s))^2]}{\epsilon^2} = \frac{\mu^2(t-s)^2 + \sigma^2|t-s|}{\epsilon^2}$$
    As $s \to t$, the numerator goes to 0. Thus the limit is 0. Condition satisfied.

---

### Problem 2. Poisson Process as a Levy Process
**(a) Prove that $\{N(t)\}$ is a Levy Process.**

[cite_start]We verify the four conditions for the Poisson process with rate $\lambda$ [cite: 1127-1128]:

1.  **$L(0)=0$:**
    By definition of the Poisson process, $N(0)=0$. Condition satisfied.

2.  **Stationary Increments:**
    [cite_start]The problem statement explicitly defines that $N(t) - N(s)$ follows a Poisson distribution with parameter $\lambda(t-s)$[cite: 1128].
    Since the parameter depends only on the length of the interval $t-s$, the distribution is stationary. Condition satisfied.

3.  **Independent Increments:**
    [cite_start]The problem statement explicitly defines that for any disjoint intervals, the increments are independent[cite: 1127]. Condition satisfied.

4.  **Continuity in Probability:**
    We must show $\lim_{s \to t} P(|N(t) - N(s)| > \epsilon) = 0$.
    Since $N(t)$ takes integer values, for any $\epsilon < 1$, the event $|N(t) - N(s)| > \epsilon$ is equivalent to $|N(t) - N(s)| \ge 1$ (i.e., at least one jump occurred).
    $$P(|N(t) - N(s)| \ge 1) = 1 - P(N(t) - N(s) = 0)$$
    Using the Poisson probability mass function $P(X=k) = e^{-\Lambda}\frac{\Lambda^k}{k!}$ with $\Lambda = \lambda|t-s|$:
    $$P(N(t) - N(s) = 0) = e^{-\lambda|t-s|}$$
    Therefore:
    $$\lim_{s \to t} (1 - e^{-\lambda|t-s|}) = 1 - e^0 = 0$$
    Condition satisfied.