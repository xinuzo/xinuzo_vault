>[!tips] Theorem 8.1.1 Neyman-Pearson Lemma
>To test simple $H_0: \theta = \theta_0$ vs simple $H_1: \theta = \theta_1$, the Most Powerful test rejects $H_0$ when:
>$$\frac{L(\theta_1)}{L(\theta_0)} \ge k$$
>for some constant $k$ determined by the significance level $\alpha$.

>[!tips] Theorem 8.2.1 Karlin-Rubin Theorem
>If the family of distributions has a Monotone Likelihood Ratio (MLR) in sufficient statistic $Y$, then the UMP test of size $\alpha$ for $H_0: \theta \le \theta_0$ vs $H_1: \theta > \theta_0$ rejects $H_0$ if $Y \ge c$.

>[!tips] Theorem 8.3.1 Asymptotic Distribution of LRT
>Under regularity conditions, if $H_0$ puts $r$ constraints on the parameter space, then as $n \to \infty$:
>$$-2 \log \Lambda \xrightarrow{D} \chi^2(r)$$