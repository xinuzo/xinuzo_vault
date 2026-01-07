>[!tips] 11.1 Prior and Posterior Distributions
>- **Prior ($h(\theta)$)**: Probability distribution expressing beliefs about $\theta$ before observing data.
>- **Posterior ($k(\theta | \mathbf{x})$)**: Conditional distribution of $\theta$ given the sample $\mathbf{x}$.
>$$k(\theta | \mathbf{x}) \propto L(\theta | \mathbf{x}) h(\theta)$$

>[!tips] 11.1 Bayes Estimator
>An estimator that minimizes the expected loss (risk) with respect to the posterior distribution.
>For Squared Error Loss ($L(\theta, \delta) = (\theta - \delta)^2$), the Bayes estimator is the posterior mean $E(\theta | \mathbf{x})$.
>For Absolute Error Loss, it is the posterior median.

>[!tips] 11.2 Conjugate Prior
>A family of prior distributions is conjugate to a sampling distribution if the posterior distribution belongs to the same family.
>Example: Beta prior is conjugate to Binomial likelihood. Normal prior is conjugate to Normal likelihood (for mean).

>[!tips] 11.4 Gibbs Sampler
>A Markov Chain Monte Carlo (MCMC) algorithm for obtaining a sequence of observations from a multivariate probability distribution, when direct sampling is difficult. It samples from conditional distributions.

>[!tips] 11.5 Empirical Bayes
>Methods where the hyperparameters of the prior distribution are estimated from the data itself.