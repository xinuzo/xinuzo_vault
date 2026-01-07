>[!tips] Theorem 2.1.1 Expectation of a Function
>For a random vector $(X_1, X_2)$ and function $Y = g(X_1, X_2)$:
>[cite_start]$$E(Y) = \int_{-\infty}^{\infty} \int_{-\infty}^{\infty} g(x_1, x_2) f(x_1, x_2) \, dx_1 \, dx_2$$ [cite: 19]

>[!tips] Theorem 2.4.1 Factorization Theorem
>[cite_start]Random variables $X_1$ and $X_2$ are independent if and only if the joint pdf $f(x_1, x_2)$ can be written as the product of a nonnegative function of $x_1$ alone and a nonnegative function of $x_2$ alone on a product space. [cite: 28]

>[!tips] Theorem 2.4.4 Expectation of Independent Variables
>[cite_start]If $X_1$ and $X_2$ are independent, then $E[u(X_1)v(X_2)] = E[u(X_1)]E[v(X_2)]$. [cite: 28]

>[!tips] Theorem 2.5.1 Bounds of Correlation
>[cite_start]For all jointly distributed random variables $(X, Y)$ whose correlation coefficient $\rho$ exists, $-1 \le \rho \le 1$. [cite: 30]

>[!tips] Theorem 2.6.1 MGF of Independent Variables
>[cite_start]If $X_1, ..., X_n$ are independent random variables with mgfs $M_{X_i}(t)$, then the mgf of $Y = \sum a_i X_i$ is $M_Y(t) = \prod M_{X_i}(a_i t)$. [cite: 46]

>[!tips] Theorem 2.8.2 Mean and Variance of Linear Combinations
>Let $T = \sum_{i=1}^n a_i X_i$. Then:
>$$E(T) = \sum_{i=1}^n a_i E(X_i)$$
>$$Var(T) = \sum_{i=1}^n a_i^2 Var(X_i) + 2 \sum_{i<j} a_i a_j Cov(X_i, X_j)$$
>[cite_start]If $X_i$ are independent, the covariance terms are zero. [cite: 38]