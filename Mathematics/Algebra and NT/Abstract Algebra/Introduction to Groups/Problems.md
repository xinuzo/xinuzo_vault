>[!question] Problem 1A Napkin
>Just a joke, "Baby, my love for you has a proper subgroup isomorphic to itself"

>[!success]- Solution
>Her love is infinite, since only infinite group has proper subgroup isomorphic to itself. 

>[!question] Problem 1B Napkin
>Prove Lagrange’s theorem for orders in the special case that $G$ is a finite abelian group.

>[!success]- Solution
>Take any $x \in G$, let $G=\{1,a_{1},a_{2},..,a_{n-1}\}$ so that $|G|=n$ . Consider $xG=\{x,xa_{1},xa_{2},..,xa_{n} \}$, then $xG=G$, multiply all the elements inside $xG$ and with the fact that G is abelian, we have
>$$x^n \cdot 1 \cdot  a_{1} \dots \cdot a_{n-1}= 1 \cdot  a_{1} \dots \cdot a_{n-1} $$
let $P= 1 \cdot  a_{1} \dots \cdot a_{n-1}$, therefore $x^n=1$


>[!question] Problem 1I Napkin
>If $F_{n}$ is a Fibonacci sequence, prove that $p \mid F_{2p(p^2-1)}$

>[!success]- Solution
Show that the Fibonacci number $F_{2p(p^2-1)}$ is divisible by $p$.
We represent the Fibonacci sequence using the matrix $Q$:
>$$
>Q = \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix}
>$$
>The powers of this matrix generate Fibonacci numbers such that:
>$$
>Q^n = \begin{pmatrix} F_{n+1} & F_n \\ F_n & F_{n-1} \end{pmatrix}
>$$
>To prove that $p \mid F_{2p(p^2-1)}$, it suffices to show that the top-right entry of $Q^{2p(p^2-1)}$ is $0 \pmod p$. We will prove a stronger statement: that $Q^{p^2-1} \equiv I \pmod p$ for $p \neq 5$.
>2. The Case $p=5$
The characteristic polynomial of $Q$ is $\det(Q - \lambda I) = \lambda^2 - \lambda - 1 = 0$.
The discriminant is $\Delta = (-1)^2 - 4(1)(-1) = 5$.
>* If $p=5$, then $5 \mid 2p(p^2-1)$, so the index is a multiple of 5.
>* Property of Fibonacci numbers: $5 \mid n \implies 5 \mid F_n$.
>* Therefore, $F_{2p(p^2-1)} \equiv 0 \pmod 5$.
>The Case $p \neq 5$
Since $p \neq 5$, the discriminant $5 \not\equiv 0 \pmod p$, so $Q$ has distinct eigenvalues $\lambda_1, \lambda_2$.
The roots of $x^2 - x - 1 = 0$ are $\frac{1 \pm \sqrt{5}}{2}$. We analyze the field in which these roots exist.
**Case A: 5 is a Quadratic Residue modulo $p$**
>* $\sqrt{5} \in \mathbb{Z}_p$, so $\lambda_1, \lambda_2 \in \mathbb{Z}_p^\times$.
>* By **Fermat's Little Theorem**, for any $a \in \mathbb{Z}_p^\times$, $a^{p-1} \equiv 1 \pmod p$.
>* Thus, $\lambda_1^{p-1} \equiv 1$ and $\lambda_2^{p-1} \equiv 1$.
>* This implies $Q^{p-1} \equiv I \pmod p$.
>**Case B: 5 is NOT a Quadratic Residue modulo $p$**
>* The roots do not exist in $\mathbb{Z}_p$, but in the quadratic extension field $\mathbb{F}_{p^2}$.
>* The multiplicative group $\mathbb{F}_{p^2}^\times$ has order $p^2 - 1$.
>* By **Lagrange's Theorem**, the order of any element divides the group order.
>* Thus, $\lambda_1^{p^2-1} = 1$ and $\lambda_2^{p^2-1} = 1$ in $\mathbb{F}_{p^2}$.
>* This implies $Q^{p^2-1} \equiv I \pmod p$.
>
In both cases ($p \neq 5$), we found that $Q^k \equiv I \pmod p$ where $k$ divides $p^2-1$.
>$$
>Q^{p^2-1} \equiv \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} \pmod p
>$$
>Looking at the top-right entry (which corresponds to $F_{p^2-1}$):
>$$
>F_{p^2-1} \equiv 0 \pmod p
>$$
>Since $p^2-1$ divides the target index $2p(p^2-1)$, and we know that $a \mid b \implies F_a \mid F_b$, it follows that:
>$$
>F_{p^2-1} \mid F_{2p(p^2-1)}
>$$
>Since $p \mid F_{p^2-1}$, then **$p \mid F_{2p(p^2-1)}$**.

>[!question] Problem 1B Napkin
>Prove Lagrange’s theorem for orders in the special case that $G$ is a finite abelian group.

>[!success]- Solution
>$$ f(x) = \begin{cases} x & \text{if } x \in \mathbb{R}\\ 0 & \text{if } x \not\in \mathbb{R}\end{cases} $$

>[!question] Problem 1B Napkin
>Prove Lagrange’s theorem for orders in the special case that $G$ is a finite abelian group.

>[!success]- Solution
>$$ f(x) = \begin{cases} x & \text{if } x \in \mathbb{R}\\ 0 & \text{if } x \not\in \mathbb{R}\end{cases} $$

