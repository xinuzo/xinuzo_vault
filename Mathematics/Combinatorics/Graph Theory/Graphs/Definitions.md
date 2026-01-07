>[!tips] 1.1 Graph, Vertex, Edge
>A graph $G$ is an ordered pair $(V(G), E(G))$ consisting of a set $V(G)$ of vertices and a set $E(G)$, disjoint from $V(G)$, of edges, together with an incidence function $\psi_G$ that associates with each edge an unordered pair of vertices.
>The number of vertices $v(G)$ is the order; the number of edges $e(G)$ is the size.

>[!tips] 1.1 Adjacency and Incidence
>Vertices $u$ and $v$ are adjacent (neighbours) if they are ends of an edge. An edge is incident with its ends. The set of neighbours of $v$ is $N_G(v)$.

>[!tips] 1.1 Types of Edges/Graphs
>- **Loop**: An edge with identical ends.
>- **Link**: An edge with distinct ends.
>- **Simple Graph**: A graph with no loops or parallel edges.
>- **Null Graph**: Graph with no vertices.
>- **Trivial Graph**: Graph with one vertex.

>[!tips] 1.1 Special Graphs
>- **Complete Graph ($K_n$)**: Simple graph where any two vertices are adjacent.
>- **Bipartite Graph ($G[X, Y]$)**: Vertex set partitioned into $X, Y$ such that every edge has one end in $X$ and one in $Y$.
>- **Complete Bipartite ($K_{m,n}$)**: Simple bipartite graph where every vertex in $X$ is joined to every vertex in $Y$.
>- **Star**: $K_{1,n}$.
>- **Path ($P_n$)**: Vertices can be arranged in a linear sequence where consecutive vertices are adjacent.
>- **Cycle ($C_n$)**: Vertices arranged in a cyclic sequence where consecutive vertices are adjacent.

>[!tips] 1.1 Connectedness
>A graph is connected if for every partition of its vertex set into two nonempty sets $X, Y$, there is an edge between $X$ and $Y$. Otherwise, it is disconnected.

>[!tips] 1.1 Matrices
>- **Incidence Matrix**: $n \times m$ matrix where entry $m_{ve}$ is the number of times vertex $v$ and edge $e$ are incident.
>- **Adjacency Matrix**: $n \times n$ matrix $A = (a_{uv})$ where $a_{uv}$ is the number of edges joining $u$ and $v$.

>[!tips] 1.1 Degree
>The degree $d_G(v)$ is the number of edges incident with $v$ (loops count as 2).
>- $\delta(G)$: Minimum degree.
>- $\Delta(G)$: Maximum degree.
>- $d(G)$: Average degree.
>- **k-regular**: Every vertex has degree $k$.

>[!tips] 1.2 Isomorphism
>Two graphs $G$ and $H$ are isomorphic ($G \cong H$) if there are bijections $\theta: V(G) \to V(H)$ and $\phi: E(G) \to E(H)$ preserving incidence.

>[!tips] 1.2 Automorphism
>An automorphism is an isomorphism from a graph to itself. The set of automorphisms forms a group $Aut(G)$.
>- **Vertex-transitive**: All vertices are similar (map to each other under automorphisms).
>- **Asymmetric**: Only identity automorphism exists.

>[!tips] 1.3 Derived Graphs
>- **Line Graph ($L(G)$)**: Vertices are edges of $G$; adjacent if they share an end in $G$.
>- **Intersection Graph**: Vertices are sets; adjacent if they intersect.
>- **Incidence Graph**: Bipartite graph representing incidence between two sets (e.g., points and lines).

>[!tips] 1.4 Operations
>- **Union ($G \cup H$)**: Union of vertex and edge sets.
>- **Cartesian Product ($G \Box H$)**: Vertex set $V(G) \times V(H)$; adjacency defined by adjacency in one coordinate and equality in the other.

>[!tips] 1.5 Directed Graphs
>A digraph $D = (V, A)$ consists of vertices and arcs (directed edges).
>- **Indegree ($d^-(v)$)**: Number of arcs entering $v$.
>- **Outdegree ($d^+(v)$)**: Number of arcs leaving $v$.
>- **Tournament**: An orientation of a complete graph.