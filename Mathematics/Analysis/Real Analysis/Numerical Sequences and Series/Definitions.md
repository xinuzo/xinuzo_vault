>[!tips] 3.1 Convergent Sequence
>A sequence $\{p_n\}$ in a metric space $X$ is said to converge if there is a point $p \in X$ with the following property: For every $\epsilon > 0$ there is an integer $N$ such that $n \ge N$ implies $d(p_n, p) < \epsilon$. We write $p_n \to p$ or $\lim_{n\to\infty} p_n = p$.

>[!tips] 3.5 Subsequence
>Given a sequence $\{p_n\}$, consider a sequence $\{n_k\}$ of positive integers, such that $n_1 < n_2 < n_3 < ...$. Then the sequence $\{p_{n_k}\}$ is called a subsequence of $\{p_n\}$.

>[!tips] 3.8 Cauchy Sequence
>A sequence $\{p_n\}$ in a metric space $X$ is said to be a Cauchy sequence if for every $\epsilon > 0$ there is an integer $N$ such that $d(p_n, p_m) < \epsilon$ if $n \ge N$ and $m \ge N$.

>[!tips] 3.12 Complete Metric Space
>A metric space in which every Cauchy sequence converges is said to be complete.

>[!tips] 3.15 Divergence to Infinity
>$s_n \to +\infty$ means for every real $M$ there is an integer $N$ such that $n \ge N$ implies $s_n \ge M$.

>[!tips] 3.16 Upper and Lower Limits
>Let $\{s_n\}$ be a sequence of real numbers. Let $E$ be the set of numbers $x$ (in the extended real number system) such that $s_{n_k} \to x$ for some subsequence.
>$s^* = \sup E = \limsup_{n\to\infty} s_n$.
>$s_* = \inf E = \liminf_{n\to\infty} s_n$.

>[!tips] 3.21 Series
>Given a sequence $\{a_n\}$, the symbol $\sum_{n=1}^\infty a_n$ is called an infinite series. $s_n = \sum_{k=1}^n a_k$ are the partial sums. If $\{s_n\}$ converges to $s$, the series converges and $s$ is the sum.

>[!tips] 3.38 Power Series
>A series of the form $\sum_{n=0}^\infty c_n z^n$ is called a power series.

>[!tips] 3.45 Absolute Convergence
>The series $\sum a_n$ is said to converge absolutely if the series $\sum |a_n|$ converges.