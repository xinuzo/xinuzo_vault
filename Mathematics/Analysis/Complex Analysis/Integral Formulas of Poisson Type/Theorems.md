>[!tips] 12.134 Poisson Integral Formula (Disk)
>Let $F(\theta)$ be piecewise continuous on $0 \le \theta \le 2\pi$. The harmonic function $u(r, \theta)$ inside the disk $r < R$ with boundary values $F(\theta)$ is:
>$$u(r, \theta) = \frac{1}{2\pi} \int_0^{2\pi} P\left(\frac{r}{R}, \theta - \phi\right) F(\phi) d\phi$$

>[!tips] 12.138 Poisson Integral Formula (Half Plane)
>For the upper half plane $y > 0$, if $F(x)$ is bounded and piecewise continuous:
>$$u(x, y) = \frac{1}{\pi} \int_{-\infty}^\infty \frac{y}{(x - t)^2 + y^2} F(t) dt$$
>Here, the kernel is $\frac{y}{(x-t)^2 + y^2}$.

>[!tips] 12.139 Uniqueness of Solutions
>The solution to the Dirichlet problem given by the Poisson integral formula is unique (under boundedness assumptions for the half-plane case).

>[!tips] 12.141 Neumann Problems
>Integral formulas can also be derived for the Neumann problem (specifying normal derivatives on the boundary), often using harmonic conjugates or modifying the kernel.