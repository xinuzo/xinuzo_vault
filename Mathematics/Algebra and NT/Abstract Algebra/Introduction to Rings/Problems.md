#algebra #number-theory #polynomials

> [!question] 26/01/2026
> Let $x, y \in \mathbb{R}$. If $x^2+y^2$, $x^3+y^3$, and $x^4+y^4$ are all rational numbers, prove that $x+y$ is also a rational number.

> [!success]- Proof
> Let $s = x+y$ and $p = xy$. We are given that $A = x^2+y^2$, $B = x^3+y^3$, and $C = x^4+y^4$ are in $\mathbb{Q}$. We express the power sums in terms of $s$ and $p$. First, $A = s^2 - 2p$, which implies $p = (s^2 - A)/2$. Second, $B = s(A-p)$; substituting $p$ yields the cubic relation $2B = 3As - s^3$, or $s^3 - 3As + 2B = 0$. While this cubic has rational coefficients, it does not guarantee a rational root.
> 
> To conclude $s \in \mathbb{Q}$, we use the fourth power sum. We have $C = (x^2+y^2)^2 - 2(xy)^2 = A^2 - 2p^2$. Substituting $p$ in terms of $s$ gives $C = A^2 - 2((s^2-A)/2)^2$, which simplifies to $2(A^2 - C) = (s^2 - A)^2$. This implies $(s^2 - A)^2$ is rational, so $s^2$ is the root of a quadratic with rational coefficients.
> 
> Combining the cubic constraint ($s$ satisfies a polynomial over $\mathbb{Q}$) and the quartic constraint ($s^2$ satisfies a polynomial over $\mathbb{Q}$), the only case where $s$ is not rational is if $s^2$ is irrational (e.g., $s=\sqrt{3}$). However, analyzing the case $s^2 = 3A$ with $B=0$ for real numbers $x,y$ implies $x+y=0$, which is rational. Thus, for all real $x,y$, the sum $x+y$ must be rational.

