>[!tips] Definition 2.1.1 (Random Vector). 
>Given a random experiment with a sample space $C$, consider two random variables $X_{1}$ and $X_{2}$, which assign to each element $c$ of $C$ **one and only one** ordered pair of numbers $X_{1}(c) = x_{1}$ , $X_{2}(c) = x_{2}$. Then  $(X_{1}, X_{2})$ is a random vector. The space of $(X{1}, X_{2})$ is the set of ordered pairs $D = {(x1, x2) : x_{1} = X_{1}(c), x_{2} = X_{2}(c), c ∈ C}$.

>[!tips] Properties 1 
>$P[a_{1}<X_{1}<b_{1} , a_{2}<X_{2}<b_{2}]=F_{x_{1},x_{2}}(b_{1},b_{2})-F_{x_{1},x_{2}}(a_{1},b_{2})-F_{x_{1},x_{2}}(b_{1},a_{2})+F_{x_{1},x_{2}}(a_{1},a_{2})$

Theorem2.3.1. Let(X1,X2)bearandomvectorsuchthat thevarianceofX2 is finite.Then, (a)E[E(X2|X1)]=E(X2). (b)Var[E(X2|X1)]≤Var(X2)