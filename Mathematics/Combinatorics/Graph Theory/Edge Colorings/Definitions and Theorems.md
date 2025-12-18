

### Topic 1: Edge Coloring (Pewarnaan Sisi)
[cite_start]**Source Reference:** [cite: 3]

#### 1.1 Definitions and Basic Lemmas
> [!info] Definition 1.1: Clique (Clique)
> [cite_start]A clique in a graph $G$ is a subset of vertices $S \subseteq V(G)$ such that every pair of distinct vertices in $S$ is adjacent[cite: 6].
> [cite_start]* The subgraph induced by $S$ $(G[S])$ is a complete graph $(K_{|S|})$[cite: 7].
> [cite_start]* **Clique Number $(\omega(G))$:** The size (number of vertices) of the maximum clique in $G$[cite: 8].

> [!info] Definition 1.2: k-Edge Coloring
> Let $G$ be a loopless graph. [cite_start]$\mathcal{C}$ is a $k$-edge coloring of $G$ if there exists a mapping $\mathcal{C}: E(G) \rightarrow \{1, ..., k\}$[cite: 10].
> [cite_start]* **Proper Coloring:** A coloring is proper if every two adjacent (incident) edges have different colors[cite: 11].
> [cite_start]* **Edge Chromatic Number $(\chi'(G))$:** The smallest integer $k$ such that $G$ has a proper $k$-edge coloring[cite: 12].

> [!note] Lemma 1.3: Color Representation
> [cite_start]Let $G$ be a connected graph that is not an odd cycle[cite: 14]. [cite_start]Then there exists a 2-edge coloring (not necessarily proper) such that both colors are represented at every vertex with degree at least 2[cite: 15].

> [!info] Definition 1.4: Optimal Coloring
> Let $\mathcal{C}$ be a $k$-edge coloring. [cite_start]$\mathcal{C}$ is optimal if for any other $k$-edge coloring $\mathcal{C}'$, the following holds[cite: 17]:
> $$\sum_{v \in V} c'(v) \le \sum_{v \in V} c(v)$$
> [cite_start]where $c(v)$ is the number of distinct colors appearing at vertex $v$[cite: 18, 19].

> [!note] Lemma 1.5: Optimality Criterion
> [cite_start]Let $\mathcal{C} = (E_1, ..., E_k)$ be an optimal $k$-edge coloring of $G$[cite: 21]. [cite_start]If there exists a vertex $u$ and colors $i, j$ such that color $i$ does not appear at $u$ and color $j$ appears at least twice at $u$, then the component of $G[E_i \cup E_j]$ containing $u$ is an odd cycle[cite: 21].

#### [cite_start]1.2 Main Edge Coloring Theorems [cite: 22]
> [!info] Theorem 1.6: Vizing's Theorem (Simple Graphs)
> If $G$ is a simple graph, then:
> [cite_start]$$\Delta(G) \le \chi'(G) \le \Delta(G) + 1$$ [cite: 27, 28]

> [!info] Theorem 1.7: Vizing's Theorem (General)
> [cite_start]For any loopless graph $G$ (which may have multiple edges)[cite: 30]:
> $$\Delta(G) \le \chi'(G) \le \Delta(G) + \mu(G)$$
> [cite_start]where $\mu(G)$ is the maximum multiplicity (max number of edges connecting the same pair of vertices)[cite: 31, 32].

> [!info] Theorem 1.8: Bipartite Graphs
> [cite_start]If $G$ is a bipartite graph, then $\chi'(G) = \Delta(G)$[cite: 34].

> [!info] Theorem 1.9: Odd Regular Graphs
> [cite_start]If $G$ is a $k$-regular graph with an odd number of vertices $|V(G)|$, then $\chi'(G) = k + 1$[cite: 36].

> [!note] Proposition 1.10: Complete Graphs
> [cite_start]1. $\chi'(K_{m,n}) = \Delta(K_{m,n}) = \max(m,n)$[cite: 38].
> [cite_start]2. $\chi'(K_{2n}) = 2n - 1$ (Complete graph with even vertices = Class 1)[cite: 39].
> [cite_start]3. $\chi'(K_{2n-1}) = 2n - 1$ (Complete graph with odd vertices = Class 2)[cite: 40].

---

### Topic 2: Vertex Coloring (Pewarnaan Titik)
[cite_start]**Source Reference:** [cite: 50]

#### 2.1 Definitions and Critical Graphs
> [!info] Definition 2.1: Chromatic Number
> [cite_start]The **Chromatic Number $(\chi(G))$** is the minimum number of colors required to color the vertices of $G$ such that no two adjacent vertices have the same color[cite: 53].

> [!info] Definition 2.2: Critical Graph
> [cite_start]A graph $G$ is called **$k$-critical** if $\chi(G) = k$ and for every proper subgraph $H \subset G$, it holds that $\chi(H) < \chi(G)$[cite: 55].

> [!note] Proposition 2.3: Properties of Critical Graphs
> [cite_start]* **1-critical:** $K_1$[cite: 57].
> [cite_start]* **2-critical:** $K_2$[cite: 58].
> [cite_start]* **3-critical:** Odd cycles[cite: 59].

#### [cite_start]2.2 Main Vertex Coloring Theorems [cite: 60]
> [!info] Theorem 2.4: Minimum Degree
> [cite_start]If $G$ is $k$-critical, then the minimum degree $\delta(G) \ge k - 1$[cite: 62].

> [!note] Corollary 2.5
> [cite_start]1. Every $k$-chromatic graph has at least $k$ vertices with degree $\ge k-1$[cite: 64].
> [cite_start]2. For any graph $G$, $\chi(G) \le \Delta(G) + 1$[cite: 65].

> [!info] Theorem 2.6: Brooks' Theorem
> [cite_start]If $G$ is a connected simple graph that is neither an odd cycle nor a complete graph $(K_n)$ then[cite: 67]:
> [cite_start]$$\chi(G) \le \Delta(G)$$[cite: 68].

> [!info] Theorem 2.7: Vertex Cut
> [cite_start]In a critical graph, no vertex cut is a clique[cite: 70]. [cite_start]**Consequence:** Every critical graph is a block (has no cut vertex)[cite: 70].

> [!info] Theorem 2.8: Dirac (2-Vertex Cut)
> [cite_start]Let $G$ be a $k$-critical graph with a 2-vertex cut $\{u, v\}$[cite: 72]. Then:
> [cite_start]1. $G = G_1 \cup G_2$, where $G_1$ is type 1 and $G_2$ is type 2[cite: 73].
> [cite_start]2. $G_1 + uv$ is $k$-critical[cite: 73].
> [cite_start]3. $G_2$ (graph resulting from identifying $u$ and $v$) is $k$-critical[cite: 77, 78].
>
> [cite_start]**Corollary 2.9:** If $G$ is $k$-critical with a 2-vertex cut $\{u, v\}$, then $d(u) + d(v) \ge 3k - 5$[cite: 80, 81].

> [!note] Theorem 2.10: Hajos Conjecture
> [cite_start]If $G$ is $k$-chromatic, then $G$ contains a subdivision of $K_k$[cite: 83]. (True for $k \le 4$) [cite_start][cite: 83].

---

### Topic 3: Plane and Planar Graphs
[cite_start]**Source Reference:** [cite: 87]

#### 3.1 Definitions
> [!info] Definition 3.1: Planar & Plane Graphs
> [cite_start]* **Planar Graph:** A graph $G$ is planar if it can be drawn on a plane such that its edges intersect only at their endpoints[cite: 90].
> [cite_start]* **Planar Embedding:** A drawing of $G$ where edges intersect only at endpoints[cite: 91]. [cite_start]This is often called a **Plane Graph**[cite: 92].

> [!info] Definition 3.2: Jordan Curve
> [cite_start]A continuous non-self-intersecting curve whose start and end points coincide[cite: 94].
> [cite_start]* The union of edges in a cycle of a plane graph forms a Jordan Curve[cite: 95].
> [cite_start]* It partitions the plane into two disjoint open sets: interior ($int.J$) and exterior ($ext.J$)[cite: 96].

#### 3.2 Non-Planarity Theorems
> [!info] Basic Non-Planar Graphs
> [cite_start]* **Theorem 3.3:** $K_5$ is non-planar[cite: 97, 98].
> [cite_start]* **Theorem 3.4:** $K_{3,3}$ is non-planar[cite: 99, 100].

> [!note] Theorem 3.5: Spherical Embedding
> [cite_start]A graph $G$ can be embedded on a plane if and only if $G$ can be embedded on the surface of a sphere[cite: 102].

---

### Topic 4: Dual Graphs
[cite_start]**Source Reference:** [cite: 106]

#### 4.1 Faces and Duals
> [!info] Definition 4.1: Face
> A plane graph $G$ partitions the plane into connected regions. [cite_start]The closures of these regions are called **faces**[cite: 109].
> [cite_start]* Every plane graph has exactly one unbounded face called the **exterior face**[cite: 112].

> [!info] Definition 4.4: Dual Graph
> [cite_start]Given a plane graph $G$, the **Dual Graph $G^*$** is defined as[cite: 119]:
> [cite_start]* Every face $f$ in $G$ corresponds to a vertex $f^*$ in $G^*$[cite: 120].
> [cite_start]* Every edge $e$ in $G$ corresponds to an edge $e^*$ in $G^*$[cite: 121].
> [cite_start]* Two vertices $f^*$ and $g^*$ are connected by $e^*$ in $G^*$ iff faces $f$ and $g$ are separated by edge $e$ in $G$[cite: 122].

> [!note] Properties of Duals
> [cite_start]1. If $G$ is planar, $G^*$ is also planar[cite: 124].
> [cite_start]2. $v(G^*) = \phi(G)$ (Number of vertices in Dual = Number of faces in Primal)[cite: 127].
> [cite_start]3. $\epsilon(G^*) = \epsilon(G)$ (Number of edges is equal)[cite: 128].
> [cite_start]4. $d_{G^*}(f^*) = d_G(f)$ for all $f \in F(G)$[cite: 129].
> [cite_start]5. $G \cong G^{**}$ iff $G$ is connected[cite: 130].

> [!info] Theorem 4.7: Handshaking Lemma for Faces
> If $G$ is a plane graph, then:
> [cite_start]$$\sum_{f \in F} d(f) = 2\epsilon$$ [cite: 135, 138]

---

### Topic 5: Euler's Formula
[cite_start]**Source Reference:** [cite: 136]

#### 5.1 Formula and Consequences
> [!info] Theorem 5.1: Euler's Formula
> If $G$ is a connected planar graph, then:
> [cite_start]$$v - \epsilon + \phi = 2$$ [cite: 140, 141]

> [!note] Corollaries
> [cite_start]* **Corollary 5.2:** All planar embeddings of a given connected planar graph have the same number of faces[cite: 143].
> * **Corollary 5.3 (Edge Upper Bound):** If $G$ is a simple planar graph with $v \ge 3$, then:
>     [cite_start]$$\epsilon \le 3v - 6$$ [cite: 145, 146]
> [cite_start]* **Corollary 5.4:** If $G$ is a simple planar graph, then $\delta(G) \le 5$[cite: 148].

> [!info] Proposition 5.6: Girth Inequality
> [cite_start]If $G$ is a connected planar graph with girth $k \ge 3$, then[cite: 153]:
> [cite_start]$$\epsilon \le \frac{k}{k-2}(v-2)$$ [cite: 154]
> [cite_start]* **Example:** For bipartite graphs ($k=4$), $\epsilon \le 2v - 4$[cite: 155].

---

### Topic 6: Kuratowski's Theorem
[cite_start]**Source Reference:** [cite: 159]

#### 6.1 Subdivisions and Blocks
> [!info] Definition 6.1: Block
> [cite_start]A block of graph $G$ is a maximal connected subgraph that has no cut-vertex[cite: 163].
> [cite_start]* $G$ is planar iff every block of $G$ is planar[cite: 166].

> [!info] Theorem 6.2: Kuratowski's Theorem
> [cite_start]A graph is planar if and only if it does not contain a subdivision of $K_5$ or $K_{3,3}$[cite: 168].

> [!note] Lemma 6.3: Subdivisions and Subgraphs
> [cite_start]* If $G$ is non-planar, then every subdivision of $G$ is non-planar[cite: 170].
> [cite_start]* If $G$ is planar, then every subgraph of $G$ is planar[cite: 171].

#### [cite_start]6.2 Bridge Theory (Brief) [cite: 172]
> [!info] Bridge Concepts
> [cite_start]* **Bridge of Cycle C:** Subgraph formed by equivalence classes of edges relative to cycle $C$[cite: 177].
> [cite_start]* **Skew:** Two bridges $B$ and $B'$ are skew if their vertices of attachment interlace on $C$[cite: 179].
> [cite_start]* **Overlap:** Bridges overlap if they are skew or equivalent 3-bridges[cite: 180].

---

### Topic 7: Planar Coloring
[cite_start]**Source Reference:** [cite: 192]

#### 7.1 Coloring Theorems
> [!info] Theorem 7.1: 5-Color Theorem (Heawood, 1890)
> [cite_start]Every planar graph is 5-vertex-colorable[cite: 194].

> [!info] Theorem 7.2: 4-Color Theorem (Appel & Haken, 1976)
> [cite_start]Every planar graph is 4-vertex-colorable[cite: 196].

> [!note] Theorem 7.3: Coloring Equivalence (Tait's Conjecture)
> [cite_start]The following three statements are equivalent[cite: 197, 198]:
> [cite_start]1. Every planar graph is 4-vertex-colorable[cite: 199].
> [cite_start]2. Every plane graph is 4-face-colorable[cite: 200].
> [cite_start]3. Every simple planar graph that is 2-edge-connected and 3-regular is 3-edge-colorable[cite: 201].