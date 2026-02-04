## 18.642 Problem Set 3 Solutions

### Problem 1. Prove Stein's Lemma
**(a)**
Let $f(x)$ be the PDF of $N(\mu, \sigma^2)$. We know that $f'(x) = -\frac{x-\mu}{\sigma^2}f(x)$, which implies $(x-\mu)f(x) = -\sigma^2 f'(x)$.
Using integration by parts with $u = g(x)$ and $dv = -\sigma^2 f'(x) dx$:
$$
\begin{aligned}
E[g(X)(X - \mu)] &= \int_{-\infty}^{\infty} g(x)(x - \mu) f(x) \, dx \\
&= \int_{-\infty}^{\infty} g(x) [-\sigma^2 f'(x)] \, dx \\
&= -\sigma^2 \left[ g(x)f(x) \Big|_{-\infty}^{\infty} - \int_{-\infty}^{\infty} g'(x)f(x) \, dx \right]
\end{aligned}
$$
Assuming $g(x)$ does not grow exponentially, the boundary terms vanish.
$$= \sigma^2 \int_{-\infty}^{\infty} g'(x)f(x) \, dx = \sigma^2 E[g'(X)]$$

**(b)**
Using the hint for the bivariate normal distribution, we can write $Y = a + bX + \epsilon$, where $\epsilon$ is independent of $X$.
$$
\begin{aligned}
Cov[g(X), Y] &= Cov[g(X), a + bX + \epsilon] \\
&= \underbrace{Cov[g(X), a]}_{0} + b \cdot Cov[g(X), X] + \underbrace{Cov[g(X), \epsilon]}_{0} \\
&= b \cdot E[g(X)(X - \mu)] \quad \text{(using property of covariance)}
\end{aligned}
$$
Substituting the result from Part (a):
$$= b \cdot \sigma^2 E[g'(X)]$$
Since $b = \rho\tau/\sigma$ and $Cov(X, Y) = \rho\sigma\tau$, we have $b = \frac{Cov(X,Y)}{\sigma^2}$.
$$= \frac{Cov(X, Y)}{\sigma^2} \cdot \sigma^2 E[g'(X)] = E[g'(X)]Cov(X, Y)$$

---

### Problem 2. Stein's Lemma for Stochastic Volatility
**(a)**
We must verify non-negativity and that it integrates to 1.
* Non-negativity: $q(V) = \frac{V p(V)}{E[V]}$. Since $V > 0$, $p(V) \ge 0$, and $E[V] > 0$, $q(V)$ is non-negative.
* Integration:
    $$\int_0^{\infty} q(V) \, dV = \int_0^{\infty} \frac{V p(V)}{E[V]} \, dV = \frac{1}{E[V]} \underbrace{\int_0^{\infty} V p(V) \, dV}_{E[V]} = 1$$

**(b)**
By the definition of covariance:
$$
\begin{aligned}
Cov[g(X), X] &= E[(g(X) - E[g(X)])(X - E[X])] \\
&= E[g(X)(X - E[X])] - E[g(X)]\underbrace{E[X - E[X]]}_{0} \\
&= E[g(X)(X - E[X])]
\end{aligned}
$$

**(c)**
**Yes.** The transition from (1) to (2) is $E[Z] = E_V[E_{X|V}[Z]]$, where $Z = g(X)(X - E[X])$. This is the Law of Iterated Expectations.

**(d)**
We need to show that $E[X]$ can be replaced by $E[X|V]$.
* Given $X|V \sim N(\mu, \sigma^2 V)$, the conditional mean is $E[X|V] = \mu$.
* The unconditional mean is $E[X] = E_V[E[X|V]] = E_V[\mu] = \mu$.
* Since $E[X] = E[X|V] = \mu$, the terms are identical, and substitution is valid.

**(e)**
**Yes.**
Equation (*) is $Cov[g(X), X] = E \left[ g'(X) \frac{V}{E[V]} \sigma^2 E[V] \right]$.
Equation (**) is $Cov[g(X), X] = E_Q[g'(X)] Var[X]$.
* **Variance Term:** Using the Law of Total Variance, $Var[X] = E[Var(X|V)] + Var(E[X|V]) = E[\sigma^2 V] + 0 = \sigma^2 E[V]$. This matches the $\sigma^2 E[V]$ term in (*).
* **Expectation Term:** The term $\frac{V p(V)}{E[V]}$ inside the expectation in (*) corresponds exactly to the size-biased density $q(V)$. Thus, the expectation under the original measure $P$ weighted by $\frac{V}{E[V]}$ becomes the expectation $E_Q$ under the measure $Q$.
    $$E\left[ g'(X) \frac{V}{E[V]} \right] = \int g'(x) \frac{v p(v)}{E[V]} dv = \int g'(x) q(v) dv = E_Q[g'(X)]$$

---

### Problem 3. Stochastic Process for Asset Price Dynamics
**(a)**
**All values** of $\mu \in (-\infty, \infty)$ and $\sigma^2 > 0$.
The process is defined as $S_{t} = S_{t-1} + X_t$. Since $X_t$ is independent of previous steps, the future state $S_{t+1}$ depends only on the current state $S_t$ and the new step. This satisfies the Markov property regardless of the drift or variance parameters.

**(b)**
**$\mu = 0$**.
For $\{S_t\}$ to be a Martingale, we require $E[S_{t+1} | S_t] = S_t$.
$$E[S_{t+1} | S_t] = E[S_t + X_{t+1} | S_t] = S_t + E[X_{t+1}] = S_t + \mu$$
This equality holds if and only if $\mu = 0$.

**(c)**
**$\mu > 0$**.
This is a first hitting time problem on a symmetric interval $(-0.20, 0.20)$ with starting point $S_0=0$.
* If $\mu = 0$, the random walk is symmetric, and the probability of hitting the upper barrier first is exactly $1/2$.
* If $\mu > 0$, the process has a positive drift ($E[S_t] = \mu t$), making it strictly more likely to hit the positive barrier ($0.20$) before the negative barrier ($-0.20$). Thus $P > 1/2$ requires $\mu > 0$.

---

### Problem 4. Principal Components Analysis of Yields
**(a)**
**No, the difference is not meaningful**.
The eigenvectors are defined by $Av = \lambda v$. If $v$ is a solution, then $-v$ is also a solution with the same eigenvalue. The sign flip affects all elements of the vector simultaneously, preserving the relative structural relationship (i.e., they all move in the same direction). It is purely a matter of mathematical convention.

**(b)**
The range is larger for the **covariance matrix** because it operates on unscaled data.
* **Covariance:** The PC loadings are influenced by the raw variance of the input variables. Yields with higher volatility (variance) will naturally have larger loadings in the first principal component as it seeks to maximize explained variance.
* **Correlation:** The variables are standardized (variance = 1). Since every variable contributes equal variance to the system, no single variable dominates due to scale, leading to a narrower, more uniform range of loadings.

**(c)**
**Interpretation of Correlation PCA:**
* **PC1 (Level):** Loadings are all negative and of similar magnitude ($\approx -0.20$ to $-0.36$). This represents a parallel shift in the yield curve.
* **PC2 (Slope):** Loadings change sign from positive at the short end (DGS3MO: $0.62$) to negative at the long end (DGS20: $-0.33$). This represents a tilting or slope change of the curve.
* **PC3 (Curvature):** Loadings are positive at the extremes (short/long) and negative in the middle. This represents a change in the curvature (convexity) of the yield curve.

**Comparison:** Covariance PC1 loadings are skewed toward the more volatile intermediate/long tenors, while Correlation PC1 treats all tenors more evenly.

**(d)**
Correlation PCA is preferred because it **treats all tenors as equally important**.
In yield curve analysis, short-term rates often have lower volatility than long-term rates. Using covariance PCA would cause the model to focus primarily on the volatile long end, potentially ignoring the structural dynamics of the short end. Correlation PCA standardizes the variances, ensuring the model captures the comovement structure across the entire term structure regardless of volatility differences.

**(e)**
**Total Variance = 9**.
**Yes, it is an integer.**
The Total Variance in PCA is the sum of the eigenvalues, which equals the trace (sum of diagonal elements) of the matrix being decomposed. For a correlation matrix, every diagonal element is 1 (the correlation of a variable with itself). Since there are 9 securities, the trace is $1 \times 9 = 9$.