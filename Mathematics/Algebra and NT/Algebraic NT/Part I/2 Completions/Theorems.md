# Theorems - Chapter II: Completions

## §1. Definitions and Completions

>[!tips] 2.1 Theorem 1 (Approximation Theorem)
>Let $|\cdot|_1, \dots, |\cdot|_s$ be pairwise independent absolute values on $K$. Given $x_1, \dots, x_s \in K$ and $\epsilon > 0$, there exists $x \in K$ such that:
>$$|x - x_i|_i < \epsilon \quad \text{for all } i$$

>[!tips] 2.1 Theorem 2 (Conjugate Embeddings)
>Let $K$ be a number field and $E$ a finite extension. Two embeddings $\sigma, \tau: E \to \overline{K}_v$ give rise to the same absolute value on $E$ if and only if they are conjugate over $K_v$.

## §2. Polynomials in Complete Fields

>[!tips] 2.2 Proposition 2 (Hensel's Lemma)
>Let $f(X) \in \mathfrak{o}[X]$. Let $\alpha_0 \in \mathfrak{o}$ such that $|f(\alpha_0)| < |f'(\alpha_0)^2|$. Then the sequence
>$$\alpha_{i+1} = \alpha_i - \frac{f(\alpha_i)}{f'(\alpha_i)}$$
>converges to a root $\alpha$ of $f(X)$ in $\mathfrak{o}$.

>[!tips] 2.2 Proposition 3 (Krasner's Lemma)
>Let $\alpha, \beta$ be in the algebraic closure of $K$, with $\alpha$ separable over $K(\beta)$. If for all $\sigma \ne id$, $|\beta - \alpha| < |\sigma \alpha - \alpha|$, then $K(\alpha) \subset K(\beta)$.

## §4. Unramified Extensions

>[!tips] 2.4 Proposition 7
>If $E/K$ is unramified, then $E = K(\alpha)$ where $\alpha$ is a root of a polynomial $g(X)$ such that its reduction $\bar{g}(X)$ is irreducible and has no multiple roots.

>[!tips] 2.4 Proposition 9
>There is a bijection between unramified extensions $E$ of $K$ and separable extensions of the residue field $A/\mathfrak{p}$.

## §5. Tamely Ramified Extensions

>[!tips] 2.5 Proposition 11 (Eisenstein Polynomial)
>If $E$ is totally ramified over $K$, a uniformizer $\Pi$ satisfies an Eisenstein equation:
>$$X^e + a_{e-1}X^{e-1} + \dots + a_0 = 0$$
>where $a_i \in \mathfrak{p}$ and $a_0 \notin \mathfrak{p}^2$. Conversely, such an equation generates a totally ramified extension.

>[!tips] 2.5 Proposition 12
>Let $E$ be totally and tamely ramified over $K$ of degree $e$. Then $E = K(\pi^{1/e})$ for some prime element $\pi$ of $K$.