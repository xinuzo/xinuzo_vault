>[!tips] 2.1 linear combination
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
>- The dimension of $V$ (if $V$ is finite-dimensional) is denoted by $\dim V$.