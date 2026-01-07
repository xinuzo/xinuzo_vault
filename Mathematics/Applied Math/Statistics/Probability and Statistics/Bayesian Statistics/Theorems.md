>[!tips] Theorem 11.1.1 Bayes' Theorem (for densities)
>$$k(\theta | \mathbf{x}) = \frac{f(\mathbf{x} | \theta) h(\theta)}{\int f(\mathbf{x} | \theta) h(\theta) d\theta} = \frac{\text{Likelihood} \times \text{Prior}}{\text{Marginal of } \mathbf{x}}$$

>[!tips] Property: Asymptotic Normality of Posterior
>For large samples, under regularity conditions, the posterior distribution $k(\theta | \mathbf{x})$ is approximately Normal centered at the MLE $\hat{\theta}$ with variance $1/I(\hat{\theta})$.