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
>**1. Characterize the Discontinuities**
>Since $f$ is strictly increasing, for any $x \in \mathbb{R}$, the left and right limits exist:
>$$ f(x^-) = \sup_{t < x} f(t) \quad \text{and} \quad f(x^+) = \inf_{t > x} f(t) $$
>And we always have $f(x^-) \le f(x) \le f(x^+)$.
>A discontinuity occurs strictly when there is a "jump," i.e., $f(x^-) < f(x^+)$.
>
>**2. Associate Jumps with Intervals**
>For every point of discontinuity $x$, define the open interval:
>$$ J_x = (f(x^-), f(x^+)) $$
>This interval represents the "vertical gap" skipped by the function at $x$.
>
>**3. Disjointness**
>If $x_1 < x_2$, then $f(x_1^+) \le f(x_2^-)$ because $f$ is increasing.
>Therefore, the intervals $J_{x_1}$ and $J_{x_2}$ are disjoint (they do not overlap).
>
>**4. Counting the Jumps**
>Every non-empty open interval of real numbers must contain a rational number (since $\mathbb{Q}$ is dense in $\mathbb{R}$).
>For each discontinuity $x$, pick one rational number $q_x \in J_x$.
>Since all intervals $J_x$ are disjoint, all chosen $q_x$ must be distinct.
>
>**5. Conclusion**
>This defines a one-to-one mapping from the set of discontinuities to a subset of $\mathbb{Q}$. Since $\mathbb{Q}$ is countable, the set of discontinuities must be countable.
>Since $\mathbb{R}$ is uncountable, $f$ must be continuous at all points in $\mathbb{R}$ except for a countable set. $\square$

>[!question] Problem 2C
>(Continuity of arithmetic continued). Show that subtraction is a continuous map $−: \mathbb{R} × \mathbb{R} → \mathbb{R}$, and division is a continuous map $÷: \mathbb{R} × \mathbb{R}_{>0} → \mathbb{R}$.

>[!success]- Solution
>**1. Subtraction:** Let $(x_n, y_n) \to (x, y)$. 
>$$ >|(x_n - y_n) - (x - y)| = |(x_n - x) - (y_n - y)| \le |x_n - x| + |y_n - y| >$$ Since $|x_n - x| \to 0$ and $|y_n - y| \to 0$, the limit is 0. 
>**2. Division:** Let $(x_n, y_n) \to (x, y)$ with $y \neq 0$. 
>$$ \left| \frac{x_n}{y_n} - \frac{x}{y} \right| = \left| \frac{x_n y - x y_n}{y_n y} \right| = \left| \frac{y(x_n - x) - x(y_n - y)}{y_n y} \right| $$ 
>$$ \le \frac{|y||x_n - x| + |x||y_n - y|}{|y_n||y|} $$
 >Since the numerator $\to 0$ and $|y_n|$ is bounded away from 0, the limit is 0.
 