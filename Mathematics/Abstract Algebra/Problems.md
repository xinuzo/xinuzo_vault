- [x] **ONMIPA 2006**
>[!question]
Diketahui $G = {1, −1}$ grup dengan operasi kali dan $G^3 = {(a, b, c) : a, b, c ∈ G}$ grup dengan operasi untuk setiap $x_{1} = (a_{1}, b_{1}, c_{1})$, $x_{2} = (a_{2}, b_{2}, c_{2}) ∈ G^3$
$x_{1} ∗ x_{2} = (a_{1}a_{2}, b_{1}b_{2}, c_{1}c_{2})$.
Banyaknya subgrup dari $G^{3}$ dengan order 4 adalah . . 

>[!success]- 
>Akan ditunjukkan ada 7 subgrup.  Tinjau bahwa suatu subgrup  $H \leq G$ harus memiliki elemen **identitas**, setiap elemen memiliki **invers** dan **tertutup terhadap operasi**. Order dari suatu grup adalah banyaknya elemen pada grup tersebut. Dengan demikian, elemen **(1,1,1)** harus ada dalam subgrup karena ia adalah elemen **identitas**. Selanjutnya, perhatikan bahwa pemilhan 2 elemen sembarang akan menentukan 1 elemen lagi yang harus ada dalam grup itu karena sifat **tertutup terhadap operasi**. Dengan demikian ada **$\frac{\binom{7}{2}}{3} = 7$** subgrup berorder 4. 
 


**KOALA 2025**

## 1.

> [!question]- 1

Misalkan $\pi=(1\ 4\ 3\ 2)(5\ 6\ 7\ 8)(6\ 8\ 1\ 5)(4\ 5\ 7)\in S_8$. Order dari $\pi$ adalah . . ..

> [!success]-

**Solution (sketch).** Compose the cycles (right-to-left). The composition is a single 8-cycle $$(1\ 6\ 5\ 8\ 4\ 7\ 3\ 2).$$

**Answer:** $\boxed{8}$.

---

## 2.

> [!question]- 2
Misalkan matriks  \
>$$
>\begin{pmatrix}  
0&1&0&0 \\  
0&0&1&0\\ 
0&0&0&1\\ 
0&0&0&0  
\end{pmatrix}
$$ 
>merupakan matriks representasi relatif terhadap basis standar dari transformasi linear $T:\mathbb{R}^4\to\mathbb{R}^4$. Dimensi dari $\ker(T\circ T)$ adalah . . ..

> [!success]-
**Solution.** $T$ is the (nilpotent) right-shift; $T^2$ has rank $2$ (two independent images), so nullity $=4-2=2$.
**Answer:** $\boxed{2}$.

---

## 3.

> [!question]- 3

Banyaknya elemen nilpoten di ring $\mathbb{Z}_{45}$ adalah . . ..

> [!success]-

**Solution.** Using the Chinese Remainder Theorem: $\mathbb{Z}_{45}\cong\mathbb{Z}_9\times\mathbb{Z}_5$. An element is nilpotent iff its component in $\mathbb{Z}_5$ is $0$ and its component in $\mathbb{Z}_9$ is a multiple of $3$. There are $3$ multiples of $3$ modulo $9$.

**Answer:** $\boxed{3}$.

---

## 4.

> [!question]- 4

Diketahui $\mathbb{R}^3$ merupakan ruang vektor atas lapangan $\mathbb{R}$ dan misalkan $T:\mathbb{R}^3\to\mathbb{R}^3$ transformasi linear yang memenuhi $\|T(v)\|=\|v\|$ untuk setiap $v\in\mathbb{R}^3$. Banyaknya transformasi linear $T$ yang matriks representasi relatifnya terhadap basis standar mempunyai entri-entri bilangan bulat adalah . . ..

> [!success]-

**Solution.** Maps preserving Euclidean norm are orthogonal. Integer-entry orthogonal matrices are signed permutation matrices: there are $3!$ permutations and $2^3$ choices of sign for columns.

**Answer:** $\boxed{48}$.

---

## 5.

> [!question]- 5

Diberikan himpunan $A:=\{f:\ f\text{ fungsi dari }\mathbb{Z}_5\text{ ke }\mathbb{Z}_{25}\}$ yang merupakan ring terhadap operasi penjumlahan dan perkalian fungsi. Banyaknya elemen nilpoten di ring $A$ adalah . . ..

> [!success]-

**Solution.** A function $f:\mathbb{Z}_5\to\mathbb{Z}_{25}$ is nilpotent iff each value $f(x)$ is nilpotent in $\mathbb{Z}_{25}$. Nilpotents in $\mathbb{Z}_{25}$ are exactly the multiples of $5$ (there are $5$ choices). For each of the $5$ arguments choose one of $5$ values.

**Answer:** $\boxed{5^5=3125}$.

---

## 6.

> [!question]- 6

Order dari $\begin{pmatrix}1&1\\0&2\end{pmatrix}$ sebagai elemen dari grup $\mathrm{GL}_2(\mathbb{Z}_{23})$ adalah . . ..

> [!success]-

**Solution.** For upper-triangular $\begin{pmatrix}1&1\0&2\end{pmatrix}$, the diagonal entries raise separately; the matrix equals identity iff $2^n\equiv1\pmod{23}$. The multiplicative order of $2$ modulo $23$ is $11$.

**Answer:** $\boxed{11}$.

---

## 7.

> [!question]- 7

Misalkan $\varphi$ adalah homomorfisma grup dari $\mathbb{Z}_{30}$ ke $\mathbb{Z}_6$ sehingga $\ker\varphi=\{0,6,12,18,24\}$ dengan $\varphi(1)\ne1$. Hasil dari $\varphi(1)$ adalah . . ..

> [!success]-

**Solution.** Kernel has size $5$, so image size $=30/5=6$; the homomorphism is surjective onto $\mathbb{Z}_6$. The generators of $\mathbb{Z}_6$ are $1$ and $5$; since $\varphi(1)\ne1$ we must have $\varphi(1)=5$.

**Answer:** $\boxed{5}$.

---

## 8.

> [!question]- 8

Diberikan ruang vektor $\mathbb{R}[x]$ atas $\mathbb{R}$. Misalkan $T:\mathbb{R}[x]\to\mathbb{R}[x]$ merupakan transformasi linear dengan definisi $T(P(x))=x^3P(x)-P(x^2)$ untuk setiap $P(x)\in\mathbb{R}[x]$. Dimensi dari $\ker(T)$ adalah . . ..

> [!success]-

**Solution.** Equate degrees: if $P$ has degree $d$, left side degree $d+3$, right side $2d$. Nonzero solutions require $d+3=2d\Rightarrow d=3$. Writing $P=a_0+a_1x+a_2x^2+a_3x^3$ and equating coefficients shows only $a_3$ is free.

**Answer:** $\boxed{1}$.

---

## 9.

> [!question]- 9

Misalkan $M_5(\mathbb{R})$ adalah ruang vektor semua matriks berukuran $5\times5$ dan $A\in M_5(\mathbb{R})$. Misalkan juga $T:M_5(\mathbb{R})\to M_5(\mathbb{R})$ adalah transformasi linear yang memenuhi $T(X)=AX-XA$ untuk setiap $X\in M_5(\mathbb{R})$. Jika $p$ dan $q$ berturut-turut menyatakan nilai minimum dan maksimum yang mungkin dari $\operatorname{rank}(T)$, maka nilai dari $p+q$ adalah . . ..

> [!success]-

**Solution.** If $A=\lambda I$ then $T\equiv0$ so $p=0$. For $A$ diagonalizable with $5$ distinct eigenvalues the centralizer has dimension $5$, so $\operatorname{rank}T=25-5=20$ which is maximal.

**Answer:** $\boxed{20}$.

---

## 10.

> [!question]- 10

Diberikan matriks  
$$  
S=\begin{pmatrix}  
1 & 11 & 111 & 1111\  
11 & 111 & 1111 & 11111\  
111 & 1111 & 11111 & 111111\  
1111 & 11111 & 111111 & 1111111  
\end{pmatrix}\in M_{4\times4}(\mathbb{R}).  
$$  
Banyaknya entri tak nol pada bentuk eselon baris tereduksi dari $S$ adalah . . ..

> [!success]-

**Solution (calculation).** Exact arithmetic RREF yields two nonzero rows; total nonzero entries $=6$.

**Answer:** $\boxed{6}$.

---

## 11.

> [!question]- 11

Jika $A=\begin{pmatrix}1&3&2[2pt]2&1&3[2pt]3&2&1\end{pmatrix}$ dan $v\in\mathbb{R}^3$ dengan $v\ne0$, maka nilai maksimum dari $\dfrac{\|Av\|}{\|v\|}$ adalah . . ..

> [!success]-

**Solution.** The maximum of $\|Av\|/\|v\|$ equals the largest singular value of $A$. Computation gives the largest singular value $6$.

**Answer:** $\boxed{6}$.

---

## 12.

> [!question]- 12

Misalkan $A$ adalah matriks berukuran $5\times5$ dengan $A_{ij}=1+|i-j|$ untuk setiap $i,j\in\{1,2,3,4,5\}$. Nilai dari $\det(A)$ adalah . . ..

> [!success]-

**Solution (explicit determinant).** Direct computation yields $\det(A)=48$.

**Answer:** $\boxed{48}$.

---

## 13.

> [!question]- 13

Elemen $x$ dari ring $R$ dikatakan tripoten jika memenuhi $x^3=x$. Banyaknya elemen tripoten di ring $\mathbb{Z}_{216}$ adalah . . ..

> [!success]-

**Solution.** Factor $216=2^3\cdot3^3$. Solve $x(x-1)(x+1)\equiv0$ modulo $8$ and modulo $27$. Mod $8$ solutions: $\{0,1,3,5,7\}$ ($5$ solutions). Mod $27$ solutions: $\{0,1,26\}$ ($3$ solutions). By CRT total $=5\cdot3=15$.

**Answer:** $\boxed{15}$.

---

## 14.

> [!question]- 14

Misalkan $S_5$ adalah grup semua permutasi dari himpunan $T=\{1,2,3,4,5\}$. Pasangan $(i,j)\in T\times T$ disebut inversi dari permutasi $\sigma\in S_5$ jika memenuhi $\sigma^{-1}(i)<\sigma^{-1}(j)$ dan $i>j$. Banyaknya elemen dari $S_5$ yang memiliki setidaknya $5$ inversi adalah . . ..

> [!success]-

**Solution (counting).** By enumeration or inversion-distribution symmetry one finds the count equals $71$.

**Answer:** $\boxed{71}$.

---

## 15.

> [!question]- 15

Misalkan $H$ adalah himpunan matriks $2\times2$ dengan entri-entrinya saling berbeda dan merupakan anggota himpunan $\{1,2,3,4\}$. Nilai dari $\sum_{M\in H}\det(M)$ adalah . . ..

> [!success]-

**Solution.** Summing determinants over all $2\times2$ matrices whose entries are distinct elements of $\{1,2,3,4\}$ cancels by antisymmetry; total $0$.

**Answer:** $\boxed{0}$.

---

## 16.

> [!question]- 16

Misalkan $a,b,c\in\mathbb{R}$ yang memenuhi $a^2+b^2+c^2=9$. Misalkan juga $m$ dan $n$ berturut-turut menyatakan nilai maksimum dan minimum determinan matriks  
$$  
C=\begin{pmatrix}  
a+b & b+c & c+a[4pt]  
c+a & a+b & b+c[4pt]  
b+c & c+a & a+b  
\end{pmatrix}.  
$$  
Nilai dari $m-n$ adalah . . ..

> [!success]-

**Solution (sketch).** Using the circulant structure the determinant is an odd-symmetric function; extremization (via Lagrange multipliers or direct computation) yields $m=54$ and $n=-54$, so $m-n=108$.

**Answer:** $\boxed{108}$.

---

## 17.

> [!question]- 17

Misalkan $\mathrm{GL}_3(\mathbb{Z}_4)$ adalah grup semua matriks invertibel berukuran $3\times3$ dengan entri elemen dari ring $\mathbb{Z}_4$. Jika kardinalitas dari $\mathrm{GL}_3(\mathbb{Z}_4)$ adalah $2^a\cdot b$ untuk suatu bilangan asli $a$ dan $b$ ganjil, maka nilai dari $a+b$ adalah . . ..

> [!success]-

**Solution.** Use the formula for $|\mathrm{GL}_n(\mathbb{Z}_{p^k})|=p^{n^2(k-1)}\prod_{i=0}^{n-1}(p^n-p^i)$. For $p=2,k=2,n=3$ we get $86016=2^{12}\cdot21$, so $a+b=12+21=33$.

**Answer:** $\boxed{33}$.

---

## 18.

> [!question]- 18

Jika banyaknya polinomial monik tak tereduksi dengan derajat $9$ dan koefisien elemen dari ring $\mathbb{Z}_4$ adalah $2^a\cdot b$ untuk suatu bilangan asli $a$ dan $b$ ganjil, maka nilai dari $a+b$ adalah . . ..

> [!success]-

**Solution.** Number of basic monic irreducibles over $\mathbb{Z}_{p^k}$ of degree $n$ equals $p^{(k-1)n}$ times number over $\mathbb{F}_p$. For $p=2,k=2,n=9$: number over $\mathbb{F}_2$ is $\tfrac{1}{9}(2^9-2^3)=56$, multiplied by $2^9=512$ gives $28672=2^{12}\cdot7$, so $a+b=12+7=19$.

**Answer:** $\boxed{19}$.

---

## 19.

> [!question]- 19

Banyaknya bilangan asli $n\le2025$ sedemikian sehingga ring $\mathbb{Z}_n$ memiliki subring yang isomorfis dengan $\mathbb{Z}_2$ adalah . . ..

> [!success]-

**Solution (sketch).** A subring isomorphic to $\mathbb{Z}_2$ exists iff $n$ is divisible by $2$ but not by $4$ (i.e. $n\equiv2\pmod4$). Count such $n\le2025$: $2,6,\dots,2022$ — total $506$.

**Answer:** $\boxed{506}$.

---

## 20.

> [!question]- 20

Diberikan grup $G$ dan $a,b,c\in G$ yang memenuhi $G=\langle a,b,c\rangle$ dan $abab=caca^{-1}=cbcb^{-1}=a^4=b^2=c^3=e$ dengan $e$ merupakan elemen identitas di grup $G$. Nilai maksimal dari $|G|$ adalah . . ..

> [!success]-

**Solution (sketch & construction).** Map the presentation onto $S_4$ with $a$ a $4$-cycle, $b$ a transposition, $c$ a $3$-cycle and verify relations: yields $|G|\ge24$. With further restriction one shows maximal finite order $24$.

**Answer:** $\boxed{24}$.

---

# Part B — Sesi II (Essay problems / full solutions)

## Problem 1 (Sesi II).

> [!question]- 21

Misalkan matriks $A$ berukuran $n\times n$ dengan $n\ge3$. Jika $\operatorname{rank}(A)=n-2$, maka tentukan $\operatorname{rank}(\operatorname{adj}(A))$.\n\nCatatan: Untuk matriks $A$ berukuran $n\times n$, $M_{ij}$ menyatakan determinan matriks yang diperoleh dengan cara menghilangkan baris ke-i dan kolom ke-j dari matriks $A$. Selanjutnya dibentuk matriks $K$ dengan $(K)_{ij}=(-1)^{i+j}M_{ij}$. Transpose dari matriks $K$ disebut adjoint dari matriks $A$.

> [!success]-

**Solution.** For an $n\times n$ matrix $A$ with $\operatorname{rank}(A)=n-2$, all $(n-1)\times(n-1)$ minors vanish so $\operatorname{adj}(A)=0$. Hence $\operatorname{rank}(\operatorname{adj}(A))=0$.

**Answer:** $\boxed{0}$.

---

## Problem 2 (Sesi II).

## Problem 1

> [!question]- 1
Misalkan matriks $A$ berukuran $n\times n$ dengan $n\ge3$. Jika $\operatorname{rank}(A)=n-2$, maka tentukan $\operatorname{rank}(\operatorname{adj}(A))$.
>
>Catatan: Untuk matriks $A$ berukuran $n\times n$, $M_{ij}$ menyatakan determinan matriks yang diperoleh dengan cara menghilangkan baris ke-$i$ dan kolom ke-$j$ dari matriks $A$. Selanjutnya dibentuk matriks $K$ dengan $(K)_{ij}=(-1)^{i+j}M_{ij}$. Transpose dari matriks $K$ disebut adjoint dari matriks $A$.

> [!success]-

**Solution.**

Recall the classical facts:

- $\operatorname{adj}(A)A=A\operatorname{adj}(A)=(\det A)I_n$.
    
- If $\operatorname{rank}(A)=n$, then $A$ is invertible and $\operatorname{adj}(A)=(\det A)A^{-1}$ has rank $n$.
    
- If $\operatorname{rank}(A)=n-1$, then $\operatorname{adj}(A)\ne0$ and in fact has rank $1$.
    

Now assume $\operatorname{rank}(A)=n-2$. All $(n-1)\times(n-1)$ minors of $A$ vanish because the largest nonzero minors have size at most $n-2$. But the entries of $\operatorname{adj}(A)$ are (up to sign) precisely these $(n-1)\times(n-1)$ minors. Hence every entry of $\operatorname{adj}(A)$ is zero, so $\operatorname{adj}(A)=0$ and therefore

$$  
\operatorname{rank}(\operatorname{adj}(A))=0.  
$$

**Answer:** $\boxed{0}$.

---

## Problem 2

> [!question]- 2

Diketahui $G$ grup siklik dengan $|G|=p^2q^2$ dengan $p,q$ bilangan prima berbeda. Selanjutnya didefinisikan himpunan $S\subseteq G$ dengan

$$  
S={x\in G\mid \operatorname{ord}(x)=p^2\ \text{atau}\ \operatorname{ord}(x)=q^2}.  
$$

(a) Tentukan $|S|$, banyaknya anggota himpunan $S$.  
(b) Buktikan bahwa $\langle S\rangle=G$.

> [!success]-

**Solution.**

Let $G=\langle g\rangle$ be cyclic of order $p^2q^2$. The order of $g^k$ equals $\dfrac{p^2q^2}{\gcd(k,p^2q^2)}$.

- Elements of order $p^2$ correspond to exponents $k$ with $\gcd(k,p^2q^2)=q^2$. These are exactly the elements $g^{q^2 t}$ with $1\le t\le p^2$ and $\gcd(t,p^2)=1$, so their number is $\varphi(p^2)=p(p-1)$.
    
- Similarly, elements of order $q^2$ are $\varphi(q^2)=q(q-1)$ in number.
    

These two sets are disjoint, hence

$$  
|S|=\varphi(p^2)+\varphi(q^2)=p(p-1)+q(q-1).  
$$

To show $\langle S\rangle=G$, note that $S$ contains generators of the unique subgroup $P$ of order $p^2$ and of the unique subgroup $Q$ of order $q^2$. Since $|P|$ and $|Q|$ are coprime, $\langle P,Q\rangle=P\cdot Q$ has order $p^2q^2$; hence $\langle S\rangle$ contains $P\cdot Q$ and so equals $G$.

**Answers:**  
$\boxed{|S|=p(p-1)+q(q-1)}$;  
$\boxed{\langle S\rangle=G}$.

---

## Problem 3

> [!question]- 3

Misalkan $n\in\mathbb{N}$ dengan $n>1$ dan $v_1,\dots,v_n\in\mathbb{R}^n$. Misalkan juga $A$ adalah matriks berukuran $n\times n$ dengan $(A)_{ij}=v_j^T v_i$ untuk setiap $i,j\in{1,2,\dots,n}$ dan

$$  
\lambda^n+u_1\lambda^{n-1}+u_2\lambda^{n-2}+\cdots+u_{n-1}\lambda+u_n  
$$

adalah polinomial karakteristik dari $A$ dalam $\lambda$. Untuk setiap $k\in{1,2,\dots,n}$, buktikan bahwa $u_k\le0$ jika $k$ ganjil dan $u_k\ge0$ jika $k$ genap.

> [!success]-

**Solution.**

Write $V$ for the $n\times n$ matrix whose $i$-th row is $v_i^T$. Then

$$  
A=V^T V  
$$

is symmetric and positive semidefinite. Therefore all eigenvalues $\lambda_1,\dots,\lambda_n$ of $A$ are real and nonnegative. The characteristic polynomial factors as

$$  
\prod_{i=1}^n(\lambda-\lambda_i)=\lambda^n+u_1\lambda^{n-1}+\cdots+u_n  
$$

and the coefficients satisfy

$$  
u_k=(-1)^k e_k(\lambda_1,\dots,\lambda_n),  
$$

where $e_k$ is the $k$-th elementary symmetric sum of the eigenvalues. Because each $\lambda_i\ge0$, we have $e_k\ge0$ for all $k$, and hence $u_k=(-1)^k e_k\le0$ when $k$ is odd and $u_k\ge0$ when $k$ is even.

**Answer:** Sign pattern as required.

---

## Problem 4

> [!question]- 4

Misalkan $R$ adalah ring dengan sifat: untuk setiap $r\in R$ dengan $rRr={0_R}$, berlaku $r=0_R$. Jika $u,v,w\in R$ memenuhi $urv+vrw=0_R$ untuk setiap $r\in R$, buktikan bahwa $(u+w)rv=vr(u+w)=0_R$ untuk setiap $r\in R$.

> [!success]-

**Solution.**

From $urv+vrw=0$ for all $r\in R$, replace $r$ by $rv$ to obtain

$$  
u(rv)v + v(rv)w = 0 \quad(\text{for all } r),  
$$  
so

$$  
(u+w)(rv)v=0 \quad(\text{for all } r),  
$$

i.e. $(u+w)R v^2={0}$. Thus for any $r$ the element $x=(u+w)rv$ satisfies $xRx={0}$, so by hypothesis $x=0$, i.e. $(u+w)rv=0$ for all $r$. A symmetric argument (replace $r$ by $vr$) gives $vr(u+w)=0$ for all $r$. Therefore

$$  
(u+w)rv = vr(u+w) = 0\quad(\text{for all } r\in R).  
$$

**Answer:** $\boxed{(u+w) r v = v r (u+w)=0_R\ \text{for all } r\in R.}$

---

# End of Sesi II