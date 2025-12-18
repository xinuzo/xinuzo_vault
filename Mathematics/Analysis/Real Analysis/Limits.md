# Comprehensive Real Analysis Notes (Part 2)
Based on uploaded lecture materials (Week 10 - Week 15)

---

## Topic 9: Continuous Functions
**Source:**,

### 9.1 Continuity at a Point
> [!info] Definition 5.1.1: Continuity
> Let $A \subseteq \mathbb{R}$, $f: A \to \mathbb{R}$, and $c \in A$. We say $f$ is **continuous at** $c$ if:
> $\forall \epsilon > 0, \exists \delta > 0$ such that if $x \in A$ and $|x - c| < \delta$, then $|f(x) - f(c)| < \epsilon$.

> [!success] Theorem 5.1.3: Sequential Criterion for Continuity
> A function $f: A \to \mathbb{R}$ is continuous at $c \in A$ if and only if for every sequence $(x_n)$ in $A$ that converges to $c$, the sequence $(f(x_n))$ converges to $f(c)$.

> [!note] Discontinuity Criterion (5.1.4)
> $f$ is discontinuous at $c$ if there exists a sequence $(x_n) \to c$ such that $(f(x_n))$ does not converge to $f(c)$.

### 9.2 Combinations of Continuous Functions
> [!info] Algebraic Combinations (5.2.1)
> If $f$ and $g$ are continuous at $c$, then:
> * $f + g$, $f - g$, $fg$, and $bf$ (scalar multiple) are continuous at $c$.
> * $f/g$ is continuous at $c$ provided $g(c) \neq 0$.

> [!note] Composition (5.2.6)
> If $f$ is continuous at $c$ and $g$ is continuous at $f(c)$, then the composition $g \circ f$ is continuous at $c$.

### 9.3 Continuous Functions on Intervals
> [!info] Definition 5.3.1: Bounded Function
> A function $f: A \to \mathbb{R}$ is bounded on $A$ if there exists $M > 0$ such that $|f(x)| \le M$ for all $x \in A$.

> [!success] Theorem 5.3.2: Boundedness Theorem
> If $I = [a, b]$ is a closed bounded interval and $f: I \to \mathbb{R}$ is continuous on $I$, then $f$ is bounded on $I$.

> [!success] Theorem 5.3.4: Maximum-Minimum Theorem
> If $I = [a, b]$ is a closed bounded interval and $f: I \to \mathbb{R}$ is continuous, then $f$ has an absolute maximum and an absolute minimum on $I$.
> * i.e., $\exists x^*, x_* \in I$ such that $f(x_*) \le f(x) \le f(x^*)$ for all $x \in I$.

> [!success] Theorem 5.3.7: Bolzano's Intermediate Value Theorem (IVT)
> Let $I$ be an interval and $f: I \to \mathbb{R}$ be continuous. If $a, b \in I$ with $a < b$ and $k \in \mathbb{R}$ satisfies $f(a) < k < f(b)$, then there exists $c \in (a, b)$ such that $f(c) = k$.
> * **Corollary (Preservation of Intervals):** The image of a closed bounded interval under a continuous function is a closed bounded interval.

### 9.4 Uniform Continuity
> [!info] Definition 5.4.1: Uniform Continuity
> Let $A \subseteq \mathbb{R}$ and $f: A \to \mathbb{R}$. $f$ is **uniformly continuous** on $A$ if:
> $\forall \epsilon > 0, \exists \delta(\epsilon) > 0$ such that $\forall u, v \in A$, if $|u - v| < \delta$, then $|f(u) - f(v)| < \epsilon$.
> * **Key difference:** $\delta$ depends only on $\epsilon$, not on the point $c$.

> [!note] Non-Uniform Continuity Criterion (5.4.2)
> $f$ is NOT uniformly continuous if $\exists \epsilon_0 > 0$ and two sequences $(x_n), (u_n)$ in $A$ such that $\lim(x_n - u_n) = 0$ but $|f(x_n) - f(u_n)| \ge \epsilon_0$.

> [!success] Theorem 5.4.3: Uniform Continuity Theorem
> Let $I$ be a **closed and bounded interval** and $f: I \to \mathbb{R}$ be continuous on $I$. Then $f$ is uniformly continuous on $I$.

> [!info] Lipschitz Functions (5.4.4)
> $f$ is a Lipschitz function on $A$ if $\exists K > 0$ such that $|f(x) - f(u)| \le K|x - u|$ for all $x, u \in A$.
> * **Theorem 5.4.5:** If $f$ is a Lipschitz function, then $f$ is uniformly continuous.

---

## Topic 10: Derivatives
**Source:**,

### 10.1 The Derivative
> [!info] Definition 6.1.1: Derivative
> Let $I \subseteq \mathbb{R}$ be an interval, $f: I \to \mathbb{R}$, and $c \in I$. The derivative of $f$ at $c$, denoted $f'(c)$, is:
> $$f'(c) = \lim_{x \to c} \frac{f(x) - f(c)}{x - c}$$
> provided the limit exists.

> [!note] Theorem 6.1.2: Continuity
> If $f$ is differentiable at $c$, then $f$ is continuous at $c$.

> [!info] Theorem 6.1.6: Chain Rule
> If $f$ is differentiable at $c$ and $g$ is differentiable at $f(c)$, then $g \circ f$ is differentiable at $c$ and:
> $$(g \circ f)'(c) = g'(f(c)) \cdot f'(c)$$.

### 10.2 Mean Value Theorems
> [!success] Theorem 6.2.3: Rolle's Theorem
> Let $f$ be continuous on $[a, b]$ and differentiable on $(a, b)$ with $f(a) = f(b) = 0$. Then there exists $c \in (a, b)$ such that $f'(c) = 0$.

> [!success] Theorem 6.2.4: Mean Value Theorem (MVT)
> Let $f$ be continuous on $[a, b]$ and differentiable on $(a, b)$. Then there exists $c \in (a, b)$ such that:
> $$f(b) - f(a) = f'(c)(b - a)$$.

> [!note] Consequences of MVT
> * If $f'(x) = 0$ for all $x \in I$, then $f$ is constant on $I$ (Thm 6.2.5).
> * If $f'(x) > 0$ for all $x \in I$, then $f$ is strictly increasing on $I$ (Thm 6.2.7).

### 10.3 Taylor's Theorem
> [!success] Theorem 6.4.1: Taylor's Theorem
> Let $n \in \mathbb{N}$, $I = [a, b]$, and $f: I \to \mathbb{R}$ such that $f, f', ..., f^{(n)}$ are continuous on $I$ and $f^{(n+1)}$ exists on $(a, b)$.
> If $x_0 \in I$, then for any $x \in I$, there exists $c$ between $x$ and $x_0$ such that:
> $$f(x) = P_n(x) + R_n(x)$$
> where:
> * $P_n(x) = \sum_{k=0}^n \frac{f^{(k)}(x_0)}{k!} (x - x_0)^k$ (Taylor Polynomial)
> * $R_n(x) = \frac{f^{(n+1)}(c)}{(n+1)!} (x - x_0)^{n+1}$ (Remainder).

---

## Topic 11: The Riemann Integral
**Source:**,,

### 11.1 Definition of Riemann Integral
> [!info] Definition 7.1.1: Partition
> A **partition** of interval $I = [a, b]$ is a set $P = \{x_0, x_1, ..., x_n\}$ where $a = x_0 < x_1 < ... < x_n = b$.
> * **Tags:** Points $t_i$ chosen such that $t_i \in [x_{i-1}, x_i]$.
> * **Tagged Partition ($\dot{P}$):** A partition with chosen tags $\dot{P} = \{(I_i, t_i)\}_{i=1}^n$.

> [!info] Definition 7.1.2: Riemann Sum
> Given a function $f: [a, b] \to \mathbb{R}$ and a tagged partition $\dot{P}$, the Riemann Sum is:
> $$S(f; \dot{P}) = \sum_{i=1}^n f(t_i)(x_i - x_{i-1})$$.

> [!info] Definition 7.1.4: Riemann Integrable
> A function $f$ is **Riemann Integrable** on $[a, b]$ ($f \in \mathcal{R}[a, b]$) if there exists a number $L \in \mathbb{R}$ such that:
> $\forall \epsilon > 0, \exists \delta > 0$ such that for any tagged partition $\dot{P}$ with norm $||\dot{P}|| < \delta$,
> $$|S(f; \dot{P}) - L| < \epsilon$$
> In this case, $\int_a^b f = L$.

> [!note] Theorem 7.1.6: Boundedness
> If $f \in \mathcal{R}[a, b]$, then $f$ is bounded on $[a, b]$.

### 11.2 Integrability Criteria
> [!success] Theorem 7.2.1: Cauchy Criterion
> $f \in \mathcal{R}[a, b]$ if and only if:
> $\forall \epsilon > 0, \exists \eta_\epsilon > 0$ such that if $\dot{P}$ and $\dot{Q}$ are tagged partitions with norm $< \eta_\epsilon$, then $|S(f; \dot{P}) - S(f; \dot{Q})| < \epsilon$.

> [!success] Theorem 7.2.3: Squeeze Theorem
> $f \in \mathcal{R}[a, b]$ if and only if $\forall \epsilon > 0$, there exist functions $\alpha_{\epsilon}$ and $\omega_{\epsilon}$ in $\mathcal{R}[a, b]$ such that:
> 1. $\alpha_{\epsilon}(x) \le f(x) \le \omega_{\epsilon}(x)$ for all $x \in [a, b]$.
> 2. $\int_a^b (\omega_{\epsilon} - \alpha_{\epsilon}) < \epsilon$.

> [!note] Classes of Integrable Functions
> * **Step Functions:** Are integrable (Thm 7.2.5).
> * **Continuous Functions:** Are integrable (Thm 7.2.7).
> * **Monotone Functions:** Are integrable (Thm 7.2.8).

> [!note] Theorem 7.2.9: Additivity Theorem
> If $f \in \mathcal{R}[a, b]$ and $c \in (a, b)$, then $f \in \mathcal{R}[a, c]$ and $f \in \mathcal{R}[c, b]$, and:
> $$\int_a^b f = \int_a^c f + \int_c^b f$$.

### 11.3 The Fundamental Theorem of Calculus (FTC)
> [!success] Theorem 7.3.1: FTC (First Form)
> Let $f \in \mathcal{R}[a, b]$ and define $F(x) = \int_a^x f(t) dt$ for $x \in [a, b]$.
> If $f$ is continuous at $c \in [a, b]$, then $F$ is differentiable at $c$ and $F'(c) = f(c)$.

> [!success] Theorem 7.3.5: FTC (Second Form)
> Let $f \in \mathcal{R}[a, b]$. If there exists a function $F: [a, b] \to \mathbb{R}$ such that $F'(x) = f(x)$ for all $x \in [a, b]$ (i.e., $F$ is an antiderivative), then:
> $$\int_a^b f(x) dx = F(b) - F(a)$$.

> [!info] Theorem 7.3.8: Substitution Theorem
> Let $J = [\alpha, \beta]$ and $\phi: J \to \mathbb{R}$ have a continuous derivative on $J$. If $f$ is continuous on an interval containing $\phi(J)$, then:
> $$\int_\alpha^\beta f(\phi(t)) \cdot \phi'(t) dt = \int_{\phi(\alpha)}^{\phi(\beta)} f(x) dx$$.