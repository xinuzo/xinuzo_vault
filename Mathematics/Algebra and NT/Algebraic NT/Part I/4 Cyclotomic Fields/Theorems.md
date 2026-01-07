# Theorems - Chapter IV: Cyclotomic Fields

## §1. Roots of Unity

>[!tips] 4.1 Theorem 1 & 2 (Degree)
>Let $\omega$ be a primitive $m$-th root of unity. Then:
>$$[\mathbb{Q}(\omega) : \mathbb{Q}] = \varphi(m)$$
>The only ramified primes in $\mathbb{Q}(\omega)$ are those dividing $m$.

>[!tips] 4.1 Theorem 3 & 4 (Ring of Integers)
>If $K = \mathbb{Q}(\omega)$ with $\omega$ a primitive $m$-th root of unity, then the ring of integers is $\mathfrak{o}_K = \mathbb{Z}[\omega]$.

## §2. Quadratic Fields

>[!tips] 4.2 Theorem 5 (Basis of Quadratic Fields)
>Let $K = \mathbb{Q}(\sqrt{m})$ with $m$ square-free.
>If $m \equiv 2, 3 \pmod 4$, a basis for $\mathfrak{o}_K$ is $\{1, \sqrt{m}\}$.
>If $m \equiv 1 \pmod 4$, a basis for $\mathfrak{o}_K$ is $\{1, \frac{1+\sqrt{m}}{2}\}$.

>[!tips] 4.2 Quadratic Reciprocity Law
>Let $p, q$ be odd primes.
>1. $(\frac{p}{q}) (\frac{q}{p}) = (-1)^{\frac{p-1}{2}\frac{q-1}{2}}$
>2. $(\frac{2}{p}) = (-1)^{\frac{p^2-1}{8}}$

## §3. Gauss Sums

>[!tips] 4.3 Formula 1 & 3
>1. $\tau(\chi, n) = \overline{\chi(n)} \tau(\chi, 1)$ if $(n, q) = 1$.
>2. $|\tau(\chi, n)| = \sqrt{q}$ for primitive $\chi$.

>[!tips] 4.3 Quadratic Sum
>If $p$ is an odd prime and $a$ is prime to $p$:
>$$\sum_{x \text{ mod } p} e^{\frac{2\pi i}{p} ax^2} = \left(\frac{a}{p}\right) G(1, p)$$
>where $G(1, p)^2 = \left(\frac{-1}{p}\right) p$.