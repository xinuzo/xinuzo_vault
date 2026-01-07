>[!tips] 4.1 Limit of a Function
>Let $X$ and $Y$ be metric spaces, $E \subset X$, $f$ maps $E$ into $Y$, and $p$ is a limit point of $E$. We write $f(x) \to q$ as $x \to p$, or $\lim_{x\to p} f(x) = q$, if there is a point $q \in Y$ such that for every $\epsilon > 0$ there exists a $\delta > 0$ such that $d_Y(f(x), q) < \epsilon$ for all $x \in E$ for which $0 < d_X(x, p) < \delta$.

>[!tips] 4.5 Continuous Function
>Suppose $X$ and $Y$ are metric spaces, $E \subset X$, $p \in E$, and $f: E \to Y$. Then $f$ is said to be continuous at $p$ if for every $\epsilon > 0$ there exists a $\delta > 0$ such that $d_Y(f(x), f(p)) < \epsilon$ for all $x \in E$ with $d_X(x, p) < \delta$.
>If $f$ is continuous at every point of $E$, then $f$ is said to be continuous on $E$.

>[!tips] 4.8 Uniform Continuity
>Let $f$ be a mapping of a metric space $X$ into a metric space $Y$. We say that $f$ is uniformly continuous on $X$ if for every $\epsilon > 0$ there exists a $\delta > 0$ such that $d_Y(f(p), f(q)) < \epsilon$ for all $p, q \in X$ for which $d_X(p, q) < \delta$.

>[!tips] 4.25 Discontinuity of the Second Kind
>If $f$ is defined on $(a, b)$ and discontinuous at $x \in (a, b)$, and if limits $f(x+)$ and $f(x-)$ exist, $f$ has a discontinuity of the first kind (simple). Otherwise, it is of the second kind.

>[!tips] 4.28 Monotonic Function
>Let $f$ be real on $(a, b)$. $f$ is monotonically increasing on $(a, b)$ if $a < x < y < b$ implies $f(x) \le f(y)$. Decreasing is defined similarly.