
### Problem 1. Brownian Motions
**(a)**
Let $B(t)$ be a standard Brownian motion. For $t > s \ge 0$, we can write $B(t) = B(s) + (B(t) - B(s))$.
* **Expectation:** By the independent increments property, $B(t) - B(s)$ is independent of $B(s)$.
    $$E[B(t) | B(s)] = E[B(s) + (B(t) - B(s)) | B(s)] = B(s) + E[B(t) - B(s)] = B(s) + 0 = B(s)$$
* **Variance:**
    $$Var[B(t) | B(s)] = Var[B(s) + (B(t) - B(s)) | B(s)] = Var[B(t) - B(s)] = t - s$$

**(b)**
Let $X(t) = \mu t + \sigma B(t)$ with $\sigma = 2$. Then $X(t) - X(s) = \mu(t-s) + 2(B(t) - B(s))$.
* **Expectation:**
    $$E[X(t) | X(s)] = X(s) + E[X(t) - X(s)] = X(s) + \mu(t-s)$$
* **Variance:**
    $$Var[X(t) | X(s)] = Var[\mu(t-s) + 2(B(t) - B(s))] = 4 Var[B(t) - B(s)] = 4(t-s)$$

**(c)**
Let $Z = B(t) - B(s)$. We know $Z \sim N(0, t-s)$.
We need to compute $E[\exp(\sigma Z)]$. This is the moment generating function of $Z$ evaluated at $\sigma$.
$$E[e^{\sigma Z}] = e^{\frac{1}{2} \sigma^2 (t-s)}$$

---

### Problem 2. The Brownian Scaling Relation
**(a)**
Let $Y(s) = B(st)$ and $Z(s) = t^{1/2}B(s)$. Both processes are Gaussian with mean zero ($B(0)=0$). We compare their covariance functions.
* **Covariance of LHS:**
    $$E[Y(s_1)Y(s_2)] = E[B(s_1 t)B(s_2 t)] = \min(s_1 t, s_2 t) = t \min(s_1, s_2)$$
* **Covariance of RHS:**
    $$E[Z(s_1)Z(s_2)] = E[t^{1/2}B(s_1) t^{1/2}B(s_2)] = t E[B(s_1)B(s_2)] = t \min(s_1, s_2)$$
Since the mean functions (zero) and covariance functions match, the two processes have the same distribution.

**(b)**
The finite dimensional distributions are determined by the joint normal distribution of the variables. Since the collection $(B(s_1 t), \dots, B(s_n t))$ is a multivariate normal vector with mean zero and covariance matrix entries $t \min(s_i, s_j)$, and the collection $(t^{1/2}B(s_1), \dots, t^{1/2}B(s_n))$ has the exact same mean vector and covariance matrix, their distributions are identical.

---

### Problem 3. Sample Estimators of Diffusion Process
**(a)**
The likelihood function for $Y_i \stackrel{iid}{\sim} N(\mu h, \sigma^2 h)$ is:
$$L(\mu, \sigma^2) = \prod_{i=1}^n \frac{1}{\sqrt{2\pi \sigma^2 h}} \exp\left( -\frac{(y_i - \mu h)^2}{2\sigma^2 h} \right)$$
Taking the log-likelihood $l$:
$$l \propto -\frac{n}{2}\ln(\sigma^2) - \sum_{i=1}^n \frac{(y_i - \mu h)^2}{2\sigma^2 h}$$
* **MLE for $\mu$:** Differentiate w.r.t $\mu$ and set to 0.
    $$\sum \frac{2(y_i - \mu h)h}{2\sigma^2 h} = 0 \implies \sum y_i = n \mu h \implies \hat{\mu} = \frac{1}{nh}\sum_{i=1}^n Y_i$$
* **MLE for $\sigma^2$:** Differentiate w.r.t $\sigma^2$ and set to 0.
    $$-\frac{n}{2\sigma^2} + \frac{1}{2(\sigma^2)^2 h} \sum (y_i - \mu h)^2 = 0 \implies \hat{\sigma}^2 = \frac{1}{nh} \sum_{i=1}^n (Y_i - h\hat{\mu})^2$$

**(b)**
* **Distribution:** $\hat{\mu} = \frac{1}{T} \sum Y_i$. Since $\sum Y_i \sim N(n \mu h, n \sigma^2 h) = N(\mu T, \sigma^2 T)$,
    $$\hat{\mu} \sim N\left(\mu, \frac{\sigma^2}{T}\right)$$
* **Expectation:** $E[\hat{\mu}] = \mu$.
* **Variance:** $Var(\hat{\mu}) = \frac{\sigma^2}{T}$.

**(c)**
* **Distribution:** Note that $\hat{\sigma}^2 = \frac{1}{n} \frac{\sigma^2}{h^{-1}} \sum (\frac{Y_i - \bar{Y}}{\sigma \sqrt{h}})^2$. The sum of squared standardized residuals follows a Chi-squared distribution with $n-1$ degrees of freedom.
    $$\frac{nh \hat{\sigma}^2}{\sigma^2 h} \sim \chi^2_{n-1} \implies \hat{\sigma}^2 \sim \frac{\sigma^2}{n} \chi^2_{n-1}$$
* **Expectation:** $E[\hat{\sigma}^2] = \frac{\sigma^2}{n}(n-1) = \sigma^2 \frac{n-1}{n}$.
* **Variance:** $Var(\hat{\sigma}^2) = (\frac{\sigma^2}{n})^2 2(n-1) = \frac{2\sigma^4(n-1)}{n^2}$.

**(d)**
As $n \to \infty$ on the fixed interval $[0, 1]$ (so $T=1$):
* $\hat{\mu}_n$: The distribution is $N(\mu, \sigma^2)$ for all $n$. It **does not converge to a constant**; it remains a random variable with variance $\sigma^2$.
* $\hat{\sigma}^2_n$: The expectation converges to $\sigma^2$ and the variance converges to 0. By Chebyshev's inequality, $\hat{\sigma}^2_n \xrightarrow{p} \sigma^2$. The limiting distribution is a point mass at $\sigma^2$.

**(e)**
* $\hat{\mu}_n$: **Not weakly consistent.** The variance $\sigma^2/T$ does not go to zero as $n \to \infty$. The probability mass does not concentrate around $\mu$.
* $\hat{\sigma}^2_n$: **Weakly consistent.** As $n \to \infty$, $P(|\hat{\sigma}^2_n - \sigma^2| > \epsilon) \to 0$.

---

### Problem 4. Variable Increments
**(a)**
Likelihood term involves $\exp(-\frac{(y_i - \mu h_i)^2}{2\sigma^2 h_i})$. Minimizing the sum of exponents w.r.t $\mu$:
$$\frac{\partial}{\partial \mu} \sum \frac{(y_i - \mu h_i)^2}{h_i} = -2 \sum (y_i - \mu h_i) = 0$$
$$\sum y_i = \mu \sum h_i \implies \hat{\mu} = \frac{\sum Y_i}{T}$$
**Distribution:** $\sum Y_i \sim N(\mu T, \sigma^2 T)$, so $\hat{\mu} \sim N(\mu, \sigma^2/T)$.

**(b)**
Log-likelihood term is $-\frac{1}{2}\ln(\sigma^2 h_i) - \frac{(y_i - \mu h_i)^2}{2\sigma^2 h_i}$. Summing over $i$:
$$-\frac{n}{2}\ln(\sigma^2) - \text{const} - \frac{1}{2\sigma^2} \sum \frac{(y_i - \mu h_i)^2}{h_i}$$
Solving for $\sigma^2$:
$$\hat{\sigma}^2 = \frac{1}{n} \sum_{i=1}^n \frac{(Y_i - \mu h_i)^2}{h_i}$$
(If substituting $\hat{\mu}$, replace $\mu$ with $\hat{\mu}$).

**(c)**
* **For $\mu$:** The estimator $\hat{\mu} = \frac{X_T - X_0}{T}$ depends only on the endpoints $X_0$ and $X_T$. Intermediate spacings do not affect the formula or the variance ($\sigma^2/T$).
* **For $\sigma^2$:** The estimator explicitly sums the squared standardized increments. While the estimator formula changes (weighting by $1/h_i$), the variance of the estimator depends on $n$ (sample size) but is fundamentally derived from the $\chi^2$ property of the sum of squares, making the variance effectively constant ($2\sigma^4/n$) regardless of specific $h_i$ choices, provided they sum to $T$.

---

### Problem 5. Covariance Stationary AR(2)
**(a)**
Taking expectations of $X_t = \phi_0 + \phi_1 X_{t-1} + \phi_2 X_{t-2} + \eta_t$:
$$\mu = \phi_0 + \phi_1 \mu + \phi_2 \mu + 0 \implies \mu(1 - \phi_1 - \phi_2) = \phi_0 \implies \mu = \frac{\phi_0}{1 - \phi_1 - \phi_2}$$

**(b)**
Let $x_t = X_t - \mu$. Then $x_t = \phi_1 x_{t-1} + \phi_2 x_{t-2} + \eta_t$.
Multiply by $x_{t-k}$ ($k>0$) and take expectations:
$$E[x_t x_{t-k}] = \phi_1 E[x_{t-1} x_{t-k}] + \phi_2 E[x_{t-2} x_{t-k}] + E[\eta_t x_{t-k}]$$
$$\gamma(k) = \phi_1 \gamma(k-1) + \phi_2 \gamma(k-2) \quad (\text{since } E[\eta_t x_{t-k}] = 0 \text{ for } k>0)$$

**(c)**
Divide the equation in (b) by $\gamma(0) = \sigma_X^2$:
$$\rho_k = \phi_1 \rho_{k-1} + \phi_2 \rho_{k-2}$$

**(d)**
Yule-Walker Equations for $k=1, 2$:
1. $\rho_1 = \phi_1 + \phi_2 \rho_1 \implies \rho_1(1-\phi_2) = \phi_1$
2. $\rho_2 = \phi_1 \rho_1 + \phi_2$

Substitute (1) into (2):
$\rho_2 = \rho_1^2(1-\phi_2) + \phi_2 = \rho_1^2 - \rho_1^2 \phi_2 + \phi_2 = \rho_1^2 + \phi_2(1-\rho_1^2)$.
$$\phi_2 = \frac{\rho_2 - \rho_1^2}{1 - \rho_1^2}, \quad \phi_1 = \frac{\rho_1(1-\rho_2)}{1-\rho_1^2}$$

**(e)**
From the system in (d):
$$\rho_1 = \frac{\phi_1}{1-\phi_2}, \quad \rho_2 = \phi_1 \left(\frac{\phi_1}{1-\phi_2}\right) + \phi_2$$

---

### Problem 6. ARMA(1,1)
**(a)**
Take expectations of $X_t - \phi_1 X_{t-1} = \phi_0 + \eta_t + \theta_1 \eta_{t-1}$:
$$\mu - \phi_1 \mu = \phi_0 + 0 + 0 \implies \mu = \frac{\phi_0}{1-\phi_1}$$

**(b)**
Let $x_t = X_t - \mu$. Then $x_t = \phi_1 x_{t-1} + \eta_t + \theta_1 \eta_{t-1}$.
Multiply by $x_t$ and take expectation ($E[x_t \eta_t] = \sigma^2$, $E[x_t \eta_{t-1}] = \phi_1 \sigma^2 + \theta_1 \sigma^2$):
$\gamma_0 = \phi_1 \gamma_1 + \sigma^2 + \theta_1(\phi_1 + \theta_1)\sigma^2$.
Multiply by $x_{t-1}$ and take expectation ($E[x_{t-1}\eta_t]=0$, $E[x_{t-1}\eta_{t-1}]=\sigma^2$):
$\gamma_1 = \phi_1 \gamma_0 + \theta_1 \sigma^2$.
Substituting $\gamma_1$ into $\gamma_0$:
$\gamma_0 = \phi_1(\phi_1 \gamma_0 + \theta_1 \sigma^2) + \sigma^2 (1 + \phi_1 \theta_1 + \theta_1^2)$.
$\gamma_0 (1 - \phi_1^2) = \sigma^2 (1 + \theta_1^2 + 2\phi_1 \theta_1)$.

**(c)**
$\rho_1 = \frac{\gamma_1}{\gamma_0} = \frac{\phi_1 \gamma_0 + \theta_1 \sigma^2}{\gamma_0} = \phi_1 + \frac{\theta_1 \sigma^2}{\gamma_0}$.
For $k > 1$, $x_t$ depends on noise at $t, t-1$. $x_{t-k}$ depends on noise at $t-k$ and prior.
$E[x_t x_{t-k}] = \phi_1 E[x_{t-1} x_{t-k}] + E[\eta_t x_{t-k}] + \theta_1 E[\eta_{t-1} x_{t-k}]$.
For $k > 1$, the noise terms are uncorrelated with $x_{t-k}$.
Thus, $\gamma_k = \phi_1 \gamma_{k-1} \implies \rho_k = \phi_1 \rho_{k-1}$.

**(d)**
* **AR(1):** Decay starts immediately from lag 0 ($\rho_k = \phi_1^k$).
* **ARMA(1,1):** Decay starts from lag 1. $\rho_1$ is determined by both AR and MA parameters, then $\rho_2, \rho_3 \dots$ decay geometrically by $\phi_1$.
* **Economic Interpretation:** An ARMA(1,1) process combines mean reversion (AR) with a specific reaction to the most recent shock (MA). The MA term allows the series to handle "overshooting" or "correction" in the period immediately following a shock before settling into the long-term decay path.

**(e)**
* **MA(1):** Has a "cutoff" property. $\rho_1 \neq 0$, but $\rho_k = 0$ for all $k > 1$.
* **MA(q):** Has a cutoff after lag $q$. $\rho_k = 0$ for all $k > q$.
* **Comparison:** ARMA processes have infinite memory (autocorrelations never reach exactly zero, just decay), whereas MA processes have finite memory (autocorrelations become exactly zero).