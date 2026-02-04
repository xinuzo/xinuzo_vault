## Problem 1: Prove Stein's Lemma

### Part 1: Proving $E[g(X)(X - \mu)] = \sigma^2 E[g'(X)]$
We use integration by parts. Let $f(x)$ be the PDF of $N(\mu, \sigma^2)$.
Recall that $f'(x) = -\frac{x-\mu}{\sigma^2}f(x)$, which implies $(x-\mu)f(x) = -\sigma^2 f'(x)$.

$$
\begin{aligned}
E[g(X)(X - \mu)] &= \int_{-\infty}^{\infty} g(x)(x - \mu) f(x) \, dx \\
&= \int_{-\infty}^{\infty} g(x) [-\sigma^2 f'(x)] \, dx \\
&= -\sigma^2 \left[ g(x)f(x) \Big|_{-\infty}^{\infty} - \int_{-\infty}^{\infty} g'(x)f(x) \, dx \right] \quad (\text{Integration by Parts})
\end{aligned}
$$

Assuming $g(x)$ does not grow exponentially (so the boundary terms vanish):
$$
= \sigma^2 \int_{-\infty}^{\infty} g'(x)f(x) \, dx = \sigma^2 E[g'(X)]
$$

### Part 2: Proving $Cov[g(X), Y] = E[g'(X)]Cov(X, Y)$
We use the linear property of the bivariate normal distribution: $Y = a + bX + \epsilon$, where $\epsilon \perp X$.
$$
\begin{aligned}
Cov[g(X), Y] &= Cov[g(X), a + bX + \epsilon] \\
&= \underbrace{Cov[g(X), a]}_{0} + b \cdot Cov[g(X), X] + \underbrace{Cov[g(X), \epsilon]}_{0} \\
&= b \cdot E[g(X)(X - \mu)] \quad (\text{Using Part 1 result}) \\
&= b \cdot \sigma^2 E[g'(X)]
\end{aligned}
$$
For a bivariate normal regression, the slope coefficient is $b = \frac{Cov(X, Y)}{Var(X)} = \frac{Cov(X, Y)}{\sigma^2}$. Substituting this back:
$$
= \frac{Cov(X, Y)}{\sigma^2} \cdot \sigma^2 E[g'(X)] = E[g'(X)]Cov(X, Y)
$$

---

## Theorem 1: Stein's Lemma for Stochastic Volatility

### (a) Show $q(V)$ is a proper probability density
We check non-negativity and the integral sum:
1.  **Non-negativity:** Since $p(V) \ge 0$, $V > 0$, and $E[V] > 0$, the ratio $q(V) = \frac{V p(V)}{E[V]}$ is non-negative.
2.  **Integral:**
$$
\int_0^{\infty} q(V) \, dV = \int_0^{\infty} \frac{V p(V)}{E[V]} \, dV = \frac{1}{E[V]} \underbrace{\int_0^{\infty} V p(V) \, dV}_{E[V]} = \frac{E[V]}{E[V]} = 1
$$

### (b) Prove $Cov[g(X), X] = E[g(X)(X - E[X])]$
By the definition of covariance $Cov[A, B] = E[(A - E[A])(B - E[B])]$:
$$
\begin{aligned}
Cov[g(X), X] &= E[g(X)(X - E[X]) - E[g(X)](X - E[X])] \\
&= E[g(X)(X - E[X])] - E[g(X)] \underbrace{E[X - E[X]]}_{0} \\
&= E[g(X)(X - E[X])]
\end{aligned}
$$

### (c) Does step (2) follow by the Law of Iterated Expectations?
**Yes.**
The Law of Iterated Expectations states $E[Z] = E_V[E_{X|V}[Z]]$.
Defining $Z = g(X)(X - E[X])$, equation (2) is simply the explicit application of this law:
$$E[g(X)(X - E[X])] = E_V \{ E_{X|V} [g(X)(X - E[X])] \}$$

### (d) Prove step (3)
We must show that $(X - E[X])$ can be replaced by $(X - E[X|V])$.
1.  Given $X|V \sim N(\mu, \sigma^2 V)$, the conditional expectation is $E[X|V] = \mu$.
2.  The unconditional expectation is $E[X] = E_V[E[X|V]] = E_V[\mu] = \mu$.
3.  Since $E[X] = E[X|V] = \mu$, the terms are identical.
    $$E_{X|V}[g(X)(X - E[X])] = E_{X|V}[g(X)(X - E[X|V])]$$

### (e) Does (*) result imply (**)? Explain.
**Yes.**
Equation (*) is derived as:
$$
Cov[g(X), X] = E \left[ g'(X) \frac{V}{E[V]} \sigma^2 E[V] \right]
$$
Equation (**) states:
$$
Cov[g(X), X] = E_Q[g'(X)] Var[X]
$$
The implication holds because:
1.  **Variance Match:** Using the Law of Total Variance, $Var[X] = E[Var(X|V)] + Var(E[X|V]) = E[\sigma^2 V] + 0 = \sigma^2 E[V]$.
2.  **Measure Change:** The term $\frac{V p(V)}{E[V]}$ inside the expectation in (*) is exactly the density $q(V)$. Therefore, $E[g'(X) \frac{V}{E[V]}] = E_Q[g'(X)]$.

Substituting these into (*):
$$
E_Q[g'(X)] \cdot (\sigma^2 E[V]) = E_Q[g'(X)] Var[X]
$$