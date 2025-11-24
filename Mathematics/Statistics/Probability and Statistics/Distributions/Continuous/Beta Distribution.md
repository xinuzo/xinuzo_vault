> [!tips] (Definition) Beta Distribution
> Defines a random variable restricted to $(0,1)$, often used to model proportions or probabilities.
> $$X \sim Beta(\alpha, \beta)$$
> **P.D.F.:**
> $$f(x) = \frac{\Gamma(\alpha+\beta)}{\Gamma(\alpha)\Gamma(\beta)} x^{\alpha-1}(1-x)^{\beta-1}, \quad 0 < x < 1$$
> **Mean & Variance:**
> $$\mu = \frac{\alpha}{\alpha+\beta}, \quad \sigma^2 = \frac{\alpha\beta}{(\alpha+\beta)^2(\alpha+\beta+1)}$$

> [!success]- Proof of $\mu$ and $\sigma^2$
> $$E[X] = \frac{\Gamma(\alpha+\beta)}{\Gamma(\alpha)\Gamma(\beta)} \int_0^1 x^{\alpha}(1-x)^{\beta-1} dx = \frac{\Gamma(\alpha+\beta)}{\Gamma(\alpha)\Gamma(\beta)} \frac{\Gamma(\alpha+1)\Gamma(\beta)}{\Gamma(\alpha+\beta+1)} = \frac{\alpha}{\alpha+\beta}$$
> $$E[X^2] = \dots \int_0^1 x^{\alpha+1}(1-x)^{\beta-1} dx = \frac{\Gamma(\alpha+\beta)}{\Gamma(\alpha)} \frac{\Gamma(\alpha+2)}{\Gamma(\alpha+\beta+2)} = \frac{\alpha(\alpha+1)}{(\alpha+\beta)(\alpha+\beta+1)}$$
> $$\sigma^2 = E[X^2] - \mu^2 = \dots (\text{algebraic simplification}) \dots = \frac{\alpha\beta}{(\alpha+\beta)^2(\alpha+\beta+1)}$$