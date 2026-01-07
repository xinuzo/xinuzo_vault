>[!tips] 5.55 Convergence of Series
>An infinite series $\sum_{n=0}^\infty z_n$ converges to sum $S$ if the sequence of partial sums $S_N$ converges to $S$.

>[!tips] 5.57 Power Series
>A series of the form $\sum_{n=0}^\infty a_n (z - z_0)^n$.
>- **Circle of Convergence**: The largest circle $|z - z_0| = R$ inside which the series converges.

>[!tips] 5.60 Laurent Series
>A representation for a function $f$ analytic in an annulus $R_1 < |z - z_0| < R_2$:
>$$f(z) = \sum_{n=0}^\infty a_n (z - z_0)^n + \sum_{n=1}^\infty \frac{b_n}{(z - z_0)^n}$$
>The first part is the analytic part; the second is the **principal part**.

>[!tips] 5.61 Absolute and Uniform Convergence
>- **Absolute**: $\sum |z_n|$ converges.
>- **Uniform**: For every $\epsilon > 0$, there exists $N$ independent of $z$ such that $|S_n(z) - S(z)| < \epsilon$ for $n > N$.