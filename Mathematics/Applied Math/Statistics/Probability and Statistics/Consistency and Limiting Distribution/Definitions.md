>[!tips] 5.1 Convergence in Probability
>A sequence of random variables $X_1, X_2, \dots$ converges in probability to a random variable $X$ if, for every $\epsilon > 0$,
>$$\lim_{n \to \infty} P(|X_n - X| \ge \epsilon) = 0$$
>We write $X_n \xrightarrow{P} X$.

>[!tips] 5.1 Consistent Estimator
>An estimator $\hat{\theta}_n$ (based on a sample of size $n$) is a consistent estimator of $\theta$ if $\hat{\theta}_n \xrightarrow{P} \theta$.

>[!tips] 5.2 Convergence in Distribution
>A sequence of random variables $X_n$ with cdfs $F_n(x)$ converges in distribution to a random variable $X$ with cdf $F(x)$ if
>$$\lim_{n \to \infty} F_n(x) = F(x)$$
>at all points $x$ where $F(x)$ is continuous. We write $X_n \xrightarrow{D} X$.

>[!tips] 5.2 Bounded in Probability
>A sequence $\{X_n\}$ is bounded in probability ($O_p(1)$) if for every $\epsilon > 0$, there exists a constant $B_\epsilon$ and integer $N_\epsilon$ such that $P(|X_n| \ge B_\epsilon) \le \epsilon$ for all $n \ge N_\epsilon$.