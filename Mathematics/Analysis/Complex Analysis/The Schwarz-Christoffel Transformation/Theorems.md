>[!tips] 11.127 Schwarz-Christoffel Formula
>The derivative of the mapping function $w = f(z)$ is given by:
>$$f'(z) = A (z - x_1)^{-k_1} (z - x_2)^{-k_2} \dots (z - x_{n-1})^{-k_{n-1}}$$
>where $x_k$ are points on the real axis mapping to vertices $w_k$ with exterior angles $k_k \pi$. $A$ is a complex constant determining rotation and scale.
>The mapping itself is:
>$$w = A \int_{z_0}^z (s - x_1)^{-k_1} \dots (s - x_{n-1})^{-k_{n-1}} ds + B$$

>[!tips] 11.129 Triangles and Rectangles
>Special cases of the transformation allow mapping the upper half plane onto a triangle or a rectangle.
>For a rectangle, the points $x_k$ are symmetric ($\pm 1, \pm 1/k$), leading to elliptic integrals.

>[!tips] 11.130 Degenerate Polygons
>The formula extends to infinite strips or semi-infinite strips by considering vertices at infinity.
>- **Strip**: Corresponds to $k_k = 1$ (exterior angle $\pi$).
>- **Fluid Flow in Channels**: Used to model flow past obstacles or abrupt changes in channel width.