# Comprehensive Real Analysis Notes
Based on uploaded lecture materials (Week 1 - Week 9)

---

## Topic 1: Preliminaries (Sets and Functions)
**Source:**,

### 1.1 Functions
> [!info] Definition: Function
> Let $A$ and $B$ be sets. A function $f: A \to B$ is a rule that assigns to each element $x \in A$ exactly one element $f(x) \in B$.
> * $D(f) = A$ is the **domain**.
> * $R(f) = \{f(x) : x \in A\}$ is the **range**.

> [!info] Definition: Types of Functions
> * **Injective (One-to-one):** A function $f: A \to B$ is injective if $\forall x_1, x_2 \in A$, $f(x_1) = f(x_2) \implies x_1 = x_2$.
> * **Surjective (Onto):** A function $f: A \to B$ is surjective if $f(A) = B$. That is, $\forall y \in B, \exists x \in A$ such that $f(x) = y$.
> * **Bijective:** A function is bijective if it is both injective and surjective.

### 1.2 Direct and Inverse Images
> [!info] Definition: Direct and Inverse Images
> Let $f: A \to B$.
> * **Direct Image:** For $E \subseteq A$, the direct image is $f(E) = \{f(x) : x \in E\}$.
> * **Inverse Image:** For $H \subseteq B$, the inverse image is $f^{-1}(H) = \{x \in A : f(x) \in H\}$.

> [!note] Properties of Images
> For sets $E, F \subseteq A$ and $H, G \subseteq B$:
> 1. $f(E \cup F) = f(E) \cup f(F)$
> 2. $f(E \cap F) \subseteq f(E) \cap f(F)$ (Equality holds if $f$ is injective)
> 3. $f^{-1}(H \cup G) = f^{-1}(H) \cup f^{-1}(G)$
> 4. $f^{-1}(H \cap G) = f^{-1}(H) \cap f^{-1}(G)$.

---

## Topic 2: Cardinality of Sets
**Source:**

### 2.1 Finite and Infinite Sets
> [!info] Definition: Finite Set
> A set $S$ is **finite** if it is empty ($\emptyset$) or if there exists a bijection from $S$ onto $\mathbb{N}_n = \{1, 2, ..., n\}$ for some $n \in \mathbb{N}$.

> [!info] Definition: Infinite Set
> A set is **infinite** if it is not finite.

### 2.2 Countability
> [!info] Definition: Denumerable and Countable
> * **Denumerable (Countably Infinite):** A set $S$ is denumerable if there exists a bijection from $S$ onto $\mathbb{N}$ (the set of natural numbers).
> * **Countable:** A set $S$ is countable if it is either finite or denumerable.
> * **Uncountable:** A set is uncountable if it is not countable.

> [!note] Key Theorems on Countability
> 1. The set $\mathbb{N} \times \mathbb{N}$ is denumerable.
> 2. The set of rational numbers $\mathbb{Q}$ is denumerable.
> 3. If $A$ is a countable set and $f: A \to B$ is surjective, then $B$ is countable.

> [!success] Cantor's Theorem
> The set of real numbers $\mathbb{R}$ is uncountable.
> *Proof Strategy:* Uses the diagonalization argument on the interval $[0, 1]$.

---

## Topic 3: The Real Numbers ($\mathbb{R}$)
**Source:**,

### 3.1 Algebraic Properties (Field Axioms)
> [!info] Field Properties
> On the set $\mathbb{R}$, operations $(+)$ and $(\cdot)$ satisfy:
> * **A1/M1 Commutative:** $a+b=b+a$, $ab=ba$.
> * **A2/M2 Associative:** $(a+b)+c = a+(b+c)$, $(ab)c = a(bc)$.
> * **A3/M3 Identity:** Existence of $0$ (additive) and $1$ (multiplicative).
> * **A4/M4 Inverse:** Existence of $-a$ and $1/a$ (for $a \neq 0$).
> * **D Distributive:** $a(b+c) = ab + ac$.

### 3.2 Order Properties
> [!info] Order Axioms
> There exists a subset $\mathbb{P} \subset \mathbb{R}$ (positive numbers) such that:
> 1. If $a, b \in \mathbb{P}$, then $a+b \in \mathbb{P}$.
> 2. If $a, b \in \mathbb{P}$, then $ab \in \mathbb{P}$.
> 3. **Trichotomy:** For any $a \in \mathbb{R}$, exactly one holds: $a \in \mathbb{P}$, $a=0$, or $-a \in \mathbb{P}$.

> [!note] Important Inequalities
> * **Bernoulli's Inequality:** If $x > -1$, then $(1+x)^n \ge 1+nx$ for all $n \in \mathbb{N}$.
> * **Triangle Inequality:** $|a + b| \le |a| + |b|$.
>     * Corollary 1: $||a| - |b|| \le |a - b|$.
>     * Corollary 2: $|a - b| < \epsilon \iff a - \epsilon < b < a + \epsilon$.

### 3.3 The Completeness Property
> [!info] Definitions: Sup and Inf
> Let $S$ be a nonempty subset of $\mathbb{R}$.
> * **Bounded Above:** $\exists u$ such that $s \le u, \forall s \in S$.
> * **Supremum ($\sup S$):** The least upper bound.
> * **Infimum ($\inf S$):** The greatest lower bound.

> [!note] Lemma: Condition for Supremum
> An upper bound $u$ is $\sup S$ if and only if for every $\epsilon > 0$, there exists $s_\epsilon \in S$ such that $u - \epsilon < s_\epsilon$.

> [!success] The Completeness Axiom
> Every nonempty set of real numbers that has an upper bound has a supremum in $\mathbb{R}$.

### 3.4 Applications of Completeness
> [!note] The Archimedean Property
> For any $x \in \mathbb{R}$, there exists $n \in \mathbb{N}$ such that $x < n$.
> * **Corollary:** For any $\epsilon > 0$, there exists $n \in \mathbb{N}$ such that $1/n < \epsilon$.

> [!note] The Density Theorem
> If $x < y$, then there exists a rational number $r \in \mathbb{Q}$ such that $x < r < y$.
> * **Corollary:** Between any two real numbers, there exists an irrational number.

---

## Topic 4: Sequences in $\mathbb{R}$
**Source:**

### 4.1 Convergence
> [!info] Definition: Sequence and Limit
> * A **sequence** $X = (x_n)$ is a function from $\mathbb{N}$ to $\mathbb{R}$.
> * A sequence converges to $x$ ($\lim(x_n) = x$) if:
>   $$\forall \epsilon > 0, \exists K(\epsilon) \in \mathbb{N} \text{ such that } \forall n \ge K(\epsilon), |x_n - x| < \epsilon$$.

> [!info] Definition: Tail of a Sequence
> The $m$-tail of a sequence $X = (x_1, x_2, ...)$ is the sequence $X_m = (x_{m+n} : n \in \mathbb{N}) = (x_{m+1}, x_{m+2}, ...)$.
> * **Theorem:** $X$ converges iff its $m$-tail $X_m$ converges.

### 4.2 Theorems on Limits
> [!note] Uniqueness and Boundedness
> * **Uniqueness:** A sequence can have at most one limit.
> * **Boundedness:** Every convergent sequence is bounded (i.e., $\exists M > 0$ such that $|x_n| \le M, \forall n$).

> [!note] Algebraic Operations on Limits
> If $\lim(x_n) = x$ and $\lim(y_n) = y$, then:
> * $\lim(x_n + y_n) = x + y$
> * $\lim(x_n y_n) = xy$
> * $\lim(x_n / y_n) = x/y$ (provided $y_n \neq 0$ and $y \neq 0$).

> [!success] Squeeze Theorem
> If $a_n \le x_n \le b_n$ for all $n$, and $\lim(a_n) = \lim(b_n) = L$, then $\lim(x_n) = L$.

---

## Topic 5: Monotone Sequences and Subsequences
**Source:**

### 5.1 Monotone Convergence
> [!info] Definition: Monotonicity
> * **Increasing:** $x_1 \le x_2 \le ... \le x_n \le ...$
> * **Decreasing:** $x_1 \ge x_2 \ge ... \ge x_n \ge ...$
> A sequence is **monotone** if it is either increasing or decreasing.

> [!success] Monotone Convergence Theorem (MCT)
> A monotone sequence is convergent if and only if it is bounded.
> * If $(x_n)$ is increasing and bounded above, $\lim(x_n) = \sup\{x_n\}$.
> * If $(x_n)$ is decreasing and bounded below, $\lim(x_n) = \inf\{x_n\}$.

### 5.2 Subsequences
> [!info] Definition: Subsequence
> Given a sequence $X=(x_n)$ and strictly increasing indices $n_1 < n_2 < ...$, the sequence $X' = (x_{n_k})$ is a subsequence of $X$.
> * **Theorem:** If $X$ converges to $x$, then every subsequence $X'$ also converges to $x$.

> [!success] Bolzano-Weierstrass Theorem
> Every bounded sequence of real numbers has a convergent subsequence.

---

## Topic 6: Cauchy Sequences
**Source:**

### 6.1 Cauchy Criterion
> [!info] Definition: Cauchy Sequence
> A sequence $(x_n)$ is a Cauchy sequence if:
> $\forall \epsilon > 0, \exists H(\epsilon) \in \mathbb{N}$ such that $\forall n, m \ge H(\epsilon)$, $|x_n - x_m| < \epsilon$.

> [!note] Lemma
> If a sequence is convergent, it is a Cauchy sequence.
> If a sequence is Cauchy, it is bounded.

> [!success] Cauchy Convergence Criterion
> A sequence of real numbers is convergent if and only if it is a Cauchy sequence.

### 6.2 Properly Divergent Sequences
> [!info] Definition: Infinite Limits
> * $\lim(x_n) = +\infty$ if $\forall M > 0, \exists K$ s.t. $x_n > M$ for all $n \ge K$.
> * $\lim(x_n) = -\infty$ if $\forall M < 0, \exists K$ s.t. $x_n < M$ for all $n \ge K$.

---

## Topic 7: Infinite Series
**Source:**

> [!info] Definitions
> * **Infinite Series:** Represented as $\sum x_n$.
> * **Partial Sums:** $s_k = x_1 + x_2 + ... + x_k$.
> * **Convergence:** The series $\sum x_n$ converges iff the sequence of partial sums $(s_k)$ converges.

> [!note] Geometric Series
> The series $\sum_{n=0}^{\infty} r^n$ converges if and only if $|r| < 1$.
> If convergent, the sum is $\frac{1}{1-r}$.

> [!note] n-th Term Test for Divergence
> If the series $\sum x_n$ converges, then $\lim(x_n) = 0$.
> **Important:** The converse is false (e.g., Harmonic Series $\sum 1/n$ diverges even though $\lim(1/n)=0$).

> [!success] Cauchy Criterion for Series
> $\sum x_n$ converges iff $\forall \epsilon > 0, \exists M$ such that if $m > n \ge M$, then $|s_m - s_n| = |x_{n+1} + ... + x_m| < \epsilon$.

---

## Topic 8: Limits of Functions
**Source:**

### 8.1 Definition
> [!info] Cluster Point
> A point $c$ is a **cluster point** of $A \subseteq \mathbb{R}$ if every $\delta$-neighborhood of $c$ contains at least one point of $A$ distinct from $c$.

> [!info] The $\epsilon-\delta$ Definition of Limit
> Let $f: A \to \mathbb{R}$ and $c$ be a cluster point of $A$. $\lim_{x \to c} f(x) = L$ if:
> $\forall \epsilon > 0, \exists \delta > 0$ such that if $x \in A$ and $0 < |x - c| < \delta$, then $|f(x) - L| < \epsilon$.

### 8.2 Sequential Criterion
> [!success] Sequential Criterion
> $\lim_{x \to c} f(x) = L$ if and only if for every sequence $(x_n)$ in $A \setminus \{c\}$ that converges to $c$, the sequence $(f(x_n))$ converges to $L$.

> [!note] Divergence Criterion
> The limit does not exist if there exists a sequence $(x_n) \to c$ ($x_n \neq c$) such that sequence $(f(x_n))$ does not converge.