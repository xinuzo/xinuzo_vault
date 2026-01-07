>[!tips] 6.1 Likelihood Function
>Let $X_1, \dots, X_n$ be a random sample from a distribution with pdf/pmf $f(x; \theta)$. The likelihood function is defined as:
>$$L(\theta) = \prod_{i=1}^n f(x_i; \theta)$$
>The log-likelihood is $l(\theta) = \log L(\theta)$.

>[!tips] 6.1 Maximum Likelihood Estimator (MLE)
>The statistic $\hat{\theta} = \hat{\theta}(X_1, \dots, X_n)$ that maximizes $L(\theta)$ (or equivalently $l(\theta)$) for a given sample is the Maximum Likelihood Estimator of $\theta$.

>[!tips] 6.2 Fisher Information
>The Fisher Information $I(\theta)$ contained in a single random variable $X$ about $\theta$ is:
>$$I(\theta) = E\left[ \left( \frac{\partial \log f(X; \theta)}{\partial \theta} \right)^2 \right] = -E\left[ \frac{\partial^2 \log f(X; \theta)}{\partial \theta^2} \right]$$
>For a random sample of size $n$, the information is $nI(\theta)$.

>[!tips] 6.2 Efficient Estimator
>An unbiased estimator $\hat{\theta}$ is efficient if its variance achieves the Rao-Cramér Lower Bound.
>The efficiency of an estimator is defined as $eff(\hat{\theta}) = \frac{1/nI(\theta)}{Var(\hat{\theta})}$.