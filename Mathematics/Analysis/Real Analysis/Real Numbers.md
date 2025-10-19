
>[!tips] Algebraic Properties of $\mathbb{R}$
>The set of real numbers ($\mathbb{R}$) equipped with two binary operations $(.) \text{ and } (+)$ satisfies the following properties: 
>
>(**A1**) $a+b=b+a$  $\forall a,b \in \mathbb{R}$ (**Commutativity of Addition**)
>(**A2**) $(a+b)+c=a+(b+c)$ $\forall a,b,c \in \mathbb{R}$ (**Associativity of Addition**)
>(**A3**) $\exists -a \in \mathbb{R} \ni a+(-a)=(-a)+a=0$ $\forall a \in \mathbb{R}$ (**Existence of Additive Inverse**)
>(**A4**) $\exists 0 \in \mathbb{R} \ni a+0=0+a=a$ $\forall a \in \mathbb{R}$ (**Existence of Additive Identity**)
>(**M1**) $(a \cdot b)\cdot c= a \cdot(b\cdot c)$ $\forall a,b,c \in \mathbb{R}$ (**Associativity of Multiplication**)
>(**M2**) $a\cdot b=b\cdot a$ $\forall a,b \in \mathbb{R}$ (**Commutativity of Multiplication**)
>(**M3**) $\exists \frac{1}{a} \ni a \cdot \frac{1}{a}=\frac{1}{a} \cdot a=1$ (**Existence of Multiplicative Inverse**)
>(**M4**) $\exists 1 \ni 1\cdot a=a\cdot 1=a$ $\forall a \in \mathbb{R}$ (**Existence of Muliplicative Identity**)
>(**D**) $a\cdot(b+c)=a\cdot b+a\cdot c$ and $(b+c)\cdot a=b\cdot a+c\cdot a$ $\forall a,b,c \in \mathbb{R}$ (**Distributive**)

There are 9 of these. 

>[!tips]  The Order Properties of $\mathbb{R}$
 There is a nonempty subset $P$ of $\mathbb{R}$, called the set of positive real numbers, that satisfies the following properties: 
 (i) $a,b\in P \implies a+b\in P$
 (ii)  $a,b\in P \implies ab \in P$
  (iii)  If $a\in \mathbb{R}$ , then exactly one of the following holds:
>$$
>a \in P \qquad a=0 \qquad -a \in P
>$$

The third property is also called **Trichotomy Property**

>[!tips] (Definition) Bounded Sets
> Let $S$ be a nonempty subset of $\mathbb{R}$
>  (a) The set S is said to be **bounded above** if there **exists** a number $u\in \mathbb{R}$ such that $s\leq u$ for all $s \in S$.  $u$ is called an **upper bound** of S.
>   (b) The set S is said to be **bounded below** if there exists a number $w\in \mathbb{R}$ such that $w\leq s$ for all $s \in S$. $w$ is called a **lower bound** of S.
>   (c) A set is said to be **bounded** if it is **both bounded above** and **bounded below**. A set is said to be **unbounded** if it is **not bounded**.

>[!tips] (Definition) Supremum Infimum
> Let $S$ be a nonempty subset of $\mathbb{R}$ 
> (a)  If $S$ is bounded above, then a number $u$ is said to be a supremum (or a least upper bound) of $s$ if it satisfies the conditions: 
> (1) $u$ is an upper bound of $$S$
>  (2) if v is any upper bound of S, then u :::; v. 
> 
> (b) If Sis bounded below, then a number w is said to be an infimum (or a greatest lower (1') w bound) of S if it satisfies the conditions: is a lower bound of S, and (2') if t is any lower bound of S, then t :::; w.


>[!tips] Completeness  Axiom of $\mathbb{R}$
>Every nonempty set of **real numbers** that is **bounded above (below)** has a **least upper (greatest lower)** bound in $\mathbb{R}$.


>[!tips] Archimedean Property
> If $x \in R$, then there exists $n_{x}\in \mathbb{N}$ E N such that $n_{x}\geq x$.
> 

>[!success]- Proof 
>Assume the assertion is false, then $n_{x}<x$ for all $\forall n\in \mathbb{N}$. Therefore, $x$ is an upper bound of N. Therefore, by the Completeness Property, the non empty set $\mathbb{N}$ has a supremum $u\in \mathbb{R}$. Subtracting $1$ from $u$ gives a number $u - 1$, which is smaller than the supremum $u$ of $\mathbb{N}$. Therefore $u - 1$ is not an upper bound of N, so there exists $m\in \mathbb{N}$ with $u - 1 < m$. Adding $1$ gives $u < m + 1$, and since $m + 1\in \mathbb{N}$, this inequality contradicts the fact that u is an upper bound of N.


>[!tips] The Density Theorem
>  $x,y \in \mathbb{R}$ \, $x < y$ $\implies \exists r\in \mathbb{Q} \ni x<r<y$

>[!success]- Proof
>WLOG assume $x>0$, 

>[!tips] Bernoulli's Inequality
>if $x>-1$, then $(1+x)^n\geq 1+xn$ $\forall n\in \mathbb{N}$.

>[!success]- Proof
>Induction. 
i




### Excercises

 Note: tbh there are a lot of weirdly obvious properties, only some of the interesting ones are included in the note and the rest as an excercise. 

  > [!question] Prove inf and sup $S_{4}$ 
  > Let $S_{4}={1-\frac{(-1)^{n}}{n} : n \in \mathbb{N}}.$  Find $inf \,S_{4} \,\text{and} \,sup \, S_{4}$

>[!success]- Solution
> **Claim:** $\sup(S) = 2$.   
>  We must show $s_n \le 2$ for all $n \in \mathbb{N} \text{ (i.e 2 is the upperbound of} \, S_{4})$. 
>   - If $n$ is odd, $s_n = 1 + \frac{1}{n}$. Since $n \ge 1$, then $\frac{1}{n} \le 1$, so $s_n \le 1+1=2$. 
>   - If $n$ is even, $s_n = 1 - \frac{1}{n}$. Since $n \ge 2$, then $s_n < 1 < 2$. 
>   - Thus, 2 is an upper bound for $S$. 
**We now show 2 is the least upper bound:** 
>   - For any $\epsilon > 0$, we must find an element $s_k \in S$ such that $s_k > 2 - \epsilon$. 
>   - Choose $s_k = s_1 = 2$. 
>   - The condition $2 > 2 - \epsilon$ simplifies to $\epsilon > 0$, which is true by definition. 
>   - Thus, no number smaller than 2 can be an upper bound. Since 2 is the least upper bound, $\sup(S) = 2$. 
> 
>  **Claim:** $\inf(S) = \frac{1}{2}$. 
>**1/2 is a lower bound:** 
>   - We must show $s_n \ge \frac{1}{2}$ for all $n \in \mathbb{N}$. 
>   - If $n$ is odd, $s_n = 1 + \frac{1}{n} > 1 > \frac{1}{2}$. 
>   - If $n$ is even, $s_n = 1 - \frac{1}{n}$. Since $n \ge 2$, then $\frac{1}{n} \le \frac{1}{2}$, which implies $s_n = 1 - \frac{1}{n} \ge 1 - \frac{1}{2} = \frac{1}{2}$. > Thus, 1/2 is a lower bound for $S$. 
**1/2 is the greatest lower bound:** 
>   - For any $\epsilon > 0$, we must find an element $s_k \in S$ such that $s_k < \frac{1}{2} + \epsilon$. 
>   - Choose $s_k = s_2 = \frac{1}{2}$. 
>   - The condition $\frac{1}{2} < \frac{1}{2} + \epsilon$ simplifies to $0 < \epsilon$, which is true by definition. 
>   - Thus, no number larger than 1/2 can be a lower bound. Since 1/2 is the greatest lower bound, $\inf(S) = \frac{1}{2}$.

