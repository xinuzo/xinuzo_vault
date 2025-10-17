**from Hogg Ed.8**

>[!tips] (Definition) Probability Space
>A **probability space** is a triplet $(S, \mathcal{B}, P)$ where:
>1. $S$ is the **sample space**, the set of all possible outcomes.
>2. $\mathcal{B}$ is a **$\sigma$-algebra** of subsets of $S$, called events.
>3. $P$ is a **probability measure**, a function $P: \mathcal{B} \to [0, 1]$ satisfying the Axioms of Probability.

> [!tips] (Definition) $\sigma$-algebra
> Let $S$ be a non-empty set. A collection of subsets of $S$, denoted by $\mathcal{B}$, is a **$\sigma$-algebra** if it satisfies three properties:
> 4.  The entire set $S$ is in the collection: $S \in \mathcal{B}$.
> 5.  The collection is **closed under complementation**: If a set $A$ is in $\mathcal{B}$, then its complement $A^c$ is also in $\mathcal{B}$.
> 6.  The collection is **closed under countable unions**: If $A_1, A_2, A_3, \dots$ is a countable sequence of sets in $\mathcal{B}$, then their union $\bigcup_{i=1}^{\infty} A_i$ is also in $\mathcal{B}$.

> [!tips] Definition Measurable Space
> A **measurable space** is a pair $(S, \mathcal{B})$ where:
> 7.  $S$ is a non-empty set.
> 8.  $\mathcal{B}$ is a $\sigma$-algebra on $S$.
>
> The sets contained in $\mathcal{B}$ are called **measurable sets**.

> [!tips] (Definition) Measure
> Given a measurable space $(S, \mathcal{B})$, a **measure** is a function $\mu: \mathcal{B} \to [0, \infty]$ that satisfies two properties:
> 9.  The measure of the empty set is zero: $\mu(\emptyset) = 0$.
> 10.  **Countable Additivity**: For any countable sequence of disjoint sets $A_1, A_2, A_3, \dots$ in $\mathcal{B}$, the measure of their union is the sum of their measures:
>     $$
>     \mu\left(\bigcup_{i=1}^{\infty} A_i\right) = \sum_{i=1}^{\infty} \mu(A_i)
>     $$

> [!tips] (Definition) Measurable Function
> Let $(S_1, \mathcal{B}_1)$ and $(S_2, \mathcal{B}_2)$ be two measurable spaces. A function $f: S_1 \to S_2$ is called a **measurable function** if for every measurable set $E$ in the codomain's $\sigma$-algebra (i.e., $E \in \mathcal{B}_2$), its preimage is a measurable set in the domain's $\sigma$-algebra (i.e., $f^{-1}(E) \in \mathcal{B}_1$).
>[!tips] (Definition) Cumulative Distribution Function (CDF)
>The **Cumulative Distribution Function** (CDF) of a random variable $X$ is the function $F(x)$ defined as:
>$$ F(x) = P(X \le x), \quad \text{for all } x \in \mathbb{R} $$
>The CDF must satisfy three properties:
>- $F(x)$ is a non-decreasing function.
>- $\lim_{x \to \infty} F(x) = 1$ and $\lim_{x \to -\infty} F(x) = 0$.
>- $F(x)$ is continuous from the right.

---
## Types of Random Variables

>[!tips] (Definition) Discrete Random Variable & PMF
>A random variable $X$ is **discrete** if its space is a countable set of points $\{x_1, x_2, \dots\}$.
>
>Its **Probability Mass Function** (PMF), $p(x)$, is defined by:
>$$ p(x) = P(X = x) $$
>The PMF must satisfy:
>1. $0 \le p(x) \le 1$ for all $x$.
>2. $\sum_x p(x) = 1$.

>[!tips] (Definition) Continuous Random Variable & PDF
>A random variable $X$ is **continuous** if its CDF, $F(x)$, is continuous.
>
>Its **Probability Density Function** (PDF), $f(x)$, is a function such that:
>$$ F(x) = \int_{-\infty}^{x} f(t) \, dt $$
>This implies $f(x) = F'(x)$. The PDF must satisfy:
>1. $f(x) \ge 0$ for all $x$.
>2. $\int_{-\infty}^{\infty} f(x) \, dx = 1$.

---
## Expectation and Moments

>[!tips] (Definition) Mathematical Expectation
>The **mathematical expectation** (or expected value) of a function $u(X)$ of a random variable $X$ is denoted by $E[u(X)]$ and defined as:
>- **Discrete case:** $E[u(X)] = \sum_x u(x) p(x)$
>- **Continuous case:** $E[u(X)] = \int_{-\infty}^{\infty} u(x) f(x) \, dx$
>
>The **mean** of $X$ is $\mu = E[X]$.

>[!tips] (Definition) Variance and Standard Deviation
>The **variance** of a random variable $X$ is the second central moment, defined as:
>$$ \sigma^2 = \text{Var}(X) = E[(X-\mu)^2] $$
>A useful computational formula is:
>$$ \text{Var}(X) = E[X^2] - (E[X])^2 $$
>The **standard deviation** is $\sigma = \sqrt{\text{Var}(X)}$.

>[!tips] (Definition) Moment Generating Function (MGF)
>Let $X$ be a random variable such that for some $h>0$, $E[e^{tX}]$ exists for $|t|<h$.
>The **moment generating function** (MGF) is the function $M(t)=E[e^{tX}] \text{, for }|t|<h$.

>[!tips] Theorem: MGF and Moments
>If a random variable $X$ has an MGF $M(t)$, then the $k$-th moment about the origin, $E[X^k]$, is the $k$-th derivative of $M(t)$ evaluated at $t=0$.
>$$ E[X^k] = M^{(k)}(0) $$

---
## Important Inequalities

>[!tips] Theorem: Markov's Inequality
>Let $u(X)$ be a non-negative function of a random variable $X$. If $E[u(X)]$ exists, then for every positive constant $c$:
>$$ P(u(X) \ge c) \le \frac{E[u(X)]}{c} $$

>[!success]- Proof
>We will show the proof for a continuous random variable $X$ with PDF $f(x)$. The proof for the discrete case is analogous, with integrals replaced by sums.
>
>By definition, $E[u(X)] = \int_{-\infty}^{\infty} u(x) f(x) \, dx$.
>
>Let $A = \{x \mid u(x) \ge c\}$. Since $u(x)$ and $f(x)$ are non-negative, we can split the integral:
>$$ E[u(X)] = \int_A u(x) f(x) \, dx + \int_{A^c} u(x) f(x) \, dx \ge \int_A u(x) f(x) \, dx $$
>
>Within the set $A$, we know that $u(x) \ge c$ by definition. Therefore:
>$$ \int_A u(x) f(x) \, dx \ge \int_A c f(x) \, dx = c \int_A f(x) \, dx $$
>
>The integral $\int_A f(x) \, dx$ is, by definition, the probability that $X$ is in the set $A$, which is $P(u(X) \ge c)$.
>
>Combining the inequalities, we have:
>$$ E[u(X)] \ge c \cdot P(u(X) \ge c) $$
>
>Dividing by $c$ (which is positive) gives the desired result:
>$$ P(u(X) \ge c) \le \frac{E[u(X)]}{c} $$

>[!tips] Theorem: Chebyshev's Inequality
>Let the random variable $X$ have a mean $\mu$ and a finite variance $\sigma^2$. Then for every constant $k>0$:
>$$ P(|X-\mu| \ge k\sigma) \le \frac{1}{k^2} $$

>[!success]- Proof
>This is a direct application of Markov's Inequality.
>
>Let the non-negative function be $u(X) = (X-\mu)^2$.
>Let the positive constant be $c = k^2\sigma^2$.
>
>Applying Markov's Inequality $P(u(X) \ge c) \le E[u(X)]/c$:
>$$ P((X-\mu)^2 \ge k^2\sigma^2) \le \frac{E[(X-\mu)^2]}{k^2\sigma^2} $$
>
>The event $(X-\mu)^2 \ge k^2\sigma^2$ is equivalent to the event $|X-\mu| \ge k\sigma$.
>
>By definition, the expected value $E[(X-\mu)^2]$ is the variance, $\sigma^2$.
>
>Substituting these back into the inequality:
>$$ P(|X-\mu| \ge k\sigma) \le \frac{\sigma^2}{k^2\sigma^2} $$
>
>Simplifying the right side gives the final result:
>$$ P(|X-\mu| \ge k\sigma) \le \frac{1}{k^2} $$
### Excercises
#### Section 1.2
- [x] 1.2.1
  > [!question] Problem 1.2.1 (a), (b), (c)
  > Find the union $C1 \cup C2$ and the intersection $C1 \cap C2$ of the two sets $C1$ and
$C2$, where
(a) $C1 = \{0, 1, 2, \}, \, C2 = \{2, 3, 4\}$.
(b) $C1 = \{x : 0 <x< 2\}, C2 = \{x : 1 ≤ x < 3\}$.
(c) $C1 = \{(x, y):0 <x< 2, 1 <y< 2\}, C2 = \{(x, y):1 <x< 3, 1 <y< 3\}$.

>[!success]- Solutions
>(a) It's too ez to see that:
>$C_{1} \cup C_{2}=\{0,1,2,3,4\} \text{ and } C_{1}\cap C_{2}=\{2\}$
> b) same. 
> $C_{1}\cup C_{2}=\{x:0<x<3\} \text{ and }C_{1}\cap C_{2}=\{x:1\leq x<2\}$ 
> (c) at this point I'm just warming up my fingers.
> $C_{1}\cup C_{2}=\{(x,y):0<x<3,1<y<3\} \text{ and } C_{1}\cap C_{2}=\{(x,y):1<x<2, 1<y<2\}$
  
- [x] 1.2.14
 >[!question] Problem
 >To join a certain club, a person must be either a statistician or a math-
ematician or both. Of the 25 members in this club, 19 are statisticians and 16
are mathematicians. How many persons in the club are both a statistician and a
mathematician?

>[!success]- Solutions
>classic.
$$ \begin{align*} |\text{Mathematician} \cap \text{Statistician}| &= |\text{Mathematician}| + |\text{Statistician}| - |\text{Mathematician} \cup \text{Statistician}| \\ &= 19 + 16 - 25 \\ &= 35 - 25 \\ &= 10 \end{align*} $$

#### Section 1.3
[!question]- Hogg Ed 7 1.3.5
> [!success]- Solusi
> 


#### Section 1.4
[!question]- Hogg Ed 7 1.4.1
> [!success]- Solusi
> 


#### Section 1.5
[!question]- Hogg Ed 7 1.5.1
> [!success]- Solusi
> 

#### Section 1.6
[!question]- Hogg Ed 7 1.6.2
> [!success]- Solusi
> 

### Homework 4 (DIKUMPULKAN - Kamis, 9 Oktober 2025)

#### Section 1.7
[!question]- Hogg Ed 7 1.7.5
> [!success]- Solusi
> 

[!question]- Hogg Ed 7 1.7.6
> [!success]- Solusi
> 

[!question]- Hogg Ed 7 1.7.8
> [!success]- Solusi
> 

[!question]- Hogg Ed 7 1.7.9
> [!success]- Solusi
> 

[!question]- Hogg Ed 7 1.7.10
> [!success]- Solusi
> 

[!question]- Hogg Ed 7 1.7.12
> [!success]- Solusi
> 

[!question]- Hogg Ed 7 1.7.14
> [!success]- Solusi
> 

[!question]- Hogg Ed 7 1.7.18
> [!success]- Solusi
> 

[!question]- Hogg Ed 7 1.7.24
> [!success]- Solusi
> 

#### Section 1.9
[!question]- Hogg Ed 7 1.9.2
> [!success]- Solusi
> 

[!question]- Hogg Ed 7 1.9.3
> [!success]- Solusi
> 

[!question]- Hogg Ed 7 1.9.5
> [!success]- Solusi
> 

[!question]- Hogg Ed 7 1.9.6
> [!success]- Solusi
> 

[!question]- Hogg Ed 7 1.9.14
> [!success]- Solusi
> 

[!question]- Hogg Ed 7 1.9.15
> [!success]- Solusi
> 

[!question]- Hogg Ed 7 1.9.17
> [!success]- Solusi
> 

[!question]- Hogg Ed 7 1.9.18
> [!success]- Solusi
> 

- [x] Hogg Ed 7 1.9.19
>[!success]- Solution
> The k-th moment, $E[X^k]$, can be found by identifying the coefficient of $t^k$ in the Maclaurin series expansion of $M(t)$. We use the definitional relationship:
$$ M(t) = \sum_{k=0}^{\infty} E[X^k] \frac{t^k}{k!} $$
We use the generalized binomial series for $(1+x)^\alpha$ where we set $x=-t$ and $\alpha=-3$. The general coefficient for the $t^k$ term is found to be:
$$ \frac{(k+2)(k+1)}{2} $$
This gives the Maclaurin series:
$$ M(t) = (1-t)^{-3} = \sum_{k=0}^{\infty} \frac{(k+2)(k+1)}{2} t^k $$
$$ \frac{E[X^k]}{k!} = \frac{(k+2)(k+1)}{2} $$
Solving for $E[X^k]$:
$$ E[X^k] = k! \cdot \frac{(k+2)(k+1)}{2} $$
Using the property that $(k+2)! = (k+2)(k+1)k!$, we can simplify the expression:
$$ E[X^k] = \frac{(k+2)!}{2} $$
This is the general formula for the k-th moment of the distribution.


>[!question]- Hogg Ed. 8 | 1.9.21
>Let $X$ be a random variable of the discrete type with pmf $p(x)$ that is positive on the nonnegative integers and is equal to zero elsewhere. Show that
>$$ E(X) = \sum_{x=0}^{\infty} [1 − F(x)] $$
>where $F(x)$ is the cdf of $X$.

>[!success]- Solution
>We will prove this by starting from the right-hand side (RHS) and showing that it equals the definition of $E(X)$.
>
>The RHS is $\sum_{x=0}^{\infty} [1 - F(x)]$. By the definition of the CDF, $F(x) = P(X \le x)$, so its complement is $1 - F(x) = P(X > x)$.
>
>$$ \text{RHS} = \sum_{x=0}^{\infty} P(X > x) $$
>
>Let's expand the sum, using $p(k) = P(X=k)$:
>$$
>\begin{align*}
>\text{RHS} &= P(X>0) + P(X>1) + P(X>2) + \dots \\
>&= [p(1)+p(2)+p(3)+\dots] \\
>&+ [p(2)+p(3)+p(4)+\dots] \\
>&+ [p(3)+p(4)+p(5)+\dots] \\
>&+ \dots
>\end{align*}
>$$
>Now, we rearrange the sum by collecting the terms for each $p(k)$:
>- The term $p(1)$ appears 1 time.
>- The term $p(2)$ appears 2 times.
>- The term $p(3)$ appears 3 times.
>- In general, the term $p(k)$ appears $k$ times.
>
>So the sum becomes:
>$$ \text{RHS} = 1 \cdot p(1) + 2 \cdot p(2) + 3 \cdot p(3) + \dots = \sum_{k=1}^{\infty} k \cdot p(k) $$
>This is the definition of the expected value of $X$. We can also write it as $\sum_{k=0}^{\infty} k \cdot p(k)$ since the $k=0$ term is zero.
>$$ \sum_{k=0}^{\infty} k \cdot P(X=k) = E[X] $$
>Thus, the equality is proven.

>[!question]- Hogg Ed. 8 | 1.10.2
>Let $X$ be a random variable such that $P(X \le 0) = 0$ and let $\mu = E(X)$ exist. Show that $P(X \ge 2\mu) \le \frac{1}{2}$.

>[!success]- Solution
>This is a direct application of **Markov's Inequality**.
>
>Markov's Inequality states that for a non-negative random variable $X$ and any constant $c > 0$:
>$$ P(X \ge c) \le \frac{E[X]}{c} $$
>
>In this problem:
>- We are given $P(X \le 0) = 0$, which means $X$ is a non-negative random variable.
>- We are given $\mu = E[X]$.
>- We choose the constant $c = 2\mu$. Assuming $\mu>0$, this constant is positive.
>
>Applying the inequality:
>$$ P(X \ge 2\mu) \le \frac{E[X]}{2\mu} $$
>
>Substituting $E[X] = \mu$:
>$$ P(X \ge 2\mu) \le \frac{\mu}{2\mu} = \frac{1}{2} $$
>The statement is proven.

>[!question]- Hogg Ed. 8 | 1.10.3
>If $X$ is a random variable such that $E(X)=3$ and $E(X^2) = 13$, use Chebyshev’s inequality to determine a lower bound for the probability $P(-2 < X < 8)$.

>[!success]- Solution
>First, we calculate the mean and variance.
>- Mean: $\mu = E[X] = 3$.
>- Variance: $\sigma^2 = \text{Var}(X) = E[X^2] - (E[X])^2 = 13 - 3^2 = 13 - 9 = 4$.
>- Standard Deviation: $\sigma = \sqrt{4} = 2$.
>
>Next, we rewrite the desired probability in terms of its distance from the mean $\mu=3$:
>The interval $(-2, 8)$ is equivalent to $(3-5, 3+5)$. So, the probability can be written as:
>$$ P(-2 < X < 8) = P(|X-3| < 5) $$
>
>Chebyshev's Inequality is stated for the complement event: $P(|X-\mu| \ge k\sigma) \le \frac{1}{k^2}$.
>We relate our interval to this form: $|X-3| \ge 5$.
>Let $k\sigma = 5$. Since $\sigma=2$, we have $2k=5$, which gives $k = 2.5$.
>
>Now apply Chebyshev's Inequality:
>$$ P(|X-3| \ge 5) \le \frac{1}{(2.5)^2} = \frac{1}{6.25} = \frac{4}{25} = 0.16 $$
>
>Finally, we use the complement rule to find the lower bound for the probability of being *inside* the interval:
>$$ P(-2 < X < 8) = P(|X-3| < 5) = 1 - P(|X-3| \ge 5) $$
>Since $P(|X-3| \ge 5) \le \frac{4}{25}$, the smallest the right side can be is $1 - \frac{4}{25}$.
>$$ P(-2 < X < 8) \ge 1 - \frac{4}{25} = \frac{21}{25} $$
>The lower bound is $\frac{21}{25}$ or $0.84$.

>[!question]- Hogg Ed. 8 | 1.10.6
>Let $X$ be a positive random variable; i.e., $P(X \le 0) = 0$. Argue that:
>(a) $E(1/X) \ge 1/E(X)$
>(b) $E[-\log X] \ge -\log[E(X)]$
>(c) $E[\log(1/X)] \ge \log[1/E(X)]$
>(d) $E[X^3] \ge [E(X)]^3$

>[!success]- Solution
>All four inequalities are direct results of **Jensen's Inequality**.
>
>Jensen's Inequality states that for a **convex** function $g(x)$, the following holds:
>$$ E[g(X)] \ge g(E[X]) $$
>A function $g(x)$ is convex if its second derivative, $g''(x)$, is non-negative on its domain. Since $X$ is a positive random variable, we only need to check for $x>0$.
>
>(a) **$E[1/X] \ge 1/E[X]$**
>Let $g(x) = 1/x = x^{-1}$.
>$g'(x) = -x^{-2}$
>$g''(x) = 2x^{-3} = 2/x^3$.
>For $x>0$, $g''(x) > 0$, so $g(x)$ is **convex**. The inequality holds by Jensen's.
>
>(b) **$E[-\log X] \ge -\log[E(X)]$**
>Let $g(x) = -\log(x)$.
>$g'(x) = -1/x$.
>$g''(x) = 1/x^2$.
>For $x>0$, $g''(x) > 0$, so $g(x)$ is **convex**. The inequality holds by Jensen's.
>
>(c) **$E[\log(1/X)] \ge \log[1/E(X)]$**
>Note that $\log(1/X) = -\log(X)$ and $\log(1/E[X]) = -\log(E[X])$. This inequality is identical to part (b) and is therefore true.
>
>(d) **$E[X^3] \ge [E(X)]^3$**
>Let $g(x) = x^3$.
>$g'(x) = 3x^2$.
>$g''(x) = 6x$.
>For $x>0$, $g''(x) > 0$, so $g(x)$ is **convex**. The inequality holds by Jensen's.