
## Problem 1: Random Walk with Bias
> [!question] **Problem Statement**
> Let $X_n$ be i.i.d steps where $P(+1)=p$, $P(-1)=q$, $P(0)=1-(p+q)$. Let $S_n = \sum X_i$.
> **(a)** Derive MGF, Mean, and Variance of step $X_i$.
> **(b)** Derive MGF, Mean, and Variance of sum $S_n$.
> **(c)** Prove convergence to Normal distribution.
> **(d)** For a 78-step intra-day model with $p=0.52, q=0.47$, find step size $\Delta$ for expected daily change of $+\$0.50$.

> [!success]- **Solution**
> **(a) Step Statistics**
> * **MGF:** $M_{X_i}(t) = E[e^{tX}] = pe^t + (1-p-q) + qe^{-t}$
> * **Mean:** $E[X_i] = p(1) + q(-1) = p-q$
> * **Variance:** $E[X_i^2] - (E[X_i])^2 = (p+q) - (p-q)^2$
>
> **(b) Random Walk Statistics ($S_n$)**
> * **MGF:** Since i.i.d, $M_{S_n}(t) = [M_{X_i}(t)]^n = (pe^t + 1-p-q + qe^{-t})^n$
> * **Mean:** $E[S_n] = n E[X_i] = n(p-q)$
> * **Variance:** $Var(S_n) = n Var(X_i) = n[(p+q) - (p-q)^2]$
>
> **(c) Convergence**
> * Since $S_n$ is a sum of $n$ i.i.d. variables with finite mean and variance, by the **Central Limit Theorem**, the standardized variable $Z_n = \frac{S_n - n\mu}{\sigma \sqrt{n}}$ converges in distribution to $N(0,1)$ as $n \to \infty$.
>
> **(d) Step Size Calculation**
> * Let step size be $\Delta$. Expected daily return is $E[S_{78}] = 78 \cdot \Delta \cdot (p-q)$.
> * $0.50 = 78 \cdot \Delta \cdot (0.52 - 0.47) \implies 0.50 = 3.9 \Delta$.
> * $\Delta = \frac{0.50}{3.9} \approx \mathbf{0.1282}$ (approx 13 cents).

---

## Problem 2: Lognormal Assets & Call Options
> [!question] **Problem Statement**
> **Part 1:** Asset price $S_t = S_0 X$, where $X \sim \text{Lognormal}(\mu=t \ln 1.15, \sigma=\sqrt{t} \ln 1.3)$. Find Mean/SD of returns for $t=1, 0.25, 0.083$.
> **Part 2:** Prove Call Option Payoff $E[(X-K)^+] = e^{\mu+\sigma^2/2}\Phi(d_1) - K\Phi(d_2)$.
> **Part 3:** Calculate expected payoff for $S_0=100$ at $t=1/12, 3/12, 1$ for Strikes $K=100, 120$.

> [!success]- **Solution**
> **Part 1: Mean & SD of Lognormal Returns**
> Using formulas $E[X] = e^{\mu+\sigma^2/2}$ and $SD(X) = E[X]\sqrt{e^{\sigma^2}-1}$:
> * **1 Year ($t=1$):** Mean $\approx 1.19$, SD $\approx 0.31$
> * **3 Months ($t=0.25$):** Mean $\approx 1.04$, SD $\approx 0.14$
> * **1 Month ($t \approx 0.08$):** Mean $\approx 1.01$, SD $\approx 0.08$
>
> **Part 2: Black-Scholes Proof Sketch**
> * Integral split: $E = \int_K^\infty x f(x)dx - K \int_K^\infty f(x)dx$.
> * **Term 2:** $P(X>K) = P(\ln X > \ln K)$. Standardizing gives $\Phi(\frac{\mu-\ln K}{\sigma})$.
> * **Term 1:** Substitute $y = \ln x$. The exponent completes the square to a shifted mean $(\mu + \sigma^2)$. The constant $e^{\mu+\sigma^2/2}$ factors out.
> * Result: $e^{\mu+\sigma^2/2}\Phi(d_1) - K\Phi(d_2)$.
>
> **Part 3: Payoff Calculation ($S_0=100$)**
> | Horizon | Strike $K=100$ (ATM) | Strike $K=120$ (OTM) |
> | :--- | :--- | :--- |
> | **1 Month** | **$3.83** | **$0.04** |
> | **3 Months** | **$7.86** | **$1.09** |
> | **1 Year** | **$23.35** | **$11.99** |
> * *Comment:* Value increases with time due to volatility; OTM options gain exponentially more value from time than ATM options.

---

## Problem 3: Principal Components
> [!question] **Problem Statement**
> **(a)** Show Mean and Variance for portfolio $Y = \vec{w}^T \vec{X}$.
> **(b)** Prove $\Sigma$ is Positive Semi-Definite (PSD).
> **(c)** If $\Sigma_{ij} > 0$, prove $\lambda_{MAX}$ has multiplicity 1 and positive eigenvector $\vec{v}$.
> **(d)** Formula, Mean, and Variance for first Principal Component $PC_1$.

> [!success]- **Solution**
> **(a) Portfolio Stats**
> * **Mean:** $E[\vec{w}^T \vec{X}] = \vec{w}^T E[\vec{X}] = \mathbf{\vec{w}^T \vec{\mu}}$ (Linearity).
> * **Variance:** $Var(\sum w_i X_i) = \sum \sum w_i w_j Cov(X_i, X_j) = \mathbf{\vec{w}^T \Sigma \vec{w}}$.
>
> **(b) PSD Proof**
> * Let $Z$ be any linear combination $Z = \vec{z}^T \vec{X}$.
> * By part (a), $Var(Z) = \vec{z}^T \Sigma \vec{z}$.
> * By definition of variance, $Var(Z) = E[(Z-\mu)^2] \ge 0$.
> * Since $\vec{z}^T \Sigma \vec{z} \ge 0$ for any vector $\vec{z}$, $\Sigma$ is **Positive Semi-Definite**.
>
> **(c) Perron-Frobenius**
> * Since $\Sigma$ has strictly positive entries ($\Sigma_{ij} > 0$), the **Strong Perron-Frobenius Theorem** applies.
> * This guarantees a unique dominant eigenvalue $\lambda_{MAX}$ (multiplicity 1) and an associated eigenvector $\vec{v}$ with strictly positive components ($v_i > 0$).
>
> **(d) First Principal Component**
> * **Formula:** $PC_1 = \vec{v}^T (\vec{X} - \vec{\mu})$
> * **Mean:** $E[\vec{v}^T (\vec{X} - \vec{\mu})] = \vec{v}^T (\vec{\mu} - \vec{\mu}) = \mathbf{0}$.
> * **Variance:** $Var(PC_1) = \vec{v}^T \Sigma \vec{v} = \vec{v}^T (\lambda_{MAX} \vec{v}) = \lambda_{MAX}(\vec{v}^T \vec{v}) = \mathbf{\lambda_{MAX}}$ (assuming normalized $\vec{v}$).