### Real Analysis: Derivative Bounds

>[!question] Problem
> Let $f :[a,b] \to \mathbb{R}$ be a continuous function that is differentiable in $(a,b)$.
> 
> Prove that there exists $c \in (a,b)$ such that:
> $$f'(c)(a-c)<2 \quad \text{and} \quad f'(c)(b-c)<2$$

>[!success]- Solution
> **Case 1:** If there exists $c$ such that $f'(c)=0$, the inequalities become $0 < 2$, which is true. We are done.
> 
> **Case 2:** Assume $f'(x) \neq 0$ for all $x$. By Darboux's property, $f'$ maintains a single sign.
> 
> * **Subcase A ($f'(x) > 0$):**
>     The inequality $f'(c)(a-c) < 2$ holds automatically because $a-c < 0$ and $f'(c) > 0$.
>     For the second inequality, assume for contradiction that $f'(x)(b-x) \geq 2$ for all $x$.
>     $$f'(x) \geq \frac{2}{b-x}$$
>     Consider $g(x) = f(x) + 2\ln(b-x)$. Then $g'(x) = f'(x) - \frac{2}{b-x} \geq 0$.
>     This implies $g$ is non-decreasing. However, as $x \to b^-$, $g(x) \to -\infty$, while $g(a)$ is finite. Contradiction.
> 
> * **Subcase B ($f'(x) < 0$):**
>     The inequality $f'(c)(b-c) < 2$ holds automatically because $b-c > 0$ and $f'(c) < 0$.
>     For the first inequality, assume for contradiction that $f'(x)(a-x) \geq 2$.
>     $$f'(x)(x-a) \leq -2 \implies f'(x) \leq \frac{-2}{x-a}$$
>     Consider $h(x) = f(x) + 2\ln(x-a)$. Then $h'(x) \leq 0$.
>     This implies $h$ is non-increasing. However, as $x \to a^+$, $h(x) \to -\infty$, while $h(b)$ is finite. Contradiction.
> 
> **Conclusion:** In all cases, such a $c$ exists.

