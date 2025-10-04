**from Hogg Ed.8**

>[!tips] (Definition) Probability Space
>A **probability space** is a triplet $(S, \mathcal{B}, P)$ where:
>1. $S$ is the **sample space**, the set of all possible outcomes.
>2. $\mathcal{B}$ is a **$\sigma$-algebra** of subsets of $S$, called events.
>3. $P$ is a **probability measure**, a function $P: \mathcal{B} \to [0, 1]$ satisfying the Axioms of Probability.

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

- [ ] Hogg Ed 7 1.9.19
> [!success]- Solusi
> Deret Maclaurin untuk $M(t)=(1-t)^{-3}, t<1$  adalah  $\sum_{i=0}^{\infty} \frac{(k)(k+1)}{2}t^{i}.$ 


- [ ] Hogg Ed 7 1.9.21

> [!success]- Solusi
> 

#### Section 1.10
- [ ]   Hogg Ed 7 1.10.2
> [!success]- Solusi
> 

- [ ] Hogg Ed 7 1.10.3
> [!success]- Solusi
> 

- [ ]  Hogg Ed 7 1.10.5
> [!success]- Solusi
> 

- [ ] Hogg Ed 7 1.10.6
> [!success]- Solusi
>