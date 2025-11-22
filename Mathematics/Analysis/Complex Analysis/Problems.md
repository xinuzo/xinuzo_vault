> [!question] Problem Statement
> 
> Let $a, b, c, d$ be complex numbers such that $|a| = |b| = |c| = |d| = r > 0$ and:
> 
> $$a + b + c = d$$
> 
> Show that $d = a$ or $d = b$ or $d = c$.

> [!success]- Solution
> 
> 1. Use the Conjugate Property
> 
> Since $|z| = r$, we know $z\bar{z} = r^2$, which implies $\bar{z} = \frac{r^2}{z}$.
> 
> 2. Transform the Equation
> 
> Take the conjugate of the given equation $a + b + c = d$:
> 
> $$\bar{a} + \bar{b} + \bar{c} = \bar{d}$$
> 
> Substitute $\bar{z} = \frac{r^2}{z}$:
> 
> $$\frac{r^2}{a} + \frac{r^2}{b} + \frac{r^2}{c} = \frac{r^2}{d}$$
> 
> Divide by $r^2$ and combine the fractions:
> 
> $$\frac{ab + bc + ca}{abc} = \frac{1}{d} \implies \boxed{d(ab + bc + ca) = abc}$$
> 
> 3. The Polynomial Argument
> 
> Consider the polynomial $P(z)$ with roots $a, b, c$:
> 
> $$P(z) = (z-a)(z-b)(z-c) = z^3 - e_1 z^2 + e_2 z - e_3$$
> 
> Using Vieta's formulas and our derived identities:
> 
> - Sum of roots ($e_1$): $a+b+c = \mathbf{d}$  
>     
> - Product of roots ($e_3$): $abc = \mathbf{d \cdot e_2}$ (from Step 2)
>     
> 
> The polynomial becomes:
> 
> $$P(z) = z^3 - d z^2 + e_2 z - d e_2$$
> 
> 4. Conclusion
> 
> Evaluate $P(z)$ at $z=d$:
> 
> $$P(d) = d^3 - d(d)^2 + e_2(d) - d(e_2) = 0$$
> 
> Since $P(d) = 0$, $d$ must be a root of the polynomial. Since the roots are defined as $\{a, b, c\}$, it follows that:
> 
> $$d \in \{a, b, c\}$$



>[!question] Problem
> Determine the largest open set $\Omega \subseteq \mathbb{C}$ such that the function $f(z) = \text{Ln}(1-z^{2025})$ is analytic on $\Omega$.

>[!success]- Solution
> The principal logarithm $\text{Ln}(w)$ is analytic everywhere except on the branch point $w=0$ and the branch cut along the negative real axis $(-\infty, 0]$.
> 
> Therefore, $f(z)$ is **not** analytic when:
> $$1 - z^{2025} \in (-\infty, 0]$$
> Solving for the singular points:
> $$1 - z^{2025} \leq 0 \implies z^{2025} \geq 1$$
> 
> This condition corresponds to values of $z$ where $z^{2025}$ is a real number greater than or equal to 1. Geometrically, if $z = re^{i\theta}$, this occurs when:
> 1.  $r \geq 1$
> 2.  $2025\theta = 2k\pi \implies \theta_k = \frac{2k\pi}{2025}$ for $k \in \mathbb{Z}$.
> 
> **Conclusion:**
> The largest open set is the complex plane excluding these rays:
> $$\Omega = \mathbb{C} \setminus \{ z \in \mathbb{C} : z^{2025} \in [1, \infty) \}$$