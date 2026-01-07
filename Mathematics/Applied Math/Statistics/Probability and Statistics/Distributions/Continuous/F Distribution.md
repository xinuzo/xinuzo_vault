
> [!tips] (Definition) F Distribution
> The distribution of the ratio of two independent chi-square variables divided by their degrees of freedom. Used in ANOVA. Let $U \sim \chi^2(r_1), V \sim \chi^2(r_2)$.
> $$W = \frac{U/r_1}{V/r_2} \sim F(r_1, r_2)$$
> **P.D.F.:** Complex expression involving Beta/Gamma functions.
> **Mean & Variance:**
> $$\mu = \frac{r_2}{r_2-2} \text{ (if } r_2>2), \quad \sigma^2 = \text{complex func of } r_1, r_2$$

> [!success]- Proof of $\mu$
> $$E[W] = \frac{r_2}{r_1} E[U] E[V^{-1}]$$
> Using mean of $\chi^2$ and mean of inverse $\chi^2$:
> $$E[U] = r_1, \quad E[V^{-1}] = \frac{1}{r_2-2}$$
> $$E[W] = \frac{r_2}{r_1} (r_1) \left(\frac{1}{r_2-2}\right) = \frac{r_2}{r_2-2}$$