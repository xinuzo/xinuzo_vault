>[!tips] 7.1 Network, Flow
>A network $N = (G, x, y, c)$ is a digraph with source $x$, sink $y$, and capacity $c(a) \ge 0$.
>A flow $f$ assigns values to arcs such that $0 \le f(a) \le c(a)$ and conservation holds at intermediate vertices ($f^+(v) = f^-(v)$).

>[!tips] 7.1 Cut, Capacity
>An $xy$-cut $\partial^+(X)$ is the set of arcs from $X$ to $\bar{X}$ where $x \in X, y \notin X$. The capacity is $\text{cap}(K) = \sum_{a \in K} c(a)$.

>[!tips] 7.2 Incrementing Path
>An $f$-incrementing path is an undirected path from $x$ to $y$ where forward arcs are unsaturated ($f < c$) and reverse arcs are positive ($f > 0$).