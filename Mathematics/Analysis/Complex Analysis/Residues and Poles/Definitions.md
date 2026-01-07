>[!tips] 6.68 Residue
>If $f$ has a singular point $z_0$ (isolated), the residue of $f$ at $z_0$, denoted $\text{Res}_{z=z_0} f(z)$, is the coefficient $b_1$ of the term $1/(z - z_0)$ in the Laurent expansion.
>$$\text{Res}_{z=z_0} f(z) = \frac{1}{2\pi i} \int_C f(z) dz$$

>[!tips] 6.72 Classification of Singularities
>If $f(z) = \sum_{n=0}^\infty a_n(z-z_0)^n + \sum_{n=1}^\infty \frac{b_n}{(z-z_0)^n}$:
>1. **Removable Singularity**: All $b_n = 0$. (Limit exists).
>2. **Pole of order m**: $b_m \neq 0$ and $b_n = 0$ for $n > m$. (Simple pole if $m=1$).
>3. **Essential Singularity**: Infinite number of nonzero $b_n$. (Picard's Theorem applies).

>[!tips] 6.76 Residue at Infinity
>If $f$ is analytic for $|z| > R$, the residue at infinity is defined via the expansion of $f(1/z)$.
>$$\int_{C} f(z) dz = 2\pi i \text{Res}_{z=0} \left[ \frac{1}{z^2} f\left(\frac{1}{z}\right) \right]$$