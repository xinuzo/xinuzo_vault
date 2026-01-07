>[!tips] 6.70 Cauchy's Residue Theorem
>Let $C$ be a simple closed contour, positively oriented. If $f$ is analytic inside and on $C$ except for a finite number of singular points $z_k$ inside $C$:
>$$\int_C f(z) dz = 2\pi i \sum_{k=1}^n \text{Res}_{z=z_k} f(z)$$

>[!tips] 6.73 Formulas for Residues
>1. **Simple Pole**: $\text{Res}_{z=z_0} f(z) = \lim_{z \to z_0} (z - z_0)f(z)$.
>2. **Pole of Order m**:
>$$\text{Res}_{z=z_0} f(z) = \frac{1}{(m-1)!} \lim_{z \to z_0} \frac{d^{m-1}}{dz^{m-1}} [(z - z_0)^m f(z)]$$
>3. **Quotient Form $p(z)/q(z)$**: If $p(z_0) \neq 0, q(z_0) = 0, q'(z_0) \neq 0$, then $\text{Res} = p(z_0)/q'(z_0)$.