>[!tips] Theorem 6.1.1 Properties of MLE
>Under regularity conditions, the MLE $\hat{\theta}$ is a consistent estimator of $\theta$ ($\hat{\theta} \xrightarrow{P} \theta$).

>[!tips] Theorem 6.2.1 Rao-Cramér Lower Bound (RCLB)
>Let $X_1, \dots, X_n$ be a sample from $f(x; \theta)$. Under regularity conditions, for any unbiased estimator $Y$ of $\theta$:
>$$Var(Y) \ge \frac{1}{n I(\theta)}$$

>[!tips] Theorem 6.2.2 Asymptotic Normality of MLE
>Under regularity conditions, the MLE $\hat{\theta}$ has the following limiting distribution:
>$$\sqrt{n}(\hat{\theta} - \theta) \xrightarrow{D} N\left(0, \frac{1}{I(\theta)}\right)$$
>That is, $\hat{\theta}$ is asymptotically efficient.