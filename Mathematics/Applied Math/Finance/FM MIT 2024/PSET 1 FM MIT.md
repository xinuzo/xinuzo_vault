## PSET Mathematics with Application in Finance

> [!question] No. 1 Fibonacci Numbers
> **(a)** Show $\vec{u}_{k+1}=A\vec{u}_{k}$.
> **(b)** Show $\vec{u}_{k}=A^{k}\vec{u}_{0}$.
> **(c)** Solve for eigenvalues $\lambda_{1}, \lambda_{2}$.
> **(d)** Show eigenvector $\vec{s}=[\lambda, 1]^T$.
> **(e)** Compute $S^{-1}$.
> **(f)** Show $A=S\Lambda S^{-1}$.
> **(g)** Compute $\vec{c}=S^{-1}\vec{u}_{0}$ and find $a$.
> **(h)** Show $F_{k}=\frac{1}{\sqrt{5}}[\lambda_{2}^{k}-\lambda_{1}^{k}]$.
> **(i)** What is the limiting ratio (Golden Ratio)?

> [!success]- Solution
> **(a)**
> $$A\vec{u}_k = \begin{bmatrix}1&1\\1&0\end{bmatrix} \begin{bmatrix}F_{k+1}\\F_k\end{bmatrix} = \begin{bmatrix}F_{k+1}+F_k\\F_{k+1}\end{bmatrix} = \begin{bmatrix}F_{k+2}\\F_{k+1}\end{bmatrix} = \vec{u}_{k+1}$$
> [cite_start]Since $F_{k+2} = F_{k+1} + F_k$[cite: 9, 11].
>
> **(b)**
> [cite_start]By induction: $\vec{u}_1 = A\vec{u}_0$, $\vec{u}_2 = A\vec{u}_1 = A(A\vec{u}_0) = A^2\vec{u}_0$. generally $\vec{u}_k = A^k\vec{u}_0$[cite: 12].
>
> **(c)**
> $\det(A-\lambda I) = (1-\lambda)(-\lambda) - 1 = \lambda^2 - \lambda - 1 = 0$.
> [cite_start]$\lambda_{1,2} = \frac{1 \pm \sqrt{5}}{2}$[cite: 13].
>
> **(d)**
> $A\vec{s} = \begin{bmatrix}1&1\\1&0\end{bmatrix}\begin{bmatrix}\lambda\\1\end{bmatrix} = \begin{bmatrix}\lambda+1\\\lambda\end{bmatrix}$.
> [cite_start]Since $\lambda^2 - \lambda - 1 = 0 \implies \lambda+1 = \lambda^2$, then $\begin{bmatrix}\lambda^2\\\lambda\end{bmatrix} = \lambda\begin{bmatrix}\lambda\\1\end{bmatrix} = \lambda\vec{s}$[cite: 15, 16].
>
> **(e)**
> $S = \begin{bmatrix}\lambda_1 & \lambda_2 \\ 1 & 1\end{bmatrix}$. Determinant is $\lambda_1 - \lambda_2$.
> [cite_start]$S^{-1} = \frac{1}{\lambda_1 - \lambda_2} \begin{bmatrix}1 & -\lambda_2 \\ -1 & \lambda_1\end{bmatrix}$[cite: 20].
>
> **(f)**
> [cite_start]Standard diagonalization definition: Since $S$ contains eigenvectors, $AS = S\Lambda$, thus $A = S\Lambda S^{-1}$[cite: 21].
>
> **(g)**
> $\vec{u}_0 = \begin{bmatrix}1\\0\end{bmatrix}$ (since $F_1=1, F_0=0$).
> $\vec{c} = S^{-1}\vec{u}_0 = \frac{1}{\lambda_1 - \lambda_2} \begin{bmatrix}1 & -\lambda_2 \\ -1 & \lambda_1\end{bmatrix} \begin{bmatrix}1\\0\end{bmatrix} = \frac{1}{\lambda_1 - \lambda_2} \begin{bmatrix}1\\-1\end{bmatrix}$.
> [cite_start]Constant $a = \frac{1}{\lambda_1 - \lambda_2} = \frac{1}{\sqrt{5}}$[cite: 23, 25].
>
> **(h)**
> $\vec{u}_k = S\Lambda^k \vec{c} = S \begin{bmatrix}\lambda_1^k & 0 \\ 0 & \lambda_2^k\end{bmatrix} (a \begin{bmatrix}1\\-1\end{bmatrix}) = a S \begin{bmatrix}\lambda_1^k \\ -\lambda_2^k\end{bmatrix}$.
> Solving for the 2nd component ($F_k$): $F_k = a(1\cdot\lambda_1^k + 1\cdot(-\lambda_2^k)) = \frac{1}{\sqrt{5}}(\lambda_1^k - \lambda_2^k)$.
> [cite_start]*(Note: The text uses $\lambda_2 > \lambda_1$, so signs may swap to match text formula)*[cite: 28, 29].
>
> **(i)**
> [cite_start]Ratio approaches $\phi = \frac{1+\sqrt{5}}{2} \approx 1.618$ (The Golden Ratio)[cite: 31].

---

> [!question] No. 2 Matrix Limits
> **(a)** When does limit diverge?
> **(b)** When is limit zero?
> **(c)** When is limit finite non-zero?

> [!success]- Solution
> **(a) Diverges:** If any eigenvalue $|\lambda_i| > 1$. [cite_start]The powers $\lambda_i^k$ grow consistently[cite: 37].
> **(b) Zeroes:** If all eigenvalues $|\lambda_i| < 1$. [cite_start]The powers $\lambda_i^k \to 0$[cite: 38].
> **(c) Finite Non-Zero:** If the largest eigenvalue is $\lambda = 1$ (and others are $<1$ in magnitude). [cite_start]The component associated with $\lambda=1$ stabilizes while others vanish[cite: 39].

---

> [!question] No. 3 Markov Chain
> **(a)** Prove $\vec{u}_{t}=A\vec{u}_{t-1}$.
> **(b)** Prove $\vec{u}_{t}=A^{k}\vec{u}_{t-k}$.
> **(c) & (d)** Numerical convergence in R.
> **(e)** Relationship between $\vec{u}_{*}$, eigenvector, and R output.

> [!success]- Solution
> **(a)**
> By law of total probability: $P(X_t=i) = \sum_j P(X_t=i | X_{t-1}=j) P(X_{t-1}=j)$. [cite_start]In matrix form, this is $\vec{u}_t = A \vec{u}_{t-1}$[cite: 56].
>
> **(b)**
> [cite_start]Recursive application: $\vec{u}_t = A \vec{u}_{t-1} = A(A \vec{u}_{t-2}) = \dots = A^k \vec{u}_{t-k}$[cite: 57].
>
> **(c) & (d)**
> [cite_start]Regardless of starting state ($\vec{u}_0 = [1,0]^T$ or $[0,1]^T$), the vector converges to the same stationary distribution $\vec{u}_* \approx [0.6, 0.4]^T$ (specifically $[0.625, 0.375]^T$ in snippet for t=4)[cite: 63, 130].
>
> **(e)**
> $\vec{u}_*$ is the eigenvector of $A$ corresponding to $\lambda=1$. [cite_start]In R, `eigen(A)` returns vectors; the first column (normalized) corresponds to value 1. $\vec{u}_*$ is this eigenvector scaled so elements sum to 1[cite: 134, 165].

---

> [!question] No. 4 Matrix Analysis
> **(a)** Solve explicitly for eigenvalues of $A = \begin{bmatrix}.8&.3\\.2&.7\end{bmatrix}$.
> **(b)** Why does case 2(c) apply?
> **(c)** Connection to Perron-Frobenius.

> [!success]- Solution
> **(a)**
> $\det\begin{bmatrix}0.8-\lambda & 0.3 \\ 0.2 & 0.7-\lambda\end{bmatrix} = \lambda^2 - 1.5\lambda + 0.56 - 0.06 = \lambda^2 - 1.5\lambda + 0.5 = 0$.
> $(\lambda - 1)(\lambda - 0.5) = 0$.
> [cite_start]$\lambda_1 = 1, \lambda_2 = 0.5$[cite: 169].
>
> **(b)**
> Since $\lambda_1 = 1$ and $|\lambda_2| = 0.5 < 1$, the matrix powers $A^k$ converge to a non-zero matrix (projecting onto the $\lambda=1$ eigenspace). [cite_start]This matches problem 2(c)[cite: 170].
>
> **(c)**
> The Perron-Frobenius theorem states that for a positive stochastic matrix, there is a unique largest eigenvalue equal to 1, and its corresponding eigenvector (stationary distribution) has strictly positive entries. [cite_start]This guarantees the existence and uniqueness of the steady state found in 3(e)[cite: 171].

---

> [!question] No. 5 No Arbitrage Proof
> Prove $S_{T}^{d} < S_{0}(1+r_{F}T) < S_{T}^{u}$.

> [!success]- Solution
> **Proof by Contradiction (Arbitrage Argument):**
> 1.  **Assume $S_0(1+r_f T) \le S_T^d$:**
>     * Borrow $S_0$ at rate $r_f$ to buy the asset now. Cost at $t=0$ is 0.
>     * At $t=T$, asset value is at least $S_T^d$. Repay loan $S_0(1+r_f T)$.
>     * Profit $\ge S_T^d - S_0(1+r_f T) \ge 0$. Risk-free profit exists (Arbitrage).
> 2.  **Assume $S_0(1+r_f T) \ge S_T^u$:**
>     * Short sell asset for $S_0$, invest proceeds at $r_f$. Cost at $t=0$ is 0.
>     * At $t=T$, investment grows to $S_0(1+r_f T)$. Buy back asset at max price $S_T^u$.
>     * Profit $\ge S_0(1+r_f T) - S_T^u \ge 0$. Risk-free profit exists (Arbitrage).
>
> Therefore, for **No Arbitrage** to hold, the price must lie strictly between the discounted future values:
> [cite_start]$\frac{S_{T}^{d}}{1+r_{F}T} < S_{0} < \frac{S_{T}^{u}}{1+r_{f}T}$[cite: 172, 176].