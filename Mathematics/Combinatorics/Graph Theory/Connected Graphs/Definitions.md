>[!tips] 3.1 Walk, Trail, Path
>A walk in a graph $G$ is a sequence $W := v_0e_1v_1 \dots e_lv_l$ whose terms are alternately vertices and edges, such that ends of $e_i$ are $v_{i-1}$ and $v_i$.
>- **Length**: The number of edges $l$.
>- **Closed Walk**: $v_0 = v_l$.
>- **Trail**: A walk with distinct edges.
>- **Path**: A walk with distinct vertices (and hence distinct edges).

>[!tips] 3.1 Connectedness, Distance
>Two vertices $x, y$ are connected if there is an $xy$-walk (and thus an $xy$-path). The distance $d_G(x, y)$ is the length of a shortest $xy$-path. If not connected, $d_G(x, y) := \infty$.

>[!tips] 3.1 Diameter
>The diameter of $G$ is the maximum eccentricity over all vertices, i.e., $\max_{u,v} d_G(u, v)$.

>[!tips] 3.5 Cycle Double Cover
>A cycle double cover of a graph is a collection of cycles such that every edge of the graph belongs to exactly two cycles in the collection.