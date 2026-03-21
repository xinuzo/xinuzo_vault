# Definitions.md

> [!tip] 74.1 Surface (2-Manifold)
> A **surface** (or 2-manifold) is a Hausdorff space with a countable basis such that each point has a neighborhood that is homeomorphic to an open subset of $\mathbb{R}^2$. A **closed surface** is a surface that is compact and connected.

> [!tip] 74.2 Polygonal Region
> A **polygonal region** in the plane is a closed, compact subspace bounded by a simple closed polygon. We can form quotient spaces by orienting the edges of the polygon and identifying (gluing) them together in pairs.

> [!tip] 74.3 Labeling Scheme (Word)
> A **labeling scheme** or **word** is a sequence of letters (like $a b c a^{-1} b^{-1} c^{-1}$) used to describe how the edges of a polygonal region are glued together. A letter without an exponent indicates a counterclockwise orientation; a letter with a $-1$ exponent indicates a clockwise orientation. 

> [!tip] 74.4 Proper Labeling
> A labeling scheme is called a **proper labeling** if each letter that appears in the word appears exactly twice (either as $a \dots a$ or $a \dots a^{-1}$). This ensures that edges are glued exactly in pairs, creating a valid surface without boundary.

> [!tip] 75.1 Connected Sum
> Let $X$ and $Y$ be disjoint surfaces. The **connected sum** of $X$ and $Y$, denoted $X \# Y$, is formed by removing a small open disk from both $X$ and $Y$, and then gluing the resulting boundary circles together via a homeomorphism.

> [!tip] 77.1 Euler Characteristic
> For a finite complex (like a triangulated surface) with $v$ vertices, $e$ edges, and $f$ faces, the **Euler characteristic** $\chi$ is the integer defined by the alternating sum:
> $$\chi = v - e + f$$