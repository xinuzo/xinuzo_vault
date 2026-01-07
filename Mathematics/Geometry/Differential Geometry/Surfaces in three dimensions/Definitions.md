>[!tips] 4.1 Surface Patch
>A surface patch is a map $\sigma: U \to \mathbb{R}^3$, where $U$ is an open set in $\mathbb{R}^2$. It is **regular** if it is smooth and the partial derivatives $\sigma_u$ and $\sigma_v$ are linearly independent at every point (i.e., $\sigma_u \times \sigma_v \neq \mathbf{0}$).
>[Image of parametric surface patch]

>[!tips] 4.1 Surface
>A subset $S \subset \mathbb{R}^3$ is a surface if, for every point $P \in S$, there is an open set $V$ in $\mathbb{R}^3$ containing $P$ and a regular surface patch $\sigma: U \to S \cap V$ that is a homeomorphism onto its image.
>The collection of such patches covering $S$ is called an **atlas**.

>[!tips] 4.4 Tangent Plane ($T_P S$)
>The tangent plane to $S$ at $P = \sigma(u, v)$ is the vector subspace of $\mathbb{R}^3$ spanned by the vectors $\sigma_u$ and $\sigma_v$.
>[Image of tangent plane to a surface]

>[!tips] 4.5 Normal Vector
>The standard unit normal vector at a point on a surface patch is:
>$$\mathbf{N} = \frac{\sigma_u \times \sigma_v}{||\sigma_u \times \sigma_v||}$$

>[!tips] 4.5 Orientability
>A surface $S$ is **orientable** if there exists a smooth choice of unit normal vector at every point.
>A **non-orientable** surface (e.g., the Möbius Strip) does not allow a continuous global definition of the normal vector.