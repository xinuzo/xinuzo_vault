
## Definitions and Theorems
![[Pasted image 20250930131038.png]]
source: MathPi/Youtube
## Excercises

>[!question] 28 Herstein Abstract Algebra 3rd Edition
>Let $G$ be a set with a binary operation $*$ that satisfies the following four axioms:
>1. **Closure:** For all $a, b \in G$, the element $a * b$ is in $G$.
>2. **Associativity:** For all $a, b, c \in G$, we have $(a * b) * c = a * (b * c)$.
>3. **Existence of a Left Identity:** There exists an element $e \in G$ such that for all $x \in G$, we have $e * x = x$.
>4. **Existence of a Left Inverse:** For each $x \in G$, there exists an element $y \in G$ such that $y * x = e$.
>
>Then, $G$ is a group. Specifically, we must prove that the left identity is also a right identity ($x*e=x$) and that every left inverse is also a right inverse ($x*y=e$).

>[!success]- Proof
>The proof consists of two parts. First, we show that a left inverse is also a right inverse. Second, we use this fact to show that the left identity is also a right identity.
>
>---
>
>**Part 1: Proving the Right Inverse Property ($x * y = e$)**
>
>Let $x$ be an arbitrary element in $G$. By Axiom 4, there exists a left inverse $y \in G$ such that $y * x = e$. Our goal is to show that this also implies $x * y = e$.
>
>Since $y$ is an element of $G$, it must also have its own left inverse. Let's call this element $z \in G$, such that $z * y = e$.
>
>Now, we will manipulate the expression $x * y$ using only the given axioms:
>
>$$
>\begin{align*}
>x * y &= e * (x * y) && \text{(by Axiom 3, Left Identity)} \\
>      &= (z * y) * (x * y) && \text{(substituting } e = z * y \text{)} \\
>      &= z * (y * (x * y)) && \text{(by Axiom 2, Associativity)} \\
>      &= z * ((y * x) * y) && \text{(by Axiom 2, Associativity)} \\
>      &= z * (e * y) && \text{(substituting } y * x = e \text{)} \\
>      &= z * y && \text{(by Axiom 3, Left Identity)} \\
>      &= e && \text{(by the definition of } z \text{)}
>\end{align*}
>$$
>
>We have successfully shown that $x * y = e$. Thus, the left inverse of any element is also its right inverse.
>
>---
>
>**Part 2: Proving the Right Identity Property ($x * e = x$)**
>
>Now we can use the result from Part 1. Let $x$ be an arbitrary element in $G$.
>
>By Axiom 4, there exists a left inverse $y$ such that $y * x = e$. From Part 1, we now know that this also means $x * y = e$.
>
>We will manipulate the expression $x * e$:
>
>$$
>\begin{align*}
>x * e &= x * (y * x) && \text{(substituting } e = y * x \text{)} \\
>      &= (x * y) * x && \text{(by Axiom 2, Associativity)} \\
>      &= e * x && \text{(substituting } x * y = e \text{, from Part 1)} \\
>      &= x && \text{(by Axiom 3, Left Identity)}
>\end{align*}
>$$
>
>We have successfully shown that $x * e = x$. Thus, the left identity is also the right identity.
>
>---
>
>**Conclusion**
>Since we have proven the existence of a two-sided identity element and a two-sided inverse for every element, in addition to closure and associativity, the set $G$ with the operation $*$ satisfies all the axioms of a group.