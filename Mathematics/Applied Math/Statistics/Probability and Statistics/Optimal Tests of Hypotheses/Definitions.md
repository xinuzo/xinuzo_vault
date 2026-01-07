>[!tips] 8.1 Power Function and Size
>For testing $H_0: \theta \in \omega$ vs $H_1: \theta \in \omega^c$, let $C$ be the critical region.
>Power function: $\gamma(\theta) = P(\mathbf{X} \in C ; \theta)$.
>Size of the test: $\alpha = \max_{\theta \in \omega} \gamma(\theta)$.

>[!tips] 8.1 Most Powerful (MP) Test
>A test defined by critical region $C$ of size $\alpha$ is a Most Powerful test of $H_0: \theta = \theta_0$ vs $H_1: \theta = \theta_1$ if $\gamma(\theta_1)$ is greater than or equal to the power of any other test of size $\alpha$.

>[!tips] 8.1 Uniformly Most Powerful (UMP) Test
>A test is UMP for $H_0$ vs composite $H_1$ if it is Most Powerful against every specific $\theta \in H_1$.

>[!tips] 8.2 Monotone Likelihood Ratio (MLR)
>A family of pdfs $f(x; \theta)$ has a Monotone Likelihood Ratio in statistic $Y$ if for $\theta_1 < \theta_2$, the ratio $f(x; \theta_2)/f(x; \theta_1)$ is a non-decreasing function of $Y$.

>[!tips] 8.3 Likelihood Ratio Test (LRT)
>The likelihood ratio statistic is:
>$$\Lambda = \frac{\max_{\theta \in \omega} L(\theta)}{\max_{\theta \in \Omega} L(\theta)}$$
>Reject $H_0$ if $\Lambda \le c$, where $c$ is chosen to satisfy the size $\alpha$.