# Combinatorial Atlas & Matroid Log-Concavity

**Tags:** #combinatorics #matroids #linear-algebra #log-concavity #spectral-graph-theory
[cite_start]**Source:** Chan & Pak, "Introduction to the Combinatorial Atlas" [cite: 1]

---

## 1. Matroid Fundamentals
[cite_start]A **Matroid** $\mathcal{M} = (X, \mathcal{I})$ consists of a ground set $X$ (size $n$) and a collection of independent sets $\mathcal{I} \subseteq 2^X$ satisfying two properties[cite: 199]:

1.  [cite_start]**Hereditary Property:** If $T \in \mathcal{I}$ and $S \subset T$, then $S \in \mathcal{I}$[cite: 200].
2.  **Exchange Property:** If $S, T \in \mathcal{I}$ and $|S| [cite_start]< |T|$, there exists $x \in T \setminus S$ such that $S \cup \{x\} \in \mathcal{I}$[cite: 201].

**Key Definitions:**
* [cite_start]**Rank:** $rk(\mathcal{M}) := \max_{S \in \mathcal{I}} |S|$[cite: 202].
* [cite_start]**Independent Set Count:** $I(k)$ denotes the number of independent sets of size $k$[cite: 203].

---

## 2. The Log-Concavity Conjectures (Mason's Conjectures)
The paper addresses the behavior of the sequence $I(k)$. The sequence is "ultra-log-concave," meaning it satisfies specific quadratic inequalities.

### Weak Mason Conjecture (Log-concavity)
$$I(k)^2 \ge I(k-1)I(k+1)$$
[cite_start]*Established by Adiprasito, Huh, and Katz[cite: 215].*

### Strong/Ultra Mason Conjecture
[cite_start]The "Combinatorial Atlas" provides an elementary proof for the **Ultra-log-concavity** of matroids (formerly the Strong Mason Conjecture)[cite: 366]:

$$I(k)^2 \ge \left(1+\frac{1}{k}\right)\left(1+\frac{1}{n-k}\right)I(k-1)I(k+1)$$
[cite_start]*For $1 \le k < rk(\mathcal{M})$[cite: 369].*

---

## 3. The Combinatorial Atlas Framework
The **Combinatorial Atlas** is a linear-algebraic framework used to prove these inequalities. [cite_start]It generalizes techniques used for Lorentzian polynomials and the Alexandrov-Fenchel inequality[cite: 13, 25].

### Structure
An atlas $\mathbb{A}$ is an acyclic digraph $\Gamma = (\Omega, \Theta)$ where:
* [cite_start]**Vertices ($v$):** Associated with a symmetric matrix $M_v$ (nonnegative diagonals) and a vector $h_v \in \mathbb{R}_{\ge 0}^d$[cite: 69].
* [cite_start]**Edges ($e^{\langle i \rangle}$):** Associated with a linear transformation $T^{\langle i \rangle}: \mathbb{R}^d \to \mathbb{R}^d$[cite: 72].


### Key Properties
To prove log-concavity, the Atlas must satisfy specific conditions:

1.  **Hyperbolic Property (Hyp):** A vertex is hyperbolic if its matrix $M$ satisfies the reverse Cauchy-Schwarz inequality on the positive cone:
    $$\langle v, Mw \rangle^2 \ge \langle v, Mv \rangle \langle w, Mw \rangle$$
    [cite_start]*Provided $\langle w, Mw \rangle > 0$[cite: 78].*

2.  **Inheritance Property (Inh):** Relates a vertex to its children:
    $$(M_v)_{i} = \langle T^{\langle i \rangle}v, M^{\langle i \rangle} T^{\langle i \rangle} h \rangle$$
    [cite_start]*For every $i$ in the support[cite: 79].*

3.  **Pullback Property (PullEq):** A relationship ensuring the hyperbolic property propagates upwards from children to parents:
    $$\sum h_i \langle T^{\langle i \rangle}v, M^{\langle i \rangle} T^{\langle i \rangle} v \rangle = \langle v, Mv \rangle$$
    [cite_start]*[cite: 86].*

### The Local-Global Principle
This is the core theorem of the framework.
> [!THEOREM] Local-Global Principle
> [cite_start]If an atlas satisfies **Inheritance** and **Pullback**, and if the out-neighbors of a regular vertex $v$ are **Hyperbolic**, then $v$ is also **Hyperbolic** [cite: 99-100].

[cite_start]This allows reducing global inequalities (at the root of the Atlas) to checking simple conditions at the sink vertices[cite: 101].

---

## 4. Application to Matroids
To apply this to Matroids, the paper constructs a specific Atlas where:
* [cite_start]**Vertices** represent "feasible words" (ordered independent sets)[cite: 220, 238].
* [cite_start]**Matrices ($M_v$)** encode counts of continuations of these words [cite: 262-264].
* [cite_start]The **Hyperbolicity** of the root vertex implies the Ultra-log-concavity inequality for the matroid[cite: 362].

### Connection to Other Concepts
* [cite_start]**Lorentzian Polynomials:** The theory of Lorentzian polynomials is a special case of the Combinatorial Atlas[cite: 25].
* [cite_start]**Alexandrov-Fenchel Inequality:** The Atlas framework also yields a self-contained proof of this classical geometric inequality regarding mixed volumes[cite: 34, 542].