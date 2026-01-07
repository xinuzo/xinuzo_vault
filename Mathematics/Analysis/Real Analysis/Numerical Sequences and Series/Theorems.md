>[!tips] Theorem 3.2 Properties of Limits
>(a) Limit is unique.
>(b) Convergent sequence is bounded.
>(c) If $p$ is a limit point of $E$, there is a sequence in $E$ converging to $p$.

>[!tips] Theorem 3.3 Algebraic Operations
>If $s_n \to s$ and $t_n \to t$, then:
>$\lim(s_n + t_n) = s + t$
>$\lim(c s_n) = c s$
>$\lim(s_n t_n) = s t$
>$\lim(1/s_n) = 1/s$ (provided $s_n \ne 0, s \ne 0$).

>[!tips] Theorem 3.6 Subsequences
>(a) If $\{p_n\}$ is a sequence in a compact metric space $X$, then some subsequence of $\{p_n\}$ converges to a point of $X$.
>(b) Every bounded sequence in $R^k$ contains a convergent subsequence.

>[!tips] Theorem 3.10 Nested Sets
>If $\{K_n\}$ is a sequence of compact sets in $X$ such that $K_n \supset K_{n+1}$ and $\lim_{n\to\infty} \text{diam } K_n = 0$, then $\bigcap_{1}^\infty K_n$ consists of exactly one point.

>[!tips] Theorem 3.11 Cauchy Criterion
>(a) In any metric space, every convergent sequence is a Cauchy sequence.
>(b) If $X$ is a compact metric space and if $\{p_n\}$ is a Cauchy sequence in $X$, then $\{p_n\}$ converges to some point of $X$.
>(c) In $R^k$, every Cauchy sequence converges.

>[!tips] Theorem 3.14 Monotonic Sequences
>A monotonic sequence converges if and only if it is bounded.

>[!tips] Theorem 3.20 Special Limits
>(a) $\lim_{n\to\infty} \frac{1}{n^p} = 0$ ($p > 0$).
>(b) $\lim_{n\to\infty} \sqrt[n]{p} = 1$ ($p > 0$).
>(c) $\lim_{n\to\infty} \sqrt[n]{n} = 1$.
>(e) $\lim_{n\to\infty} x^n = 0$ if $|x| < 1$.

>[!tips] Theorem 3.22 Cauchy Criterion for Series
>$\sum a_n$ converges iff for every $\epsilon > 0$ there is an integer $N$ such that $|\sum_{k=n}^m a_k| \le \epsilon$ if $m \ge n \ge N$.

>[!tips] Theorem 3.23 Necessary Condition
>If $\sum a_n$ converges, then $\lim_{n\to\infty} a_n = 0$.

>[!tips] Theorem 3.25 Comparison Test
>(a) If $|a_n| \le c_n$ for $n \ge N_0$, and $\sum c_n$ converges, then $\sum a_n$ converges.
>(b) If $a_n \ge d_n \ge 0$ for $n \ge N_0$, and $\sum d_n$ diverges, then $\sum a_n$ diverges.

>[!tips] Theorem 3.26 Geometric Series
>If $0 \le x < 1$, $\sum_{n=0}^\infty x^n = \frac{1}{1-x}$. If $x \ge 1$, the series diverges.

>[!tips] Theorem 3.27 Cauchy Condensation Test
>Suppose $a_1 \ge a_2 \ge a_3 \ge ... \ge 0$. Then $\sum_{n=1}^\infty a_n$ converges if and only if $\sum_{k=0}^\infty 2^k a_{2^k}$ converges.

>[!tips] Theorem 3.28 p-series
>$\sum \frac{1}{n^p}$ converges if $p > 1$ and diverges if $p \le 1$.

>[!tips] Theorem 3.31 The Number e
>$\lim_{n\to\infty} (1 + \frac{1}{n})^n = e = \sum_{n=0}^\infty \frac{1}{n!}$.

>[!tips] Theorem 3.33 Root Test
>Given $\sum a_n$, put $\alpha = \limsup_{n\to\infty} \sqrt[n]{|a_n|}$.
>(a) If $\alpha < 1$, $\sum a_n$ converges.
>(b) If $\alpha > 1$, $\sum a_n$ diverges.
>(c) If $\alpha = 1$, the test gives no information.

>[!tips] Theorem 3.34 Ratio Test
>The series $\sum a_n$:
>(a) Converges if $\limsup_{n\to\infty} |\frac{a_{n+1}}{a_n}| < 1$.
>(b) Diverges if $|\frac{a_{n+1}}{a_n}| \ge 1$ for all $n \ge n_0$.

>[!tips] Theorem 3.39 Radius of Convergence
>Given $\sum c_n z^n$, put $\alpha = \limsup_{n\to\infty} \sqrt[n]{|c_n|}$, $R = 1/\alpha$. Then the series converges if $|z| < R$, and diverges if $|z| > R$.

>[!tips] Theorem 3.42 Summation by Parts
>Suppose (a) partial sums $A_n$ of $\sum a_n$ are bounded; (b) $b_0 \ge b_1 \ge ...$; (c) $\lim b_n = 0$. Then $\sum a_n b_n$ converges.

>[!tips] Theorem 3.43 Alternating Series
>If $|c_1| \ge |c_2| \ge ...$, $c_{2m-1} \ge 0, c_{2m} \le 0$, and $\lim c_n = 0$, then $\sum c_n$ converges.

>[!tips] Theorem 3.45 Absolute Convergence
>If $\sum a_n$ converges absolutely, then $\sum a_n$ converges.

>[!tips] Theorem 3.50 Product of Series (Mertens)
>If $\sum a_n$ converges absolutely to $A$, $\sum b_n$ converges to $B$, and $c_n = \sum_{k=0}^n a_k b_{n-k}$, then $\sum c_n = AB$.

>[!tips] Theorem 3.54 Riemann Rearrangement Theorem
>Let $\sum a_n$ be a series of real numbers which converges, but not absolutely. Then for any $\alpha, \beta$, there exists a rearrangement with $\liminf = \alpha$ and $\limsup = \beta$.