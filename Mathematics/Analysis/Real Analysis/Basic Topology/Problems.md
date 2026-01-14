>[!question] Problem 2D Napkin
>Exhibit a function $f:\mathbb{R} \to \mathbb{R}$ such that $f$ is continuous at $x \in \mathbb{R}$ iff $x=0$.

>[!success]- Solution
>$$ f(x) = \begin{cases} x & \text{if } x \in \mathbb{Q}\\ 0 & \text{if } x \not\in \mathbb{Q}\end{cases} $$

>[!question] Problem 2F Napkin
>Someone on the Internet posted the question “is 1/x a continuous function?”, leading to great controversy on Twitter. How should you respond?

>[!success]- Solution
>$\frac{1}{x}$ is continuous only in $(0,\infty)$ and $(-\infty,0)$ but not on $\mathbb{R}$

>[!question] Problem 2A Napkin
>Let $M=(M,d)$ be a metric space. show that
> $$ d: M \times M \to \mathbb{R}
>$$
is itself a continuous function (where $M \times M$ is equipped with the product metric).

>[!success]- Solution
>Consider $|d(x_{n},y_{n})-d(x,y)|\leq |d(x_{n},x)+d(y_{n},y)|$. We then have $d(x_{n},y_{n})=d(x,y)$ when $x_{n} \to x$ and $y_{n}\to y$

>[!question] Problem 2B Napkin
>Consider $Q$ and $N$ as metric spaces (each with the obvious metric $d(x, y) = |x − y|$). Are these spaces homeomorphic?

>[!success]- Solution
>no, coz homeomorphism $\mathbb{Q} \to \mathbb{N}$ is impossible. 

>[!question] Problem 2E Napkin
>Prove that a function $f : \mathbb{R} → \mathbb{R}$ which is strictly increasing must be continuous at some point

>[!success]- Solution
>$$ f(x) = \begin{cases} x & \text{if } x \in \mathbb{R}\\ 0 & \text{if } x \not\in \mathbb{R}\end{cases} $$

>[!question] Problem 2C
>Continuity of arithmetic continued). Show that subtraction is a continuous map $−: \mathbb{R} × \mathbb{R} → \mathbb{R}$, and division is a continuous map $÷: \mathbb{R} × \mathbb{R}_{>0} → \mathbb{R}$.

>[!success]- Solution
>**1. Subtraction:** Let $(x_n, y_n) \to (x, y)$. 
>$$ >|(x_n - y_n) - (x - y)| = |(x_n - x) - (y_n - y)| \le |x_n - x| + |y_n - y| >$$ Since $|x_n - x| \to 0$ and $|y_n - y| \to 0$, the limit is 0. 
>**2. Division:** Let $(x_n, y_n) \to (x, y)$ with $y \neq 0$. 
>$$ \left| \frac{x_n}{y_n} - \frac{x}{y} \right| = \left| \frac{x_n y - x y_n}{y_n y} \right| = \left| \frac{y(x_n - x) - x(y_n - y)}{y_n y} \right| $$ 
>$$ \le \frac{|y||x_n - x| + |x||y_n - y|}{|y_n||y|} $$
 >Since the numerator $\to 0$ and $|y_n|$ is bounded away from 0, the limit is 0.