>[!tips] 3.1.1  (Definition) Sequence
>A sequence of real numbers (sequence in $\mathbb{R}$ is a function defined on the set $\mathbb{N} = { 1, 2, . . . }$ of natural numbers whose range is contained in the set $\mathbb{R}$. of real numbers.

>[!tips] 3.1.3 (Definition) Convergence
> A sequence $X= (x_{n})$ in $\mathbb{R}$ is said to **converge** to $x \in \mathbb{R}$, or $x$ is said to be a **limit** of $(X_{n})$, if  $\forall \epsilon  > 0$, $\exists K(\epsilon) \in \mathbb{N}$ $\ni n\geq K(\epsilon) \implies |x_{n}-x|<\epsilon.$

>[!tips] (Theorem) 3.1.4 Uniqueness of Limits 
>A sequence in $\mathbb{R}$ can have at most one limit.

>[!success]- Proof.
> Suppose that $x'$ and $x"$ are both limits of $(x_{n})$. For each $\epsilon>0$  there exist $K'$ such that $|x_{n}- x'|< \frac{\epsilon}{2}$ for all $n_{\epsilon}\geq K'$, and there exists $K"$ such that $|x_{n}- x''| < \frac{\epsilon}{2}$ for all $n_{{\epsilon}}\geq K''$. Let $K=max\{K',K''\}$, then for $n_{\epsilon}\geq K$ by  the Triangle Inequality we get $|x'-x''|=|x'-x+x-x''|\leq|x'-x_{n}|+|x''-x_{n}|=\frac{\epsilon}{2}+\frac{\epsilon}{2}=\epsilon.$. 
> Since $\epsilon>0$ is an arbitrary positive number, we conclude that $x'-x''=0$.