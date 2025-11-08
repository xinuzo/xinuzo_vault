>[!tips] 3.1.1  (Definition) Sequence
>A sequence of real numbers (sequence in $\mathbb{R}$ is a function defined on the set $\mathbb{N} = { 1, 2, . . . }$ of natural numbers whose range is contained in the set $\mathbb{R}$. of real numbers.

>[!tips] 3.1.3 (Definition) Convergence
> A sequence $X= (x_{n})$ in $\mathbb{R}$ is said to **converge** to $x \in \mathbb{R}$, or $x$ is said to be a **limit** of $(X_{n})$, if  $\forall \epsilon  > 0$, $\exists K(\epsilon) \in \mathbb{N}$ $\ni n\geq K(\epsilon) \implies |x_{n}-x|<\epsilon.$

>[!tips] (Theorem) 3.1.4 Uniqueness of Limits 
>A sequence in $\mathbb{R}$ can have at most one limit.

>[!success]- Proof.
> Suppose that $x'$ and $x"$ are both limits of $(x_{n})$. For each $\epsilon>0$  there exist $K'$ such that $|x_{n}- x'|< \frac{\epsilon}{2}$ for all $n_{\epsilon}\geq K'$, and there exists $K"$ such that $|x_{n}- x''| < \frac{\epsilon}{2}$ for all $n_{{\epsilon}}\geq K''$. Let $K=max\{K',K''\}$, then for $n_{\epsilon}\geq K$ by  the Triangle Inequality we get $|x'-x''|=|x'-x+x-x''|\leq|x'-x_{n}|+|x''-x_{n}|=\frac{\epsilon}{2}+\frac{\epsilon}{2}=\epsilon.$. 
> Since $\epsilon>0$ is an arbitrary positive number, we conclude that $x'-x''=0$.

>[!tips] (Definition) m-tail Sequences
> If $X = ( x_{1} , x_{2}, . . . , X_{n}, . . . )$ is a sequence of real numbers and if m is a given natural number, then the m-tail of X is the sequence Xm := (xm+n : n E N) = (xm+l , Xm+2, . . . ) For example, the 3-tail of the sequence X = (2, 4, 6, 8, 10, . . . , 2n, . . . ), is the sequence x3 = (8, 10, 12, . . . , 2n + , . . . ). 

>[!tips] 3.1.9 Theorem
> Let X = (xn : n EN) be a sequence of real numbers and let mEN. Then the m-tail Xm = (xm+n : n E N) of X converges if and only if X converges. In this case, limXm = lim X. 

> [!success]- Proof
>  We note that _for any p E N, the pth term of Xm is the (p + m)th term of X. Similarly, if q > m, then the qth term of X is the (q- m)th term of Xm. Assume X converges to x. Then given any 1; > 0, if the terms of X for n 2 K( t:) satisfy lxn- xl < B, then the terms of Xm for k 2 K(e)- m satisfy lxk- xl

>[!tips] 3.1.10 Theorem 
Let $(x_{n})$ be a sequence of real numbers and let $x \in \mathbb{R}$ If $(a_{n})$ is a sequence of positive real numbers with $lim(a_{n}) = 0$ and if for some constant $C > 0$ and some $m \in \mathbb{N}$ we have $|x_{n} - x| <C$ an fo r all n -2: m, then it fo llows that lim(xn) = x.

>[!tips] Definisi: Barisan Terbatas

Sebuah barisan $(x_n)$ dikatakan terbatas jika terdapat sebuah bilangan real $M > 0$ sedemikian sehingga $|x_n| \le M$ untuk semua $n \in \mathbb{N}$.

Dengan demikian, barisan $(x_n)$ terbatas jika dan hanya jika himpunan nilai-nilainya $\{x_n : n \in \mathbb{N}\}$ adalah himpunan bagian terbatas dari $\mathbb{R}$.

[!success]

3.2.2 Teorema: Barisan Konvergen Pasti Terbatas

Sebuah barisan bilangan real yang konvergen adalah terbatas.

Bukti: Misalkan $\lim(x_n) = x$ dan ambil $\epsilon := 1$. Maka terdapat sebuah bilangan asli $K = K(1)$ sedemikian sehingga $|x_n - x| < 1$ untuk semua $n \ge K$.

Jika kita menerapkan Ketaksamaan Segitiga untuk $n \ge K$, kita peroleh:

$$|x_n| = |x_n - x + x| \le |x_n - x| + |x| < 1 + |x|$$

Jika kita menetapkan:

$$M := \sup\{ |x_1|, |x_2|, \dots, |x_{K-1}|, 1 + |x| \}$$

maka berlaku $|x_n| \le M$ untuk semua $n \in \mathbb{N}$.

3.2.4 Teorema

Jika $X = (x_n)$ adalah barisan bilangan real yang konvergen dan jika $x_n \ge 0$ untuk semua $n \in \mathbb{N}$, maka $x = \lim(x_n) \ge 0$.

3.2.7 Teorema Apit (Squeeze Theorem)

Misalkan $X = (x_n)$, $Y = (y_n)$, dan $Z = (z_n)$ adalah barisan bilangan real sedemikian sehingga:

$$x_n \le y_n \le z_n \quad \text{untuk semua } n \in \mathbb{N}$$

dan $\lim(x_n) = \lim(z_n)$. Maka $Y = (y_n)$ adalah konvergen dan:

$$\lim(x_n) = \lim(y_n) = \lim(z_n)$$

Bukti: Misalkan $w := \lim(x_n) = \lim(z_n)$. Jika diberikan $\epsilon > 0$, maka dari konvergensi $X$ dan $Z$ ke $w$, terdapat sebuah bilangan asli $K$ sedemikian sehingga jika $n \ge K$ maka:

$$|x_n - w| < \epsilon \quad \text{dan} \quad |z_n - w| < \epsilon$$

Karena hipotesis menyiratkan bahwa $x_n - w \le y_n - w \le z_n - w$ untuk semua $n \in \mathbb{N}$, maka (mengapa?) berlaku:

$$-\epsilon < y_n - w < \epsilon$$

untuk semua $n \ge K$. Karena $\epsilon > 0$ adalah sembarang, ini menyiratkan bahwa $\lim(y_n) = w$.
>[!tips] 3.3.1 (Definition) Monotone Increasing (Decreasing)
> Let $X= (x_{n})$ be a sequence of real numbers.  $X$ is **increasing** if it satisfies the inequalities
> $x_{1}\leq x_{2}\leq\dots\leq x_{n}\leq x_{n+1}\leq\dots$.
$X$ is **decreasing** if it satisfies the inequalities $x_{1}\geq x_{2}\geq\dots\geq x_{n}\geq x_{n+1}\geq\dots$

3.3.2 Monotone Convergence Theorem A monotone sequence of real numbers is convergent if and only if it is bounded. Further: 72 CHAPTER 3 SEQUENCES AND SERIES (a) If X = (xn) is a bounded increasing sequence, then lim(xn) = sup{xn : n E N}. (b) If Y = (yn) is a bounded decreasing sequence, then Iim(yn) = inf{Yn : n E N}.

3.4.1 Definition Let X= (xn) be a sequence of real numbers and let n1 < n2 < · · · < nk < · · · be a strictly increasing sequence of natural numbers. Then the sequence X' = ( Xnk ) given by ( Xnl ' Xn2 ' . . . ' Xnk ' . . . ) is called a subsequence of X.

3.4.5 Divergence Criteria If a sequence X= (xn) of real numbers has either of the fo llowing properties, then X is divergent. (i) X has two convergent subsequences X' = (xnk) and X" = (xrk ) whose limits are not equal. (ii) X is unbounded.

>[!tips] 3.4.8 The Bolzano-Weierstrass Theorem
>A bounded sequence of real numbers has a convergent subsequence. 

>[!success]-  Proof.
> It follows from the **Monotone Subsequence Theorem** that if X= (xn) is a bounded sequence, then it has a subsequence X' = ( Xnk ) that is monotone. Since this subsequence is also bounded, it follows from the Monotone Convergence Theorem 3.3.2 that the subsequence is convergent.