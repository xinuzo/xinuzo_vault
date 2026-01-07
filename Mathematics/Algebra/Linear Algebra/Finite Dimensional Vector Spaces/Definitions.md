>[!tips] 1.1 complex numbers, $\mathbb{C}$
>A complex number is an ordered pair $(𝑎,𝑏)$, where $𝑎,𝑏 ∈ \mathbb{R}$, written as $𝑎 + 𝑏𝑖$. 
>
>The set of all complex numbers is denoted by $\mathbb{C} ={𝑎+𝑏𝑖 ∶ 𝑎,𝑏 ∈ \mathbb{R}}$.
> 
> Addition and multiplication on $\mathbb{C}$ are defined by 
> $$(𝑎 +𝑏𝑖) +(𝑐 +𝑑𝑖) = (𝑎+𝑐)+(𝑏+𝑑)𝑖, (𝑎 +𝑏𝑖)(𝑐 + 𝑑𝑖) = (𝑎𝑐 −𝑏𝑑) +(𝑎𝑑+𝑏𝑐)𝑖$$
>  here $𝑎,𝑏,𝑐,𝑑 ∈ \mathbb{R}$

>[!tips] 1.3 - 1.5 addition and multiplication on $\mathbf{F}^n$
>>[!tips] 2.1 linear combination
>A **linear combination** of a list $v_1, \dots, v_m$ of vectors in $V$ is a vector of the form
>$$a_1v_1 + \dots + a_mv_m$$
>where $a_1, \dots, a_m \in \mathbf{F}$.

>[!tips] 2.3 span
>The set of all linear combinations of a list of vectors $v_1, \dots, v_m$ in $V$ is called the **span** of $v_1, \dots, v_m$, denoted $\text{span}(v_1, \dots, v_m)$.
>$$\text{span}(v_1, \dots, v_m) = \{a_1v_1 + \dots + a_mv_m : a_1, \dots, a_m \in \mathbf{F}\}$$
>The span of the empty list $()$ is defined to be $\{0\}$.

>[!tips] 2.8 finite-dimensional vector space
>A vector space $V$ is called **finite-dimensional** if there exists a list $v_1, \dots, v_m$ of vectors in $V$ such that $V = \text{span}(v_1, \dots, v_m)$.

>[!tips] 2.9 polynomial, $\mathcal{P}(\mathbf{F})$
>- A function $p: \mathbf{F} \to \mathbf{F}$ is called a **polynomial** with coefficients in $\mathbf{F}$ if there exist $a_0, \dots, a_m \in \mathbf{F}$ such that
>$$p(z) = a_0 + a_1z + \dots + a_mz^m$$
>for all $z \in \mathbf{F}$.
>- $\mathcal{P}(\mathbf{F})$ is the set of all polynomials with coefficients in $\mathbf{F}$.

>[!tips] 2.10 degree of a polynomial, $\deg p$
>- A polynomial $p \in \mathcal{P}(\mathbf{F})$ is said to have **degree** $m$ if there exist scalars $a_0, a_1, \dots, a_m \in \mathbf{F}$ with $a_m \neq 0$ such that $p(z) = a_0 + a_1z + \dots + a_mz^m$ for all $z \in \mathbf{F}$.
>- The degree of a polynomial $p$ is denoted by $\deg p$.
>- The degree of the 0 polynomial is defined to be $-\infty$.

>[!tips] 2.15 infinite-dimensional vector space
>A vector space $V$ is called **infinite-dimensional** if it is not finite-dimensional.

>[!tips] 2.17 linearly independent
>- A list $v_1, \dots, v_m$ of vectors in $V$ is called **linearly independent** if the only choice of $a_1, \dots, a_m \in \mathbf{F}$ that satisfies $a_1v_1 + \dots + a_mv_m = 0$ is $a_1 = \dots = a_m = 0$.
>- The empty list $()$ is also declared to be linearly independent.

>[!tips] 2.19 linearly dependent
>- A list of vectors in $V$ is called **linearly dependent** if it is not linearly independent.
>- In other words, a list $v_1, \dots, v_m$ of vectors in $V$ is linearly dependent if there exist $a_1, \dots, a_m \in \mathbf{F}$, not all 0, such that $a_1v_1 + \dots + a_mv_m = 0$.

>[!tips] 2.26 basis
>A **basis** of $V$ is a list of vectors in $V$ that is linearly independent and spans $V$.

>[!tips] 2.34 dimension, $\dim V$
>- The **dimension** of a finite-dimensional vector space $V$ is the length of any basis of the list of vectors in $V$.
>- The dimension of $V$ (if $V$ is finite-dimensional) is denoted by $\dim V$.- **list**: A list of length $n$ is an ordered collection of $n$ elements (which might be numbers, other lists, or more abstract entities) separated by commas and surrounded by parentheses.
>- **coordinate**: For a list $(x_1, \dots, x_n)$ and $j \in \{1, \dots, n\}$, the $j^{\text{th}}$ coordinate is the element $x_j$.
>- **$\mathbf{F}^n$**: $\mathbf{F}^n$ is the set of all lists of length $n$ of elements of $\mathbf{F}$.
>$$\mathbf{F}^n = \{(x_1, \dots, x_n) : x_j \in \mathbf{F} \text{ for } j = 1, \dots, n\}$$
>- **addition in $\mathbf{F}^n$**: Addition in $\mathbf{F}^n$ is defined by adding corresponding coordinates:
>$$(x_1, \dots, x_n) + (y_1, \dots, y_n) = (x_1+y_1, \dots, x_n+y_n)$$
>- **scalar multiplication in $\mathbf{F}^n$**: The product of a number $\lambda$ and a vector in $\mathbf{F}^n$ is computed by multiplying each coordinate of the vector by $\lambda$:
>$$\lambda(x_1, \dots, x_n) = (\lambda x_1, \dots, \lambda x_n)$$

>[!tips] 1.8 vector space
>A **vector space** is a set $V$ along with an addition on $V$ and a scalar multiplication on $V$ such that the following properties hold:
>- **commutativity**: $u+v = v+u$ for all $u, v \in V$.
>- **associativity**: $(u+v)+w = u+(v+w)$ and $(ab)v = a(bv)$ for all $u, v, w \in V$ and all $a, b \in \mathbf{F}$.
>- **additive identity**: There exists an element $0 \in V$ such that $v+0 = v$ for all $v \in V$.
>- **additive inverse**: For every $v \in V$, there exists $w \in V$ such that $v+w = 0$.
>- **multiplicative identity**: $1v = v$ for all $v \in V$.
>- **distributive properties**: $a(u+v) = au + av$ and $(a+b)v = av + bv$ for all $a, b \in \mathbf{F}$ and all $u, v \in V$.

>[!tips] 1.11 vector, point
>Elements of a vector space are called **vectors** or **points**.

>[!tips] 1.12 real vector space, complex vector space
>- A vector space over $\mathbf{R}$ is called a **real vector space**.
>- A vector space over $\mathbf{C}$ is called a **complex vector space**.

>[!tips] 1.18 subspace
>A subset $U$ of $V$ is called a **subspace** of $V$ if $U$ is also a vector space with the same additive identity, addition, and scalar multiplication as on $V$.

>[!tips] 1.22 sum of subsets
>Suppose $U_1, \dots, U_m$ are subsets of $V$. The **sum** of $U_1, \dots, U_m$, denoted $U_1 + \dots + U_m$, is the set of all possible sums of elements of $U_1, \dots, U_m$. More precisely,
>$$U_1 + \dots + U_m = \{u_1 + \dots + u_m : u_1 \in U_1, \dots, u_m \in U_m\}$$

>[!tips] 1.25 direct sum
>Suppose $U_1, \dots, U_m$ are subspaces of $V$.
>- The sum $U_1 + \dots + U_m$ is called a **direct sum** if each element of $U_1 + \dots + U_m$ can be written in only one way as a sum $u_1 + \dots + u_m$, where each $u_j \in U_j$.
>- If the sum $U_1 + \dots + U_m$ is a direct sum, it is denoted by $U_1 \oplus \dots \oplus U_m$.