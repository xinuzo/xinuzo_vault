>[!tips] Theorem 3.1.4 Hopf's Umlaufsatz
>The total signed curvature of a simple closed curve in $\mathbb{R}^2$ is $\pm 2\pi$.
>$$\int_0^L \kappa_s ds = \pm 2\pi$$
>[cite_start]This implies the tangent vector rotates by exactly $2\pi$ (or $-2\pi$) on going once around the curve. [cite: 1228]

>[!tips] Proposition 3.2.1 Area Formula
>If $\gamma(t) = (x(t), y(t))$ is a positively-oriented simple closed curve with period $T$, the area contained by it is:
>$$\mathcal{A}(\gamma) = \frac{1}{2} \int_0^T (x\dot{y} - y\dot{x}) dt$$
>(Derived from Green's Theorem)[cite_start]. [cite: 1228]

>[!tips] Theorem 3.2.2 Isoperimetric Inequality
>Let $\gamma$ be a simple closed curve with length $L$ and enclosing area $\mathcal{A}$. Then:
>$$\mathcal{A} \le \frac{1}{4\pi} L^2$$
>[cite_start]Equality holds if and only if $\gamma$ is a circle. [cite: 1228]

>[!tips] Proposition 3.2.3 Wirtinger's Inequality
>Let $F: [0, \pi] \to \mathbb{R}$ be a smooth function with $F(0) = F(\pi) = 0$. Then:
>$$\int_0^\pi \left(\frac{dF}{dt}\right)^2 dt \ge \int_0^\pi F(t)^2 dt$$
>Equality holds iff $F(t) = D \sin t$. (Used to prove the Isoperimetric Inequality)[cite_start]. [cite: 1228]

>[!tips] Theorem 3.3.3 Four Vertex Theorem
>Every convex simple closed curve in $\mathbb{R}^2$ has at least four vertices (points where $\dot{\kappa}_s = 0$).
>[cite_start]Example: An ellipse has exactly four vertices (ends of the major and minor axes). [cite: 1229]