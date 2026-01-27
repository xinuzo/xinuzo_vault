## PSET Mathematics with Application in Finance

> [!question] No. 1 Fibonacci Numbers and Matrix
> **(a)** Show that $\vec{u}_{k+1}=A\vec{u}_{k}$.
> **(b)** Show that $\vec{u}_{k}=A^{k}\vec{u}_{0}$.
> **(c)** Solve for eigenvalues $\lambda_{1}, \lambda_{2}$ of A.
> **(d)** Show that for eigenvalue $\lambda$, the eigenvector is $\vec{s}=[\lambda, 1]^T$.
> **(e)** Compute $S^{-1}$.
> **(f)** Show $A=S\Lambda S^{-1}$.
> **(g)** Compute $\vec{c}=S^{-1}\vec{u}_{0}$ and find constant $a$.
> **(h)** Derive the formula for $F_{k}$.
> **(i)** What is the limiting ratio (Golden Ratio)?

> [!success]- Solution
> **(a)**
> Given $F_{k+2} = F_{k+1} + F_k$:
> $$A\vec{u}_k = \begin{bmatrix}1&1\\1&0\end{bmatrix} \begin{bmatrix}F_{k+1}\\F_k\end{bmatrix} = \begin{bmatrix}F_{k+1}+F_k\\F_{k+1}\end{bmatrix} = \begin{bmatrix}F_{k+2}\\F_{k+1}\end{bmatrix} = \vec{u}_{k+1}$$
>
> **(b)**
> By repeated application:
> $\vec{u}_1 = A\vec{u}_0$
> $\vec{u}_2 = A\vec{u}_1 = A(A\vec{u}_0) = A^2\vec{u}_0$
> Generalizing: $\vec{u}_k = A^k\vec{u}_0$.
>
> **(c)**
> Solve $\det(A-\lambda I) = 0$:
> $(1-\lambda)(-\lambda) - 1 = \lambda^2 - \lambda - 1 = 0$
> Using the quadratic formula: $\lambda_{1,2} = \frac{1 \pm \sqrt{5}}{2}$.
>
> **(d)**
> We need to show $A\begin{bmatrix}\lambda\\1\end{bmatrix} = \lambda\begin{bmatrix}\lambda\\1\end{bmatrix}$.
> LHS: $\begin{bmatrix}1&1\\1&0\end{bmatrix}\begin{bmatrix}\lambda\\1\end{bmatrix} = \begin{bmatrix}\lambda+1\\\lambda\end{bmatrix}$.
> Since $\lambda^2 - \lambda - 1 = 0 \implies \lambda^2 = \lambda+1$.
> RHS: $\lambda\begin{bmatrix}\lambda\\1\end{bmatrix} = \begin{bmatrix}\lambda^2\\\lambda\end{bmatrix} = \begin{bmatrix}\lambda+1\\\lambda\end{bmatrix}$.
> LHS = RHS.
>
> **(e)**
> $S = \begin{bmatrix}\lambda_1 & \lambda_2 \\ 1 & 1\end{bmatrix}$.
> Determinant $\det(S) = \lambda_1 - \lambda_2$.
> $S^{-1} = \frac{1}{\lambda_1 - \lambda_2} \begin{bmatrix}1 & -\lambda_2 \\ -1 & \lambda_1\end{bmatrix}$.
>
> **(f)**
> By definition of diagonalization, if $S$ contains the eigenvectors, then $A = S\Lambda S^{-1}$.
>
> **(g)**
> $\vec{u}_0 = \begin{bmatrix}1\\0\end{bmatrix}$.
> $\vec{c} = S^{-1}\vec{u}_0 = \frac{1}{\lambda_1 - \lambda_2} \begin{bmatrix}1 & -\lambda_2 \\ -1 & \lambda_1\end{bmatrix} \begin{bmatrix}1\\0\end{bmatrix} = \frac{1}{\lambda_1 - \lambda_2} \begin{bmatrix}1\\-1\end{bmatrix}$.
> Thus $\vec{c} = a\begin{bmatrix}1\\-1\end{bmatrix}$ where $a = \frac{1}{\lambda_1 - \lambda_2} = \frac{1}{\sqrt{5}}$ (assuming $\lambda_1 > \lambda_2$).
>
> **(h)**
> $\vec{u}_k = S \Lambda^k \vec{c}$. The second row of $\vec{u}_k$ is $F_k$.
> $F_k = \frac{1}{\sqrt{5}}(\lambda_1^k - \lambda_2^k)$.
>
> **(i)**
> The limiting ratio is the largest eigenvalue, $\phi = \frac{1+\sqrt{5}}{2} \approx 1.618$ (The Golden Ratio).

---

> [!question] No. 2 Matrix Limits
> **(a)** Under what conditions does the limit diverge?
> **(b)** Under what conditions is the limit the zero matrix?
> **(c)** Under what conditions is the limit a finite non-zero matrix?

> [!success]- Solution
> **(a) Diverges:** If any eigenvalue satisfies $|\lambda_i| > 1$.
> **(b) Zero Matrix:** If all eigenvalues satisfy $|\lambda_i| < 1$.
> **(c) Finite Non-Zero:** If the largest eigenvalue is $\lambda = 1$ (and all other eigenvalues have magnitude $< 1$). This leads to a steady state.

---

> [!question] No. 3 Markov Chain Processes
> **(a)** Prove $\vec{u}_{t}=A\vec{u}_{t-1}$.
> **(b)** Prove $\vec{u}_{t}=A^{k}\vec{u}_{t-k}$.
> **(c)** Numerical convergence for $X_0=1$.
> **(d)** Numerical convergence for $X_0=2$.
> **(e)** Relationship between limiting vector and eigenvectors.

> [!success]- Solution
> **(a)**
> Based on the definition of a Markov chain, the probability distribution at time $t$ depends on $t-1$ via the transition matrix $A$.
> $\vec{u}_t = A \vec{u}_{t-1}$.
>
> **(b)**
> By induction: $\vec{u}_t = A \vec{u}_{t-1} = A(A \vec{u}_{t-2}) = \dots = A^k \vec{u}_{t-k}$.
>
> **(c) & (d)**
> (R code omitted).
> Regardless of the starting position ($X_0=1$ or $X_0=2$), the vector $\vec{u}_t$ converges to the same **stationary distribution**:
> $\vec{u}_* \approx \begin{bmatrix} 0.6 \\ 0.4 \end{bmatrix}$.
>
> **(e)**
> The limiting vector $\vec{u}_*$ is the eigenvector of $A$ corresponding to the eigenvalue $\lambda=1$.
> In R, `eigen(A)` returns normalized vectors. The first column corresponds to $\lambda=1$. If you scale that column so the elements sum to 1, you get the stationary distribution $\vec{u}_*$.

---

> [!question] No. 4 Matrix Eigenvalue Analysis
> **(a)** Solve explicitly for the eigenvalues of $A = \begin{bmatrix}.8&.3\\.2&.7\end{bmatrix}$.
> **(b)** Explain why case (c) of problem 2 applies here.
> **(c)** Connection to Perron-Frobenius Theorem.

> [!success]- Solution
> **(a)**
> $\det(A-\lambda I) = (.8-\lambda)(.7-\lambda) - (.2)(.3) = 0$
> $\lambda^2 - 1.5\lambda + 0.56 - 0.06 = 0$
> $\lambda^2 - 1.5\lambda + 0.5 = 0$
> $(\lambda - 1)(\lambda - 0.5) = 0$.
> Eigenvalues are **1** and **0.5**.
>
> **(b)**
> Problem 2(c) applies (finite non-zero limit) because the largest eigenvalue is exactly 1, and the other eigenvalue (0.5) is less than 1 in absolute value. This ensures convergence to a steady state rather than divergence or zero.
>
> **(c)**
> The **Perron-Frobenius Theorem** guarantees that for a positive stochastic matrix (like A), there exists a unique largest eigenvalue $\lambda=1$, and its corresponding eigenvector has strictly positive entries. This explains why a unique stationary probability distribution exists.

---

> [!question] No. 5 One-Period Economy (No Arbitrage)
> Prove that no arbitrage requires:
> $\frac{S_{T}^{d}}{1+r_{F}T}<S_{0}<\frac{S_{T}^{u}}{1+r_{f}T}$.

> [!success]- Solution
> We prove this by showing that violating either inequality allows for **Arbitrage** (risk-free profit).
>
> **Case 1: If $S_{0} \le \frac{S_{T}^{d}}{1+r_{F}T}$ (Price is too low)**
> * **Strategy:** Borrow cash to buy the asset now ($S_0$).
> * **Payoff:** At time $T$, the asset is worth at least $S_T^d$.
> * **Cost:** You repay the loan $S_0(1+r_f T)$, which is $\le S_T^d$.
> * **Result:** You make a non-negative profit with zero initial cost.
>
> **Case 2: If $S_{0} \ge \frac{S_{T}^{u}}{1+r_{f}T}$ (Price is too high)**
> * **Strategy:** Short sell the asset now (receive $S_0$) and invest the cash at $r_f$.
> * **Payoff:** Your cash grows to $S_0(1+r_f T)$.
> * **Cost:** You buy back the asset at time $T$, costing at most $S_T^u$.
> * **Result:** Since your cash $> S_T^u$, you pocket the difference risk-free.
>
> **Conclusion:**
> To prevent these arbitrage opportunities, the current price $S_0$ must be strictly between the discounted best-case and worst-case future values.