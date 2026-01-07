>[!tips] 6.1 First Fundamental Form ($I$)
>A quadratic form on the tangent plane $T_P S$ that allows calculation of lengths and angles on the surface.
>If $\mathbf{v} = \lambda \sigma_u + \mu \sigma_v$ is a tangent vector:
>$$I(\mathbf{v}) = ||\mathbf{v}||^2 = E\lambda^2 + 2F\lambda\mu + G\mu^2$$
>Coefficients: $E = \sigma_u \cdot \sigma_u$, $F = \sigma_u \cdot \sigma_v$, $G = \sigma_v \cdot \sigma_v$.
>

>[!tips] 6.2 Isometry
>A map between surfaces $f: S_1 \to S_2$ is an isometry if it preserves the lengths of all curves.
>Locally, this means the first fundamental forms are identical in corresponding charts ($E_1=E_2, F_1=F_2, G_1=G_2$).

>[!tips] 6.3 Conformal Map
>A map that preserves angles between tangent vectors.
>Condition: The first fundamental forms are proportional ($E_1 = \lambda E_2$, etc.).

>[!tips] 6.4 Area Element
>The area of a region $R$ on a surface patch $\sigma$ is:
>$$\text{Area}(R) = \iint_R ||\sigma_u \times \sigma_v|| du dv = \iint_R \sqrt{EG - F^2} du dv$$