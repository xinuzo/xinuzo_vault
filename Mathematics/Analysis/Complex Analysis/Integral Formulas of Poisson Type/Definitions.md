>[!tips] 12.134 Poisson Kernel
>For the unit disk ($R=1, r < 1$):
>$$P(r, \theta - \phi) = \frac{1 - r^2}{1 - 2r \cos(\theta - \phi) + r^2}$$
>It acts as an approximate identity (approaches Dirac delta) as $r \to 1^-$.

>[!tips] 12.135 Dirichlet Problem for Disk
>Find a harmonic function $u(r, \theta)$ in the disk $r < R$ such that $u(R, \theta) = F(\theta)$, where $F$ is piecewise continuous.

>[!tips] 12.140 Schwarz Integral Formula
>A formula that recovers an analytic function $f(z) = u + iv$ within a disk from the boundary values of its real part $u$ on the circle.
>$$f(z) = \frac{1}{2\pi i} \int_C \frac{\zeta + z}{\zeta - z} u(\zeta) \frac{d\zeta}{\zeta} + iv(0)$$