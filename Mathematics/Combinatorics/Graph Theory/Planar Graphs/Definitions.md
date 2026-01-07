>[!tips] 10.1 Planar Graph / Embedding
>A graph is **planar** if it can be drawn in the plane so that edges meet only at points corresponding to their common ends. Such a drawing is a **planar embedding**. A graph with a specific embedding is a **plane graph**.

>[!tips] 10.1 Face
>A plane graph partitions the rest of the plane into connected regions called **faces**. The unbounded region is the **outer face**.

>[!tips] 10.2 Dual Graph
>Given a plane graph $G$, the **dual graph** $G^*$ is constructed by placing a vertex in each face of $G$ and joining two vertices by an edge for each edge shared by the corresponding faces.

>[!tips] 10.4 Bridge
>Let $H$ be a subgraph of $G$. The **bridges** of $H$ in $G$ are the subgraphs induced by the equivalence classes of edges in $E(G) \setminus E(H)$ (under the relation of being connected by a path internally disjoint from $H$).

>[!tips] 10.5 Minor
>A graph $H$ is a **minor** of $G$ if $H$ can be obtained from a subgraph of $G$ by contracting edges.
> **Kuratowski Minors**: $K_5$ and $K_{3,3}$.

>[!tips] 10.6 Genus
>The **genus** $\gamma(G)$ of a graph is the minimum number of handles required on a sphere to embed the graph (i.e., minimum genus of the orientable surface).