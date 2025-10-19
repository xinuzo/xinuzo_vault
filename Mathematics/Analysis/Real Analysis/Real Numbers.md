
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
  $$
  $$
\begin{align}
a\in P      a=0       -a\in P
\end{align}
$$


>[!tips] Completeness  Axiom of $\mathbb{R}$
>Every nonempty set of **real numbers** that is **bounded above (below)** has a **least upper (greatest lower)** bound in $\mathbb{R}$.

>[!tips] Bernoulli's Inequality
>if $x>-1$, then $(1+x)^n\geq 1+xn$ $\forall n\in \mathbb{N}$.

>[!success]- Proof
>Induction. 
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

