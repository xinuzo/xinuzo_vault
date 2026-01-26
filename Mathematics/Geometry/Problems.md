#geometry #combinatorics #convexity

> [!question] 26/01/2026
> Prove that in any convex pentagon, one can select three diagonals that form a triangle (i.e., satisfy the triangle inequality).

> [!success]- Proof
> We proceed by contradiction. Let the diagonals be $d_1 \ge d_2 \ge d_3 \ge d_4 \ge d_5$. Assume no three diagonals satisfy the triangle inequality. This implies that for the longest pair, $d_1 \ge d_2 + d_3$, or equivalently $d_3 \le d_1 - d_2$. Since the remaining diagonals are even shorter, every diagonal $d_k$ (for $k \ge 3$) must satisfy $d_k \le d_1 - d_2$.
> 
> We utilize the lemma that in any convex quadrilateral, the sum of the diagonals is strictly greater than the sum of any pair of opposite sides ($PQ+RS > PR+QS$). We analyze two cases for the longest diagonals $d_1$ and $d_2$.
> 
> **Case 1: $d_1$ and $d_2$ share a vertex.** Let $d_1 = AC$ and $d_2 = AD$. Consider the quadrilateral $ACDE$ with diagonals $AD$ and $CE$. By the lemma, $AD + CE > AC + DE$. Rearranging for $CE$ gives $CE > AC - AD + DE$. Since $DE > 0$, this implies $CE > d_1 - d_2$. However, $CE$ is a diagonal (one of the "shorter" ones), which contradicts our assumption that all shorter diagonals must be $\le d_1 - d_2$.
> 
> **Case 2: $d_1$ and $d_2$ do not share a vertex (they cross).** Let $d_1 = AC$ and $d_2 = BD$. Consider the quadrilateral $ACDE$ again with diagonals $AD$ and $CE$. The lemma gives $AD + CE > AC + DE$. From our initial assumption, we know the "short" diagonal $CE$ satisfies $CE \le AC - BD$. Substituting this upper bound into the inequality gives $AD + (AC - BD) > AC + DE$, which simplifies to $AD > BD + DE$. This implies $AD > BD$. However, this contradicts our definition that $BD$ ($d_2$) is the second longest diagonal ($BD \ge AD$).
> 
> Since both cases lead to a contradiction, the initial assumption is false, and a triangle must exist.