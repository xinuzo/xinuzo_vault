>[!tips] 5.1 Cut Vertex
>A cut vertex is a vertex $v$ such that $c(G-v) > c(G)$ (increases the number of components).

>[!tips] 5.2 Separation, Separating Vertex
>A separation of a connected graph is a decomposition into two nonempty connected subgraphs having just one vertex in common. This vertex is a separating vertex.

>[!tips] 5.2 Nonseparable, Block
>A graph is nonseparable if it is connected and has no separating vertices. A block is a maximal nonseparable subgraph.

>[!tips] 5.3 Ear Decomposition
>An ear decomposition of a nonseparable graph $G$ is a sequence $G_0 \subset G_1 \subset \dots \subset G_k = G$ where $G_0$ is a cycle, and $G_{i+1} = G_i \cup P_i$ where $P_i$ is an ear (path) intersecting $G_i$ only at its ends.