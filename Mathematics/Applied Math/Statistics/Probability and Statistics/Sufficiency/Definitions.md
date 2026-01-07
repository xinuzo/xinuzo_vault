>[!tips] 7.1 Sufficient Statistic
>A statistic $Y = u(X_1, \dots, X_n)$ is sufficient for $\theta$ if the conditional distribution of the sample $X_1, \dots, X_n$ given $Y=y$ does not depend on $\theta$.

>[!tips] 7.2 Minimal Sufficient Statistic
>A sufficient statistic is minimal if it is a function of any other sufficient statistic.

>[!tips] 7.2 Ancillary Statistic
>A statistic whose distribution does not depend on the parameter $\theta$ is called an ancillary statistic.

>[!tips] 7.3 Complete Statistic
>A family of distributions $\{f(y; \theta) : \theta \in \Omega\}$ is complete if $E[u(Y)] = 0$ for all $\theta \in \Omega$ implies $P(u(Y) = 0) = 1$ for all $\theta$. A statistic $Y$ is complete if its family of induced distributions is complete.

>[!tips] 7.5 Exponential Class
>A pdf of the form $f(x; \theta) = \exp[p(\theta)K(x) + H(x) + q(\theta)]$ belongs to the regular exponential class. For these families, $K(X)$ is a complete sufficient statistic.