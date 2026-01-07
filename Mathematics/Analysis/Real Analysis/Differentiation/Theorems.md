>[!tips] Theorem 5.2 Differentiability implies Continuity
>If $f$ is differentiable at $x$, then $f$ is continuous at $x$.

>[!tips] Theorem 5.3 Arithmetic of Derivatives
>$(f+g)' = f' + g'$, $(fg)' = f'g + fg'$, $(f/g)' = (g f' - f g')/g^2$.

>[!tips] Theorem 5.5 Chain Rule
>If $h(x) = g(f(x))$, then $h'(x) = g'(f(x))f'(x)$.

>[!tips] Theorem 5.8 Derivative at Local Extrema
>If $f$ is defined on $[a, b]$, has a local maximum at $x \in (a, b)$, and $f'(x)$ exists, then $f'(x) = 0$.

>[!tips] Theorem 5.9 Generalized Mean Value Theorem
>If $f, g$ are continuous on $[a, b]$ and differentiable on $(a, b)$, there exists $x \in (a, b)$ such that
>$$[f(b) - f(a)]g'(x) = [g(b) - g(a)]f'(x)$$

>[!tips] Theorem 5.10 Mean Value Theorem
>If $f$ is continuous on $[a, b]$ and differentiable on $(a, b)$, there exists $x \in (a, b)$ such that
>$$f(b) - f(a) = (b - a)f'(x)$$

**link**:  **[[Cauchy MVT Visual Proof]]**

>[!tips] Theorem 5.11 L'Hospital's Rule
>Suppose $f, g$ are differentiable in $(a, b)$, $g'(x) \ne 0$, $f(x) \to 0$ and $g(x) \to 0$ as $x \to a$ (or $g(x) \to \infty$). If $\lim_{x\to a} f'(x)/g'(x) = A$, then $\lim_{x\to a} f(x)/g(x) = A$.

>[!tips] Theorem 5.15 Taylor's Theorem
>If $f$ has $n-1$ continuous derivatives on $[a, b]$ and $f^{(n)}(t)$ exists on $(a, b)$, then there exists $x \in (a, b)$ such that
>$$f(b) = \sum_{k=0}^{n-1} \frac{f^{(k)}(a)}{k!} (b-a)^k + \frac{f^{(n)}(x)}{n!} (b-a)^n$$