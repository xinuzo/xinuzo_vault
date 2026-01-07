>[!tips] 10.1 Location Model
>A model $X_i = \theta + e_i$ where $e_i$ are iid with continuous pdf $f(x)$ symmetric about 0. The parameter $\theta$ is the median (and mean, if it exists).

>[!tips] 10.1 Sign Test
>A simple nonparametric test for $H_0: \theta = 0$.
>Statistic $S$: The number of positive observations $X_i > 0$.
>Under $H_0$, $S \sim \text{Binomial}(n, 0.5)$.

>[!tips] 10.2 Signed-Rank Test
>Wilcoxon Signed-Rank Test uses the ranks of absolute values $|X_i|$ combined with the signs of $X_i$.
>Statistic $T = \sum_{i=1}^n \text{sgn}(X_i) R_i$, where $R_i$ is the rank of $|X_i|$.

>[!tips] 10.3 Mann-Whitney-Wilcoxon Test
>A test for equality of two independent distributions (Shift model: $F_Y(x) = F_X(x - \Delta)$). Tests $H_0: \Delta = 0$.
>Based on the sum of ranks of one sample in the combined ranking of both samples.

>[!tips] 10.7 Breakdown Point
>A measure of robustness. The smallest proportion of observations that can be arbitrarily contaminated to force the estimator to infinity.
>Sample mean has breakdown point $1/n \to 0$. Sample median has breakdown point $0.5$.