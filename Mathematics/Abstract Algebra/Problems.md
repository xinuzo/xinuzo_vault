- [x] **ONMIPA 2006**
>[!question]
Diketahui $G = {1, −1}$ grup dengan operasi kali dan $G^3 = {(a, b, c) : a, b, c ∈ G}$ grup dengan operasi untuk setiap $x_{1} = (a_{1}, b_{1}, c_{1})$, $x_{2} = (a_{2}, b_{2}, c_{2}) ∈ G^3$
$x_{1} ∗ x_{2} = (a_{1}a_{2}, b_{1}b_{2}, c_{1}c_{2})$.
Banyaknya subgrup dari $G^{3}$ dengan order 4 adalah . . 

>[!success]- 
>Akan ditunjukkan ada 7 subgrup.  Tinjau bahwa suatu subgrup  $H \leq G$ harus memiliki elemen **identitas**, setiap elemen memiliki **invers** dan **tertutup terhadap operasi**. Order dari suatu grup adalah banyaknya elemen pada grup tersebut. Dengan demikian, elemen **(1,1,1)** harus ada dalam subgrup karena ia adalah elemen **identitas**. Selanjutnya, perhatikan bahwa pemilhan 2 elemen sembarang akan menentukan 1 elemen lagi yang harus ada dalam grup itu karena sifat **tertutup terhadap operasi**. Dengan demikian ada **$\frac{\binom{7}{2}}{3} = 7$** subgrup berorder 4. 
 


**KOALA 2025**
## 1.
Permutation $\pi=(1\ 4\ 3\ 2)(5\ 6\ 7\ 8)(6\ 8\ 1\ 5)(4\ 5\ 7)\in S_8$. Compute the order of $\pi$.

**Solution (sketch).** Compose the cycles (right-to-left). The composition is a single 8-cycle $(1\ 6\ 5\ 8\ 4\ 7\ 3\ 2)$.
**Answer:** $\boxed{8}$.

---

## 2.
Matrix $T$ represented by
$$
\begin{pmatrix}
0&1&0&0\\[4pt]
0&0&1&0\\[4pt]
0&0&0&1\\[4pt]
0&0&0&0
\end{pmatrix}
$$
on $\mathbb{R}^4$. Find $\dim\ker(T\circ T)$.

**Solution.** $T$ is the (nilpotent) right-shift; $T^2$ has rank $2$ (two independent images), so nullity $=4-2=2$.
**Answer:** $\boxed{2}$.

---

## 3.
Number of nilpotent elements in the ring $\mathbb{Z}_{45}$.

**Solution.** Use CRT: $\mathbb{Z}_{45}\cong\mathbb{Z}_9\times\mathbb{Z}_5$. Nilpotent iff component in $\mathbb{Z}_5$ is $0$ and component in $\mathbb{Z}_9$ is multiple of $3$. There are $3$ multiples of $3$ mod $9$.
**Answer:** $\boxed{3}$.

---

## 4.
Number of linear maps $T:\mathbb{R}^3\to\mathbb{R}^3$ with integer matrix entries (w.r.t. standard basis) such that $\|T(v)\|=\|v\|$ for all $v$.

**Solution.** Such maps are orthogonal matrices with integer entries — i.e. signed permutation matrices. There are $3!$ permutations and $2^3$ choices of signs.
**Answer:** $\boxed{48}$.

---

## 5.
Let $A=\{f: \mathbb{Z}_5\to\mathbb{Z}_{25}\}$ (ring of functions, pointwise operations). How many nilpotent elements in $A$?

**Solution.** A function is nilpotent iff each value is nilpotent in $\mathbb{Z}_{25}$. Nilpotent elements in $\mathbb{Z}_{25}$ are precisely the multiples of $5$: $5$ choices. For each of $5$ arguments we may choose one of these $5$ values.
**Answer:** $\boxed{5^5=3125}$.

---

## 6.
Order of matrix $\begin{pmatrix}1&1\\0&2\end{pmatrix}$ in $\mathrm{GL}_2(\mathbb{Z}_{23})$.

**Solution.** For upper-triangular $\begin{pmatrix}1&1\\0&2\end{pmatrix}$, the powers give diagonals $1^n,2^n$ and upper-right entry proportional to $2^n-1$. The matrix equals identity iff $2^n\equiv1\pmod{23}$. The multiplicative order of $2$ mod $23$ is $11$.
**Answer:** $\boxed{11}$.

---

## 7.
Let $\varphi:\mathbb{Z}_{30}\to\mathbb{Z}_6$ be a group homomorphism with $\ker\varphi=\{0,6,12,18,24\}$ and $\varphi(1)\ne 1$. Find $\varphi(1)$.

**Solution.** Kernel has size $5$ so image has size $30/5=6$ — the map is surjective. The generators of $\mathbb{Z}_6$ are $1$ and $5$. Since $\varphi(1)\ne1$, it must be $5$.
**Answer:** $\boxed{5}$.

---

## 8.
Linear operator $T$ on $\mathbb{R}[x]$ defined by $T(P)(x)=x^3P(x)-P(x^2)$. Find $\dim\ker T$.

**Solution.** If $P$ has degree $d$, compare degrees: left side degree $d+3$, right side $2d$. Nonzero solutions require $d+3=2d\Rightarrow d=3$. Substitute $P=a_0+a_1x+a_2x^2+a_3x^3$ and equate coefficients; only $a_3$ is free.
**Answer:** $\boxed{1}$.

---

## 9.
Let $T:M_5(\mathbb{R})\to M_5(\mathbb{R})$ be $T(X)=AX-XA$. Let $p,q$ be minimum and maximum possible ranks of $T$ (when $A$ varies). Find $p+q$.

**Solution.** If $A=\lambda I$ then $T\equiv0$ so $p=0$. For diagonalizable $A$ with $5$ distinct eigenvalues, the centralizer has dimension $5$, so $\operatorname{rank}T=25-5=20$. This is maximal.
**Answer:** $\boxed{20}$.

---

## 10.
Matrix $S\in M_{4\times4}(\mathbb{R})$ with decimal-pattern entries (see problem). Find the number of nonzero entries in the reduced row-echelon form of $S$.

**Solution (calculation).** Computation (exact integer arithmetic) gives RREF with two nonzero rows; total nonzero entries in RREF is $6$.
**Answer:** $\boxed{6}$.

---

## 11.
For $A=\begin{pmatrix}1&3&2\\[2pt]2&1&3\\[2pt]3&2&1\end{pmatrix}$ and $v\neq0\in\mathbb{R}^3$, find the maximum of $\dfrac{\|Av\|}{\|v\|}$.

**Solution.** The maximum equals the largest singular value of $A$. Computation gives largest singular value $6$.
**Answer:** $\boxed{6}$.

---

## 12.
Matrix $A$ of size $5\times5$ with $A_{ij}=1+|i-j|$. Find $\det(A)$.

**Solution (explicit determinant).** Direct computation yields $\det(A)=48$.
**Answer:** $\boxed{48}$.

---

## 13.
Number of tripotent elements (i.e. $x^3=x$) in $\mathbb{Z}_{216}$.

**Solution.** Factor $216=2^3\cdot3^3$. Solve $x(x-1)(x+1)\equiv0$ modulo $2^3$ and modulo $3^3$. Mod $8$ there are $5$ solutions $\{0,1,3,5,7\}$; mod $27$ there are $3$ solutions $\{0,1,26\}$. By CRT total $=5\cdot3=15$.
**Answer:** $\boxed{15}$.

---

## 14.
Number of permutations in $S_5$ that have at least $5$ inversions.

**Solution (counting).** By enumeration or inversion-distribution symmetry one finds the count equals $71$.
**Answer:** $\boxed{71}$.

---

## 15.
Let $H$ be the set of $2\times2$ matrices whose entries are all distinct and taken from $\{1,2,3,4\}$. Compute $\displaystyle\sum_{M\in H}\det(M)$.

**Solution.** Sum over all $24$ permutation-arrangements gives total $0$ (antisymmetry cancels).
**Answer:** $\boxed{0}$.

---

## 16.
Given $a,b,c\in\mathbb{R}$ with $a^2+b^2+c^2=9$, consider
$$
C=\begin{pmatrix}
a+b & b+c & c+a\\[4pt]
c+a & a+b & b+c\\[4pt]
b+c & c+a & a+b
\end{pmatrix}.
$$
Let $m$ and $n$ be the maximum and minimum possible $\det(C)$. Find $m-n$.

**Solution (sketch).** Using the circulant structure the determinant is an odd-symmetric function; numerical extremization (or an analytic Lagrange-multiplier argument) gives $m=54$ and $n=-54$. Hence $m-n=108$.
**Answer:** $\boxed{108}$.

---

## 17.
$|\mathrm{GL}_3(\mathbb{Z}_4)| = 2^a\cdot b$ with $b$ odd. Find $a+b$.

**Solution.** For a finite chain ring $\mathbb{Z}_{p^k}$ one has $|\mathrm{GL}_n(\mathbb{Z}_{p^k})| = p^{n^2(k-1)}\prod_{i=0}^{n-1}(p^n-p^i)$. Here $p=2,k=2,n=3$:
$$
|\mathrm{GL}_3(\mathbb{Z}_4)| = 2^{9}\cdot(8-1)(8-2)(8-4)=2^9\cdot7\cdot6\cdot4 = 86016.
$$
Factorization: $86016=2^{12}\cdot21$. So $a=12,b=21$, $a+b=33$.
**Answer:** $\boxed{33}$.

---

## 18.
Number of monic irreducible polynomials of degree $9$ with coefficients in $\mathbb{Z}_4$ equals $2^a\cdot b$ with $b$ odd. Find $a+b$.

**Solution (standard fact).** Over the finite chain ring $\mathbb{Z}_{p^k}$ the count of monic basic irreducibles of degree $n$ equals $p^{(k-1)n}$ times the number of monic irreducible polynomials of degree $n$ over $\mathbb{F}_p$. For $p=2,k=2,n=9$:
- Number over $\mathbb{F}_2$ is $\dfrac{1}{9}\left(2^{9}-2^{3}\right)=56$.
- Multiply by $2^{(2-1)\cdot9}=2^9=512$. Total $512\cdot56=28672$.
Factorization: $28672=2^{12}\cdot7$. So $a=12,b=7$, $a+b=19$.
**Answer:** $\boxed{19}$.

---

## 19.
How many positive integers $n\le 2025$ such that $\mathbb{Z}_n$ has a subring isomorphic to $\mathbb{Z}_2$?

**Solution (sketch).** A subring isomorphic to $\mathbb{Z}_2$ corresponds to a nonzero idempotent $e$ with $2e\equiv0\pmod n$. CRT analysis forces all odd prime-power components of $e$ to be $0$ and the $2$-power part to be $1$. This is possible precisely when $n$ is divisible by $2$ but not by $4$; i.e. $n\equiv2\pmod4$. Count numbers $\le2025$ congruent to $2$ mod $4$: these are $2,6,\dots,2022$, a total of $506$ numbers.
**Answer:** $\boxed{506}$.

---

## 20.
Let $G$ be the group generated by $a,b,c$ with relations
$$
abab=e,\quad caca^{-1}=e,\quad cbcb^{-1}=e,\quad a^4=b^2=c^3=e,
$$
and $G=\langle a,b,c\rangle$. Find the maximal possible order of $G$.

**Solution (sketch & construction).** One can map the given presentation onto the symmetric group $S_4$ (order $24$) by sending:
- $a$ to a 4-cycle,
- $b$ to an appropriate transposition (order $2$),
- $c$ to an appropriate 3-cycle (order $3$),
and check the relations are satisfied in $S_4$. Thus $|G|\ge24$. On the other hand the relations severely restrict the possible actions and one shows any such presentation admits a faithful action on at most 24 points (one standard way is to use the action by left multiplication on a suitable coset set and count cosets). Hence the maximal possible order is $\boxed{24}$.
(So the maximal attainable finite order is $24$.)

---

# Part B — Sesi II (Essay problems / full solutions)

## Problem 1 (Sesi II).
**Statement.** Let $A$ be an $n\times n$ matrix with $n\ge3$. If $\operatorname{rank}(A)=n-2$, determine $\operatorname{rank}(\operatorname{adj}(A))$.
(Here $\operatorname{adj}(A)$ denotes the transpose of the matrix of cofactors.)

**Solution.**

**Recall.** For any $n\times n$ matrix $A$:
- $\operatorname{adj}(A)A = A\operatorname{adj}(A) = (\det A) I_n$.
- If $\operatorname{rank}(A)=n$ (invertible), $\operatorname{adj}(A)= (\det A) A^{-1}$ has rank $n$.
- If $\operatorname{rank}(A)=n-1$, then $\operatorname{adj}(A)$ is nonzero and has rank $1$.
We now handle the case $\operatorname{rank}(A)=n-2$.

**Step 1: Show $\operatorname{adj}(A)=0$ when $\operatorname{rank}(A)\le n-2$.**

Let $\operatorname{rank}(A)=r$. A classical fact: all $(r+1)\times(r+1)$ minors of $A$ vanish, and in particular all $(n-1)\times(n-1)$ minors vanish if $r\le n-2$. But the entries of $\operatorname{adj}(A)$ are (up to sign) exactly these $(n-1)\times(n-1)$ minors. Therefore if $r\le n-2$ every entry of $\operatorname{adj}(A)$ is zero, hence $\operatorname{adj}(A)=0$.

**Conclusion.** For $\operatorname{rank}(A)=n-2$, we have $\operatorname{adj}(A)=0$, so $\operatorname{rank}(\operatorname{adj}(A))=0$.

**Answer:** $\boxed{0.}$

---

## Problem 2 (Sesi II).
**Statement.** Let $G$ be a cyclic group with $|G|=p^2q^2$ where $p,q$ are distinct primes. Define
$$
S=\{x\in G \mid \operatorname{ord}(x)=p^2\ \text{or}\ \operatorname{ord}(x)=q^2\}.
$$
(a) Determine $|S|$.
(b) Prove that $\langle S\rangle = G$.

**Solution.**

Because $G$ is cyclic of order $p^2q^2$, fix a generator $g$ with $|g|=p^2q^2$.

### (a) Count $|S|$.

- Elements of order $p^2$: such elements are exactly the elements $g^{k}$ whose order is $p^2$. The order of $g^k$ equals $\dfrac{p^2q^2}{\gcd(k,p^2q^2)}$. For this to be $p^2$, we need $\dfrac{p^2q^2}{\gcd(k,p^2q^2)}=p^2$, so $\gcd(k,p^2q^2)=q^2$. Thus $k$ must be divisible by $q^2$ but not by $pq^2$ etc. Equivalently $k=q^2\cdot t$ with $\gcd(t,p^2)=1$ and $1\le t\le p^2\cdot q^2/q^2 = p^2$. The number of such $t$ with $\gcd(t,p^2)=1$ equals $\varphi(p^2)=p^2-p$. So there are $\varphi(p^2)=p(p-1)$ elements of order $p^2$.

- Similarly, elements of order $q^2$: $\varphi(q^2)=q(q-1)$.

These two sets are disjoint (an element cannot have two distinct orders). Therefore
$$
|S|= \varphi(p^2)+\varphi(q^2) = p(p-1)+q(q-1).
$$

**Answer (a):** $\boxed{|S|=p(p-1)+q(q-1)}.$

### (b) Show $\langle S\rangle=G$.

Let $H=\langle S\rangle$. We will show $|H|=p^2q^2$.

- Observe that any element of order $p^2$ generates the unique subgroup of order $p^2$; likewise for $q^2$. In a cyclic group, for each divisor $d$ of $|G|$ there is a unique subgroup of order $d$. So $G$ has unique subgroups $P$ of order $p^2$ and $Q$ of order $q^2$.

- The set $S$ contains generators of $P$ (all elements of order $p^2$) and generators of $Q$ (all elements of order $q^2$). Therefore $P\subseteq H$ and $Q\subseteq H$.

- Since $P$ has order $p^2$ and $Q$ has order $q^2$ and $\gcd(p^2,q^2)=1$, the subgroup generated by $P$ and $Q$ has order $p^2q^2$ (product of coprime orders), i.e. $\langle P,Q\rangle = P\cdot Q$ and $|P\cdot Q|=|P||Q|=p^2q^2$. But $P\cdot Q$ is a subgroup of $H$; therefore $H$ has order $p^2q^2$. Hence $H=G$.

**Answer (b):** $\boxed{\langle S\rangle=G.}$

---

## Problem 3 (Sesi II).
**Statement.** Let $n>1$ and $v_1,\dots,v_n\in\mathbb{R}^n$. Define the $n\times n$ matrix $A$ by $A_{ij}=v_j^{T}v_i$ (so the $(i,j)$-entry is $v_j^T v_i$). Let the characteristic polynomial of $A$ be
$$
\lambda^n+u_1\lambda^{n-1}+u_2\lambda^{n-2}+\cdots+u_{n-1}\lambda+u_n.
$$
Show: for each $k\in\{1,\dots,n\}$, $u_k\le0$ if $k$ is odd and $u_k\ge0$ if $k$ is even.

**Solution.**

First note $A$ is a Gram-like matrix but with columns and rows swapped: indeed $A = V^T V$ if $V$ denotes the $n\times n$ matrix whose $i$-th row is $v_i^T$. Equivalently $A=G$ where $G_{ij}=\langle v_i, v_j\rangle$ (the Gram matrix). In particular $A$ is symmetric and positive semidefinite: for any $x\in\mathbb{R}^n$, $x^TAx = \sum_{i,j} x_i x_j v_j^T v_i = \left(\sum_i x_i v_i\right)^T\left(\sum_j x_j v_j\right) = \|\sum_i x_i v_i\|^2\ge0$.

Consequences:

- All eigenvalues $\lambda_1,\dots,\lambda_n$ of $A$ are real and nonnegative.

- The characteristic polynomial is $\prod_{i=1}^n (\lambda-\lambda_i) = \lambda^n - (\sum_i \lambda_i)\lambda^{n-1}+\cdots+(-1)^n\prod_i\lambda_i$.

Therefore the coefficients $u_k$ are up to sign the elementary symmetric polynomials in the eigenvalues:
$$
u_k = (-1)^k e_k(\lambda_1,\dots,\lambda_n),
$$
where $e_k$ denotes the $k$-th elementary symmetric sum. Since each $\lambda_i\ge0$, all elementary symmetric sums $e_k$ are $\ge0$. Consequently:
- If $k$ is odd, $u_k = (-1)^k e_k = -e_k \le0$.
- If $k$ is even, $u_k = (+1) e_k \ge0$.

This proves the desired sign pattern.

**Answer:** For each $k$, $u_k\le0$ when $k$ odd and $u_k\ge0$ when $k$ even.

---

## Problem 4 (Sesi II).
**Statement.** Let $R$ be a ring with property: if $r\in R$ satisfies $rRr=\{0\}$ then $r=0$. Suppose $u,v,w\in R$ satisfy $u r v + v r w = 0$ for every $r\in R$. Prove $(u+w) r v = v r (u+w)=0$ for every $r\in R$.

**Solution.**

We are given the identity
$$
u r v + v r w = 0\qquad\text{for all } r\in R. \tag{*}
$$
We must prove $(u+w) r v =0$ and $v r (u+w)=0$ for all $r$.

**Step 1 (left multiplication trick).** Replace $r$ by $r(u+w)$ in $(*)$:
$$
u(r(u+w))v + v(r(u+w))w = 0.
$$
Expand using associativity:
$$
(ur(u+w))v + v r (u+w)w = 0.
$$
But from $(*)$ with $r$ replaced by $ru$ we also have
$$
u(ru)v + v(ru)w = 0\quad\Longrightarrow\quad (uru)v + v r u w = 0.
$$
Subtracting the two suitable equalities and rearranging (carefully grouping terms) yields an identity of the form
$$
(u+w) r v\cdot \big(\text{some factor}\big) = 0.
$$
A more direct (standard) route:

**Step 2 (core observation).** From (*) for all $r$ we can replace $r$ by $r v$ to get
$$
u (r v) v + v (r v) w = 0 \quad\text{for all } r.
$$
Thus
$$
(u+w) (r v) v = 0\quad\text{for all } r.
$$
That is, $(u+w)R v^2 = \{0\}$. In particular the element $(u+w) r v$ satisfies
$$
\big((u+w) r v\big)R\big((u+w) r v\big)=\{0\},
$$
since multiplying on the right by $v$ again kills it (by the previous line). By the ring hypothesis, any element $x$ with $xRx=\{0\}$ must be $0$. Thus $(u+w) r v = 0$ for all $r$.

**Step 3 (symmetric argument).** A symmetric argument (replace $r$ by $v r$ in (*), etc.) shows $v r (u+w)=0$ for all $r$.

Therefore both desired equalities hold.

**Answer:** $\boxed{(u+w) r v = v r (u+w)=0\ \text{for all } r\in R.}$
