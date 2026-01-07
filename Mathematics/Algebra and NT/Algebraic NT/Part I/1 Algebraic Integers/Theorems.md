# Theorems - Chapter I: Algebraic Integers

## §2. Integral Closure

>[!tips] 1.2 Proposition 1
>Let $A$ be a ring, $K$ its quotient field, and $x$ algebraic over $K$. Then there exists $c \neq 0$ in $A$ such that $cx$ is integral over $A$.

>[!tips] 1.2 Proposition 2
>If $B$ is integral over $A$ and finitely generated as an $A$-algebra, then $B$ is a finitely generated $A$-module.

>[!tips] 1.2 Proposition 3 (Transitivity)
>Let $A \subset B \subset C$. If $B$ is integral over $A$ and $C$ is integral over $B$, then $C$ is integral over $A$.

>[!tips] 1.2 Theorem 1
>Let $A$ be a principal ideal ring, and $L$ a finite separable extension of its quotient field of degree $n$. Let $B$ be the integral closure of $A$ in $L$. Then $B$ is a free module of rank $n$ over $A$.

## §3. Prime Ideals

>[!tips] 1.3 Nakayama's Lemma
>Let $A$ be a ring, $\mathfrak{a}$ an ideal contained in all maximal ideals of $A$, and $M$ a finitely generated $A$-module. If $\mathfrak{a}M = M$, then $M = 0$.

>[!tips] 1.3 Proposition 9
>Let $A \subset B$ be integral over $A$. Let $\mathfrak{p}$ be a prime of $A$. Then $\mathfrak{p}B \neq B$ and there exists a prime ideal $\mathfrak{P}$ of $B$ lying above $\mathfrak{p}$.

>[!tips] 1.3 Proposition 10
>Let $A \subset B$ be integral. Let $\mathfrak{P} | \mathfrak{p}$. Then $\mathfrak{P}$ is maximal if and only if $\mathfrak{p}$ is maximal.

## §4. Chinese Remainder Theorem

>[!tips] 1.4 Chinese Remainder Theorem
>Let $\mathfrak{a}_1, \dots, \mathfrak{a}_n$ be ideals such that $\mathfrak{a}_i + \mathfrak{a}_j = A$ for all $i \neq j$. Given $x_1, \dots, x_n \in A$, there exists $x \in A$ such that:
>$$x \equiv x_i \pmod{\mathfrak{a}_i}$$

## §5. Galois Extensions

>[!tips] 1.5 Proposition 11 (Transitive Action)
>Let $A$ be integrally closed in $K$, $L/K$ Galois. Let $\mathfrak{p}$ be a maximal ideal of $A$. Then the Galois group $G$ acts transitively on the prime ideals $\mathfrak{P}$ of $B$ lying above $\mathfrak{p}$.

>[!tips] 1.5 Proposition 14
>Let $B/\mathfrak{P}$ and $A/\mathfrak{p}$ be the residue fields. Then $B/\mathfrak{P}$ is a normal extension of $A/\mathfrak{p}$ and the map $\sigma \mapsto \bar{\sigma}$ induces a homomorphism of $G_{\mathfrak{P}}$ onto the Galois group of $B/\mathfrak{P}$ over $A/\mathfrak{p}$.

## §6. Dedekind Rings

>[!tips] 1.6 Theorem 2 (Unique Factorization)
>Let $\mathfrak{o}$ be a Dedekind ring. Then every ideal of $\mathfrak{o}$ can be uniquely factored into prime ideals, and the non-zero fractional ideals form a group under multiplication.
>$$\mathfrak{a} = \prod \mathfrak{p}^{v_{\mathfrak{p}}}$$

>[!tips] 1.6 Proposition 16 (Localization)
>If $A$ is a Dedekind ring and $S$ a multiplicative subset, then $S^{-1}A$ is a Dedekind ring.

## §7. Discrete Valuation Rings

>[!tips] 1.7 Proposition 18
>Let $M, N$ be $A$-modules. If $S_{\mathfrak{p}}^{-1}M \subset S_{\mathfrak{p}}^{-1}N$ for all primes $\mathfrak{p}$, then $M \subset N$.

>[!tips] 1.7 Proposition 21 (Fundamental Identity)
>Let $L/K$ be a finite separable extension. Let $\mathfrak{p}$ be a prime of $A$. Then:
>$$[L:K] = \sum_{\mathfrak{P}|\mathfrak{p}} e_{\mathfrak{P}} f_{\mathfrak{P}}$$
>If $L/K$ is Galois, then $e_{\mathfrak{P}}$ and $f_{\mathfrak{P}}$ are constant for all $\mathfrak{P}$, and $[L:K] = efr$.

## §8. Explicit Factorization

>[!tips] 1.8 Proposition 25 (Dedekind-Kummer)
>Let $B = A[\alpha]$, $f(X)$ be the irreducible polynomial of $\alpha$. Let $\bar{f}(X) = \prod \bar{P}_i(X)^{e_i}$ mod $\mathfrak{p}$. Then:
>$$\mathfrak{p}B = \prod \mathfrak{P}_i^{e_i}$$
>where $\mathfrak{P}_i = \mathfrak{p}B + P_i(\alpha)B$.