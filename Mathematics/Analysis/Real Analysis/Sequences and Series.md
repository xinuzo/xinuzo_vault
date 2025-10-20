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
Let $(x_{n})$ be a sequence of real numbers and let $x \in \mathbb{R}$ If $(a_{n})$ is a sequence of positive real numbers with $lim(a_{n}) = 0$ and if for some constant C > 0 and some m E N we have l xn - xl ::; Can fo r all n -2: m, then it fo llows that lim(xn) = x.

exists a real number M > 0 such that lxn I :S M for all n E N. Thus, the sequence (xn) is bounded if and only if the set { Xn : n E N} of its values is a bounded subset of R 3.2.2 Theorem A convergent sequence of real numbers is bounded. Proof Suppose that lim(xn) = x and let e := I. Then there exists a natural number K = K(l) such that lxn- xl < I for all n 2: K. If we apply the Triangle Inequality with n 2: K we obtain If we set l xnl = lxn -X+ xl :S lxn - xl + lxl < 1 + lxl M := sup{ lx, l , lx2l , . . . , lxK- I I , 1 + lxl }, then it follows that lxn I :S M for all n E N.

3.2.4 Theorem If X= (x,) is a convergent sequence of real numbers and ifx11 ;:::: Ofor all n E N, then x = lim(x11) ;:::: 0.

3.2.7 Squeeze Theorem Suppose that X= (x11), Y = (y11), and Z = (zn) are sequences of real numbers such that Xn :s; Yn :s; Zn for all n E N, and that lim(x11) = lim(z11). Then Y = (y11) is convergent and lim(xn) = Iim(y11) = Iim(zn)· Proof Let w := Iim(xn) = Iim(z11). If e > 0 is given, then it follows from the conver gence of X and Z to w that there exists a natural number K such that if n � K then J xn- w J < e and Since the hypothesis implies that : s ; Yn - w :s; Zn - w for all n E N, Xn - w it follows (why?) that -e < Yn- w < e for all n � K. Since e > 0 is arbitrary, this implies that Iim(y11) = w.

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