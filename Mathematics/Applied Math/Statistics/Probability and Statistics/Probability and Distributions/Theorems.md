>[!tips] Theorem 1.3.1 Complement Rule
>For each event $A$, $P(A) = 1 - P(A^c)$.

>[!tips] Theorem 1.3.3 Monotonicity
>If $A \subset B$, then $P(A) \le P(B)$.

>[!tips] Theorem 1.3.5 Addition Rule
>For any two events $A$ and $B$,
>$$P(A \cup B) = P(A) + P(B) - P(A \cap B)$$

>[!tips] Theorem 1.3.6 Continuity Theorem of Probability
>If $\{C_n\}$ is a nondecreasing sequence of events ($C_n \subset C_{n+1}$), then
>$$\lim_{n\to\infty} P(C_n) = P(\lim_{n\to\infty} C_n) = P(\bigcup_{n=1}^{\infty} C_n)$$
>If $\{C_n\}$ is nonincreasing, $\lim_{n\to\infty} P(C_n) = P(\bigcap_{n=1}^{\infty} C_n)$.

>[!tips] Theorem 1.3.7 Boole's Inequality
>For an arbitrary sequence of events $\{C_n\}$,
>$$P(\bigcup_{n=1}^{\infty} C_n) \le \sum_{n=1}^{\infty} P(C_n)$$

>[!tips] Multiplication Rule
>$P(A \cap B) = P(A)P(B|A)$.
>Extended: $P(A \cap B \cap C) = P(A)P(B|A)P(C|A \cap B)$.

>[!tips] Law of Total Probability
>If $A_1, ..., A_k$ form a partition of $\mathcal{C}$, then for any event $B$:
>$$P(B) = \sum_{i=1}^k P(A_i)P(B|A_i)$$

>[!tips] Theorem 1.4.1 Bayes' Theorem
>$$P(A_j|B) = \frac{P(A_j)P(B|A_j)}{\sum_{i=1}^k P(A_i)P(B|A_i)}$$

>[!tips] Theorem 1.5.1 Properties of CDF
>(a) $F(a) \le F(b)$ if $a < b$ (nondecreasing).
>(b) $\lim_{x\to-\infty} F(x) = 0$.
>(c) $\lim_{x\to\infty} F(x) = 1$.
>(d) $\lim_{x \downarrow x_0} F(x) = F(x_0)$ (right continuous).

>[!tips] Theorem 1.5.3 Mass at Discontinuities
>$P[X=x] = F_X(x) - F_X(x-)$.
>For continuous random variables, $P[X=x] = 0$.

>[!tips] Theorem 1.7.1 Transformation (Continuous)
>Let $Y = g(X)$ where $g$ is one-to-one and differentiable. The pdf of $Y$ is:
>$$f_Y(y) = f_X(g^{-1}(y)) \left| \frac{dx}{dy} \right|$$
>where $dx/dy$ is the Jacobian of the inverse transformation $x = g^{-1}(y)$.

>[!tips] Theorem 1.8.1 Expectation of a Function
>Let $Y = g(X)$.
>Continuous: $E(Y) = \int_{-\infty}^{\infty} g(x) f_X(x) dx$.
>Discrete: $E(Y) = \sum_{x \in \mathcal{D}} g(x) p_X(x)$.

>[!tips] Theorem 1.8.2 Linearity of Expectation
>$E[k_1 g_1(X) + k_2 g_2(X)] = k_1 E[g_1(X)] + k_2 E[g_2(X)]$.

>[!tips] Theorem 1.10.2 Markov's Inequality
>If $u(X)$ is a nonnegative function and $c > 0$,
>$$P[u(X) \ge c] \le \frac{E[u(X)]}{c}$$

>[!tips] Theorem 1.10.3 Chebyshev's Inequality
>Let $X$ have finite variance $\sigma^2$. For every $k > 0$,
>$$P(|X - \mu| \ge k\sigma) \le \frac{1}{k^2}$$

>[!tips] Theorem 1.10.5 Jensen's Inequality
>If $\phi$ is convex on an open interval containing the support of $X$, then
>$$\phi(E(X)) \le E[\phi(X)]$$
>Example: Since $\phi(x) = x^2$ is convex, $(E[X])^2 \le E[X^2]$.