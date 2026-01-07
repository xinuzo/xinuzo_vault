>[!tips] 6.1 Partition
>A partition $P$ of $[a, b]$ is a finite set of points $x_0, x_1, ..., x_n$ such that $a = x_0 \le x_1 \le ... \le x_n = b$. $\Delta x_i = x_i - x_{i-1}$.

>[!tips] 6.1 Upper/Lower Sums
>Let $f$ be bounded on $[a, b]$, $P$ a partition. $M_i = \sup f(x)$ on $[x_{i-1}, x_i]$, $m_i = \inf f(x)$. Let $\alpha$ be monotonically increasing on $[a, b]$. $\Delta \alpha_i = \alpha(x_i) - \alpha(x_{i-1})$.
>$$U(P, f, \alpha) = \sum M_i \Delta \alpha_i$$
>$$L(P, f, \alpha) = \sum m_i \Delta \alpha_i$$

>[!tips] 6.2 Riemann-Stieltjes Integral
>$\int_a^b f d\alpha$ exists (denoted $f \in \mathscr{R}(\alpha)$) if $\inf U(P, f, \alpha) = \sup L(P, f, \alpha)$.