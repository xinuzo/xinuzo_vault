# Theorems - Chapter III: The Different and Discriminant

## §1. Complementary Modules

>[!tips] 3.1 Proposition 1 (Dual Basis)
>If $L = Aw_1 + \dots + Aw_n$, then $L' = Aw_1' + \dots + Aw_n'$, where $\{w_i'\}$ is the dual basis relative to the trace ($Tr(w_i w_j') = \delta_{ij}$).

>[!tips] 3.1 Proposition 2 Corollary
>If $B = A[\alpha]$ and $f$ is the irreducible polynomial of $\alpha$, then the complementary module is $B' = B / f'(\alpha)$, and the different is $\mathfrak{D}_{B/A} = (f'(\alpha))$.

>[!tips] 3.1 Proposition 5 (Tower Formula)
>Let $K \subset F \subset E$. Then $\mathfrak{D}_{E/K} = \mathfrak{D}_{E/F} \mathfrak{D}_{F/K}$.

## §2. The Different and Ramification

>[!tips] 3.2 Proposition 8
>Let $\mathfrak{P}$ lie above $\mathfrak{p}$ with ramification index $e$. Then $\mathfrak{P}^{e-1}$ divides $\mathfrak{D}_{B/A}$.
>$\mathfrak{P}$ is unramified if and only if $\mathfrak{P}$ does not divide the different.

## §3. The Discriminant

>[!tips] 3.3 Proposition 13
>Let $\mathfrak{b}$ be a fractional ideal of $B$. Then $D_{E/K}(\mathfrak{b}) = (N_K^E(\mathfrak{b}))^2 D_{E/K}(B)$.

>[!tips] 3.3 Proposition 14
>The discriminant and different are related by:
>$$N_{K}^{E} \mathfrak{D}_{B/A} = D_{E/K}(B)$$

>[!tips] 3.3 Stickelberger's Criterion
>Let $E$ be an extension of degree $n$ over $\mathbb{Q}$, and $\alpha_i$ algebraic integers. Then:
>$$D_{E/Q}(\alpha_1, \dots, \alpha_n) \equiv 0 \text{ or } 1 \pmod 4$$

>[!tips] 3.3 Proposition 17 (Linearly Disjoint Fields)
>If $K, E$ have relatively prime discriminants and are linearly disjoint, then:
>$$\mathfrak{o}_{KE} = \mathfrak{o}_K \mathfrak{o}_E \quad \text{and} \quad D_{KE} = D_K^m D_E^n$$