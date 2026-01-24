---
tags:
  - math/combinatorics
  - math/algebra
  - paper-notes
  - graph-theory
source: arXiv:2203.01533v1
authors: Swee Hong Chan, Igor Pak
---

# Introduction to the Combinatorial Atlas

> [!abstract] Overview
> This paper introduces the **Combinatorial Atlas** technology to provide elementary, self-contained proofs for deep results in combinatorics and geometry, specifically the **Strong Mason Conjecture** and the **Alexandrov-Fenchel Inequality**. It also connects these concepts to **Lorentzian Polynomials**.

---

## Combinatorial Atlas Structure

The core object is an acyclic digraph equipped with linear algebraic data. This structure is derived from the Hasse diagram of a poset.

> [!definition] Definition: Combinatorial Atlas
> A **Combinatorial Atlas** $\mathbb{A}$ of dimension $d$ consists of an acyclic digraph $\Gamma = (\Omega, \Theta)$ where:
> 1. **Vertices:** Each vertex $v \in \Omega$ is associated with a pair $(M_v, h_v)$:
>    - $M_v$: A symmetric $d \times d$ matrix.
>    - $h_v \in \mathbb{R}_{\ge 0}^d$: A nonnegative vector.
> 2. **Edges:** Outgoing edges from non-sink vertices are labeled with indices $i \in [d]$.
> [cite_start]3. **Maps:** Each edge $e^{\langle i \rangle} = (v, v^{\langle i \rangle})$ is associated with a linear transformation $T^{\langle i \rangle}_v: \mathbb{R}^d \to \mathbb{R}^d$ [cite: 68-72].

### Key Properties

For the machinery to work, the atlas must satisfy specific local properties relating a vertex to its neighbors (children) in the graph.

> [!info] Inheritance Property (Inh)
> For every non-sink vertex $v$, the matrix $M_v$ is determined by its children:
> $$(M_v)_{i} = \langle T^{\langle i \rangle}v, M^{\langle i \rangle} T^{\langle i \rangle} h \rangle$$
> [cite_start]for every $i \in \text{supp}(M)$[cite: 79].

> [!info] Pullback Property (Pull)
> A condition ensuring convexity flows "up" the graph:
> $$\sum_{i \in \text{supp}(M)} h_i \langle T^{\langle i \rangle} v, M^{\langle i \rangle} T^{\langle i \rangle} v \rangle \ge \langle v, M v \rangle$$
> [cite_start]Ideally, this is an equality **(PullEq)** in log-concave settings [cite: 80-84].

---

## 2. The Engine: Local-Global Principle

This is the main theorem allowing us to prove hard global inequalities by checking simple local conditions (usually at the "sink" vertices of the graph).

> [!theorem] Theorem 3.4: Local-Global Principle
> Let $\mathbb{A}$ be a combinatorial atlas satisfying **(Inh)** and **(Pull)**. Let $v$ be a non-sink regular vertex.
> 
> [cite_start]**If** every out-neighbor of $v$ is hyperbolic, **Then** $v$ is also hyperbolic [cite: 99-100].

### What is Hyperbolicity?
A matrix $M$ is **hyperbolic** (satisfies **Hyp**) if:
$$\langle v, Mw \rangle^2 \ge \langle v, Mv \rangle \langle w, Mw \rangle$$
for every $v, w \in \mathbb{R}^d$ such that $\langle w, Mw \rangle > 0$. [cite_start]This is equivalent to the **Hodge-Riemann Relations** or the matrix having **at most one positive eigenvalue** (OPE)[cite: 78, 110].

---

## 3. Application I: Matroids (Strong Mason Conjecture)

The authors use the atlas to prove the **Ultra-log-concavity** of the number of independent sets in a matroid.

> [!example] Setup for Matroids
> - Let $\mathcal{M} = (X, \mathcal{I})$ be a matroid with $|X|=n$.
> - Let $I(k)$ be the number of independent sets of size $k$.
> [cite_start]- The Atlas is built using feasible words in the matroid (similar to a greedoid structure) [cite: 236-238].

> [!success] Theorem 4.8 (Strong Mason Conjecture)
> For a matroid $\mathcal{M}$ and integer $1 \le k < \text{rk}(\mathcal{M})$:
> $$I(k)^2 \ge \left(1 + \frac{1}{k}\right) \left(1 + \frac{1}{n-k}\right) I(k-1) I(k+1)$$
> [cite_start][cite: 366-369].

This improves upon the "Weak" Mason conjecture ($I(k)^2 \ge I(k-1)I(k+1)$) and the standard log-concavity results.

---

## 4. Application II: Geometry (Alexandrov-Fenchel)

The atlas provides an elementary proof of this deep geometric inequality for mixed volumes of convex bodies.

> [!theorem] Theorem 6.2: Alexandrov-Fenchel Inequality
> For convex bodies $A, B, K_1, \dots, K_{n-2} \subset \mathbb{R}^n$:
> $$V(A, B, \mathbf{K})^2 \ge V(A, A, \mathbf{K}) \cdot V(B, B, \mathbf{K})$$
> [cite_start]where $\mathbf{K} = (K_1, \dots, K_{n-2})$ represents the sequence of other bodies [cite: 540-542].

**Proof Strategy:**
1. [cite_start]Construct an atlas where vertices represent mixed volume matrices of polytopes[cite: 691].
2. [cite_start]Verify properties (Inh) and (PullEq) using geometric identities[cite: 710, 727].
3. Apply the Local-Global principle.

---

## 5. Connection to Lorentzian Polynomials

> [!note] Lorentzian Polynomials
> The paper shows that **Lorentzian Polynomials** (introduced by Brändén-Huh) are a special case of the Combinatorial Atlas. 
> 
> [cite_start]For every Lorentzian polynomial $f$, one can construct an atlas $\mathbb{A}$ such that the hyperbolicity of the atlas corresponds to the Hessian of $f$ having the correct signature[cite: 25, 469].

---

## Summary of Techniques

| Concept | Matroid Application | Geometric Application |
| :--- | :--- | :--- |
| **Vertices $\Omega$** | Feasible words $\alpha \in X^*$ | Subspaces/Projections |
| **Matrix $M_v$** | Counts of continuations of words | Mixed volume matrices |
| **Goal** | Bound $I(k)$ (Independent sets) | Bound $V(\cdot)$ (Mixed Volumes) |
| **Result** | Strong Mason Conjecture | Alexandrov-Fenchel |