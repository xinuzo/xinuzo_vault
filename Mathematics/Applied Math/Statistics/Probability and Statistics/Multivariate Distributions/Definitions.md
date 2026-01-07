>[!tips] 2.1 Joint Cumulative Distribution Function (cdf)
>The joint cdf of two random variables $X_1$ and $X_2$ is defined as:
>$$F_{X_1,X_2}(x_1, x_2) = P(\{X_1 \le x_1\} \cap \{X_2 \le x_2\})$$
>[cite_start]for all $(x_1, x_2) \in \mathbb{R}^2$. [cite: 16]

>[!tips] 2.1 Discrete Random Vector
>A random vector $(X_1, X_2)$ is discrete if its space $\mathcal{D}$ is finite or countable. [cite_start]The joint probability mass function (pmf) is $p_{X_1,X_2}(x_1, x_2) = P(X_1 = x_1, X_2 = x_2)$. [cite: 16]

>[!tips] 2.1 Continuous Random Vector
>A random vector $(X_1, X_2)$ is continuous if its joint cdf $F_{X_1,X_2}(x_1, x_2)$ is continuous. The joint probability density function (pdf) $f_{X_1,X_2}(x_1, x_2)$ satisfies:
>[cite_start]$$F_{X_1,X_2}(x_1, x_2) = \int_{-\infty}^{x_1} \int_{-\infty}^{x_2} f_{X_1,X_2}(w_1, w_2) \, dw_2 \, dw_1$$ [cite: 17]

>[!tips] 2.1 Marginal Distributions
>For a discrete random vector, the marginal pmf of $X_1$ is $p_1(x_1) = \sum_{x_2} p(x_1, x_2)$.
>[cite_start]For a continuous random vector, the marginal pdf of $X_1$ is $f_1(x_1) = \int_{-\infty}^{\infty} f(x_1, x_2) \, dx_2$. [cite: 18]

>[!tips] 2.3 Conditional Probability Density Function
>The conditional pdf of $X_1$ given $X_2 = x_2$ is defined as:
>$$f_{1|2}(x_1|x_2) = \frac{f(x_1, x_2)}{f_2(x_2)}$$
>[cite_start]provided $f_2(x_2) > 0$. [cite: 25]

>[!tips] 2.3 Conditional Expectation
>The conditional mean of $X_1$ given $X_2 = x_2$ is:
>$$E(X_1|x_2) = \int_{-\infty}^{\infty} x_1 f_{1|2}(x_1|x_2) \, dx_1$$
>[cite_start]The conditional variance is $Var(X_1|x_2) = E([X_1 - E(X_1|x_2)]^2 | x_2)$. [cite: 25]

>[!tips] 2.4 Independent Random Variables
>Random variables $X_1$ and $X_2$ are independent if and only if their joint pdf (or pmf) factors into the product of their marginals:
>$$f(x_1, x_2) = f_1(x_1)f_2(x_2)$$
>[cite_start]for all $(x_1, x_2)$. [cite: 27]

>[!tips] 2.5 Covariance
>[cite_start]The covariance of $X$ and $Y$ is defined as $Cov(X, Y) = E[(X - \mu_X)(Y - \mu_Y)] = E(XY) - \mu_X \mu_Y$. [cite: 30]

>[!tips] 2.5 Correlation Coefficient
>The correlation coefficient $\rho$ is defined as:
>[cite_start]$$\rho = \frac{Cov(X, Y)}{\sigma_X \sigma_Y}$$ [cite: 30]

>[!tips] 2.6 Multivariate Variance-Covariance Matrix
>[cite_start]For a random vector $\mathbf{X} = (X_1, ..., X_n)'$, the variance-covariance matrix is given by $Cov(\mathbf{X}) = E[(\mathbf{X} - \mathbf{\mu})(\mathbf{X} - \mathbf{\mu})']$. [cite: 35]