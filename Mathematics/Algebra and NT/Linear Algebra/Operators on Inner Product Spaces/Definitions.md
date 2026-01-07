>[!tips] 7.2 adjoint, $T^*$
>Suppose $T \in \mathcal{L}(V, W)$. The **adjoint** of $T$ is the function $T^*: W \to V$ such that
>$$\langle Tv, w \rangle = \langle v, T^*w \rangle$$
>for every $v \in V$ and every $w \in W$.

>[!tips] 7.11 self-adjoint
>An operator $T \in \mathcal{L}(V)$ is called **self-adjoint** if $T = T^*$.

>[!tips] 7.18 normal
>An operator on an inner product space is called **normal** if it commutes with its adjoint; that is, $T$ is normal if $TT^* = T^*T$.

>[!tips] 7.31 positive operator
>An operator $T \in \mathcal{L}(V)$ is called **positive** if $T$ is self-adjoint and
>$$\langle Tv, v \rangle \ge 0$$
>for all $v \in V$.

>[!tips] 7.33 square root, $\sqrt{T}$
>An operator $R$ is called a **square root** of an operator $T$ if $R^2 = T$.

>[!tips] 7.37 isometry
>An operator $S \in \mathcal{L}(V)$ is called an **isometry** if $\|Sv\| = \|v\|$ for every $v \in V$.

>[!tips] 7.49 singular values
>Suppose $T \in \mathcal{L}(V)$. The **singular values** of $T$ are the eigenvalues of $\sqrt{T^*T}$, with each eigenvalue $\lambda$ repeated $\dim E(\lambda, \sqrt{T^*T})$ times.