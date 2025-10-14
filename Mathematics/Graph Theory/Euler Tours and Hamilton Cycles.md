Of course. Here is a concise summary of those key theorems, formatted as copy-pastable Obsidian Markdown.

The proofs provided are proof sketches or intuitive ideas, as formal proofs can be quite lengthy.

---

## Eulerian Graphs маршрут

These theorems provide exact conditions for determining if a graph is Eulerian by looking at vertex degrees. The graph must be connected.

> Theorem (Eulerian Tour/Circuit)
> 
> A connected graph has an Eulerian tour if and only if every vertex has an even degree.
> 
> **Proof Idea:** To complete a circuit, every time you enter a vertex through an edge, you must leave it through a different edge. This pairing of "in" and "out" edges means that all vertices must have an even degree.
> 
> **Usefulness:** A simple, exact test. Just check the degree of every vertex.

> Theorem (Eulerian Trail/Path)
> 
> A connected graph has an Eulerian trail if and only if it has exactly zero or exactly two vertices of odd degree.
> 
> **Proof Idea:** The trail must start at one vertex and end at another. The starting vertex uses one "outgoing" edge without a corresponding "incoming" one. The ending vertex uses one "incoming" edge without an "outgoing" one. These two endpoints will have an odd degree, while all intermediate vertices (which are entered and then exited) must have an even degree. The "zero odd degree" case is just an Eulerian tour.
> 
> **Usefulness:** A slight generalization of the tour theorem that covers non-circular paths.

---

## Hamiltonian Graphs 🚲

Unlike Eulerian graphs, there is no simple necessary and sufficient condition. These theorems provide **sufficient conditions** (if the condition is met, a cycle is guaranteed, but if not, one might still exist).

> Theorem (Dirac's Theorem)
> 
> If a simple graph G with n≥3 vertices has a minimum degree of δ(G)≥n/2, then G is Hamiltonian.
> 
> **Proof Idea:** The proof is by contradiction. Assume you have the longest possible path that doesn't cover all vertices. The high connectivity guaranteed by the minimum degree condition forces the endpoints of this path to have neighbors that create a cycle, which can then be extended, contradicting that the path was the longest.
> 
> **Usefulness:** A quick and easy-to-check condition based on the least connected vertex.

> Theorem (Ore's Theorem)
> 
> If a simple graph G with n≥3 vertices satisfies deg(u)+deg(v)≥n for every pair of non-adjacent vertices u and v, then G is Hamiltonian.
> 
> **Proof Idea:** Similar to Dirac's Theorem, it relies on high connectivity. The condition ensures that if you have a long path, its endpoints must be connected in such a way that you can form a cycle that includes all vertices on that path.
> 
> **Usefulness:** A stronger (more general) condition than Dirac's. A graph might fail Dirac's test but pass Ore's.

---

## Matchings and Coverings ⚭

These theorems relate sets of independent edges (matchings) to sets of vertices that "touch" all edges (vertex covers).

> Theorem (Hall's Marriage Theorem)
> 
> In a bipartite graph G=(U,V,E), a matching that covers every vertex in U exists if and only if for every subset S⊆U, the size of its neighborhood is at least the size of the subset itself (∣N(S)∣≥∣S∣).
> 
> **Proof Idea:** If there is a subset of vertices in ![](data:,) that collectively connect to fewer vertices in ![](data:,) (a "bottleneck"), it's impossible to match them all. Hall's theorem proves the more difficult reverse direction: if no such bottleneck exists, a complete matching is always possible.
> 
> **Usefulness:** The fundamental theorem for solving assignment and allocation problems in bipartite graphs.

> Theorem (Kőnig's Theorem)
> 
> In any bipartite graph, the number of edges in a maximum matching is equal to the number of vertices in a minimum vertex cover.
> 
> **Proof Idea:** This theorem establishes a fundamental duality. The proof often uses augmenting paths to show that if you have a maximum matching, you can always construct a vertex cover of the same size, and vice-versa.
> 
> **Usefulness:** Connects two different optimization problems on bipartite graphs. If you find a matching and a vertex cover of the same size, you have proven both are optimal.