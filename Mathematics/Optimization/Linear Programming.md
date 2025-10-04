
## Chapter 1: Introduction

>[!info]- (Definition) Linear Programming (LP) Problem
>A Linear Programming (LP) problem is the task of optimizing (maximizing or minimizing) a linear **objective function** subject to a set of linear **constraints** (inequalities or equalities) and **non-negativity constraints** on the decision variables.

>[!info]- (Definition) Standard Form (Bazaraa's Convention)
>An LP problem is in **Standard Form** if:
>1. The objective is a **minimization**.
>2. All constraints are **equalities**.
>3. The right-hand side vector $\mathbf{b}$ is non-negative.
>4. All variables are non-negative.
>
>We convert inequalities to equalities by adding **slack variables** (for $\le$ constraints) or subtracting **surplus variables** (for $\ge$ constraints). A maximization objective `max Z` can be converted to minimization by `min (-Z)`.

---
## Chapter 2: Geometry of Linear Programming

>[!info]- (Definition) Convex Set
>A set $S$ is **convex** if for any two points $\mathbf{x}_1, \mathbf{x}_2 \in S$, the entire line segment connecting them is also in $S$. The feasible region of an LP problem is always a convex set (a polytope).
>

>[!info]- (Definition) Extreme Point
>An **extreme point** (or vertex) of a convex set is a point that cannot be represented as a convex combination of two other distinct points in the set. In 2D, these are the corners of the feasible region.

>[!tips]- (Theorem) Equivalence of Extreme Points and BFS
>A point $\mathbf{x}$ is an **extreme point** of the feasible region $S = \{\mathbf{x} \in \mathbb{R}^n \mid A\mathbf{x} = \mathbf{b}, \mathbf{x} \ge \mathbf{0}\}$ if and only if $\mathbf{x}$ is a **Basic Feasible Solution (BFS)**.

>[!success]- Proof Outline
>This proof shows the connection between the geometry (corners) and the algebra (basic solutions).
>
>**($\Rightarrow$) If $\mathbf{x}$ is a BFS, then it is an extreme point.**
>1. Let $\mathbf{x}$ be a BFS. By definition, its positive components correspond to linearly independent columns of $A$. Let these columns be $A_1, \dots, A_m$.
>2. Assume, for contradiction, that $\mathbf{x}$ is *not* an extreme point. This means $\mathbf{x}$ can be written as a convex combination of two other distinct points $\mathbf{y}, \mathbf{z} \in S$: $\mathbf{x} = \lambda \mathbf{y} + (1-\lambda)\mathbf{z}$ for $0 < \lambda < 1$.
>3. Because all components of $\mathbf{x}, \mathbf{y}, \mathbf{z}$ are non-negative, if a component $x_j=0$, then the corresponding components $y_j$ and $z_j$ must also be zero.
>4. This implies that $\mathbf{y}$ and $\mathbf{z}$ also have at most $m$ non-zero components, corresponding to the same columns $A_1, \dots, A_m$.
>5. Therefore, $A\mathbf{y} = \sum_{j=1}^m y_j A_j = \mathbf{b}$ and $A\mathbf{z} = \sum_{j=1}^m z_j A_j = \mathbf{b}$.
>6. Subtracting these gives $\sum_{j=1}^m (y_j - z_j) A_j = \mathbf{0}$. Since the columns $A_j$ are linearly independent, this forces $y_j - z_j = 0$ for all $j$. Thus, $\mathbf{y} = \mathbf{z}$.
>7. This is a contradiction, as we assumed $\mathbf{y}$ and $\mathbf{z}$ were distinct. Therefore, $\mathbf{x}$ must be an extreme point.
>
>**($\Leftarrow$) If $\mathbf{x}$ is an extreme point, then it is a BFS.**
>8. Let $\mathbf{x}$ be an extreme point. Assume it has $k$ positive components. We want to show the corresponding columns of $A$ are linearly independent.
>9. Assume, for contradiction, that these columns are linearly dependent. This means there exists a non-zero vector $\mathbf{d}$ such that $A\mathbf{d} = \mathbf{0}$, where the non-zero components of $\mathbf{d}$ correspond to the positive components of $\mathbf{x}$.
>10. We can then construct two new points: $\mathbf{y} = \mathbf{x} + \epsilon \mathbf{d}$ and $\mathbf{z} = \mathbf{x} - \epsilon \mathbf{d}$ for some small $\epsilon > 0$.
>11. For a small enough $\epsilon$, both $\mathbf{y}$ and $\mathbf{z}$ are feasible (non-negative and satisfy $A\mathbf{y}=A\mathbf{x}+\epsilon A\mathbf{d} = \mathbf{b}+\mathbf{0}=\mathbf{b}$).
>12. We can write $\mathbf{x} = \frac{1}{2}\mathbf{y} + \frac{1}{2}\mathbf{z}$. This expresses $\mathbf{x}$ as a convex combination of two other distinct points in the feasible set.
>13. This contradicts the definition of an extreme point. Therefore, the columns corresponding to the positive components of $\mathbf{x}$ must be linearly independent, which means $\mathbf{x}$ is a BFS.

>[!tips]- (Theorem) Existence of an Optimal BFS
>If an LP problem has an optimal solution, then at least one **Basic Feasible Solution (BFS)** must be optimal.

>[!success]- Proof Outline
>14. Let $\mathbf{x}^*$ be an optimal solution. If $\mathbf{x}^*$ is an extreme point, then by the previous theorem it's a BFS and we are done.
>15. Assume $\mathbf{x}^*$ is *not* an extreme point. This means it lies in the interior of a line segment within the feasible region, so $\mathbf{x}^* = \lambda \mathbf{y} + (1-\lambda)\mathbf{z}$ for distinct feasible $\mathbf{y}, \mathbf{z}$.
>16. The objective value at $\mathbf{x}^*$ is $\mathbf{c}^T\mathbf{x}^* = \lambda (\mathbf{c}^T\mathbf{y}) + (1-\lambda)(\mathbf{c}^T\mathbf{z})$.
>17. Since $\mathbf{x}^*$ is optimal, its objective value must be greater than or equal to any other feasible point. So, $\mathbf{c}^T\mathbf{x}^* \ge \mathbf{c}^T\mathbf{y}$ and $\mathbf{c}^T\mathbf{x}^* \ge \mathbf{c}^T\mathbf{z}$.
>18. For the convex combination to hold, this implies that in fact $\mathbf{c}^T\mathbf{x}^* = \mathbf{c}^T\mathbf{y} = \mathbf{c}^T\mathbf{z}$. The objective function is constant along the entire line segment.
>19. This means we can "slide" our solution from $\mathbf{x}^*$ towards an extreme point (like $\mathbf{y}$ or $\mathbf{z}$) without making the solution worse. By repeating this process, we must eventually reach an extreme point that has an objective value at least as good as our starting point. Since our starting point was optimal, that extreme point must also be optimal.

>[!tips]- (Theorem) Improvement of a Basic Solution
>Given a non-optimal Basic Feasible Solution, the Simplex method moves to an adjacent BFS with an improved (or equal) objective value. The change in the objective function value when moving from one basis to another is given by the coefficient in the objective row of the entering variable.

>[!success]- Proof Outline
>20. In the Simplex tableau, the objective row represents the objective function $Z$ in terms of the non-basic variables. For a maximization problem, it's written as $Z + \sum_{j \in N} (c_j' - z_j')x_j = Z_0$, where $N$ is the set of non-basic variables and $(c_j' - z_j')$ are the reduced costs in the objective row. This is usually written as $Z = Z_0 - \sum (c_j' - z_j')x_j$.
>21. The current BFS has all non-basic variables $x_j=0$, so $Z = Z_0$.
>22. The **Optimality Condition** states that if all $(c_j' - z_j') \ge 0$, then any increase in a non-basic $x_j$ (which must be positive) would cause $Z$ to decrease (or stay the same). Thus, the current solution is optimal.
>23. If there is a non-basic variable $x_k$ with a negative coefficient, say $(c_k' - z_k') < 0$, then the objective function is $Z = Z_0 - (c_k' - z_k')x_k + \dots$.
>24. Since $(c_k' - z_k')$ is negative, increasing $x_k$ from 0 will **increase** the value of $Z$.
>25. The Simplex pivot operation does exactly this: it increases the chosen non-basic variable $x_k$ (the entering variable) as much as possible until one of the current basic variables becomes zero (the leaving variable). This corresponds to moving to an adjacent extreme point along an edge of the feasible region, and the proof shows that this move increases the objective value.

```tikz
\begin{tikzpicture}[scale=0.8]
    % Define the axes
    \draw[->] (0,0) -- (7,0) node[right] {$x_1$};
    \draw[->] (0,0) -- (0,8) node[above] {$x_2$};
    
    % Draw the constraints
    \draw[thick, blue] (4,0) -- (4,3) node[above left, black] {$x_1 \le 4$};
    \draw[thick, blue] (0,6) -- (4,6) node[above, black] {$2x_2 \le 12$};
    \draw[thick, blue] (6,0) -- (0,9) node[above, black] {$3x_1 + 2x_2 \le 18$};
    
    % Fill the feasible region
    \fill[yellow, opacity=0.3] (0,0) -- (4,0) -- (4,3) -- (2,6) -- (0,6) -- cycle;
    
    % Mark the extreme points (BFS)
    \node[circle, fill=red, inner sep=2pt, label=below:A(0,0)] (A) at (0,0) {};
    \node[circle, fill=red, inner sep=2pt, label=below:B(4,0)] (B) at (4,0) {};
    \node[circle, fill=red, inner sep=2pt, label=right:C(4,3)] (C) at (4,3) {};
    \node[circle, fill=red, inner sep=2pt, label=above:D(2,6)] (D) at (2,6) {};
    \node[circle, fill=red, inner sep=2pt, label=left:E(0,6)] (E) at (0,6) {};
    
    % Draw the path of the Simplex algorithm from the exercise
    \draw[->, ultra thick, red] (A) -- (E) node[midway, below left] {Iter 1};
    \draw[->, ultra thick, red] (E) -- (D) node[midway, above] {Iter 2};
    
    % Highlight the optimal point
    \node[star, star points=7, fill=green, inner sep=3pt, label=above
    right:\textbf{Optimal!}] at (D) {};
    \end{tikzpicture}
```
```tikz
```

>[!tips]- (Theorem) Fundamental Theorem of Linear Programming
>If an optimal solution to a Linear Programming problem exists, then at least one **extreme point** of the feasible region must be optimal.
>
>This theorem is the foundation of the Simplex method, which works by moving from one extreme point (BFS) to an adjacent one, improving the objective function at each step, until an optimal solution is found.

---
## Chapter 3: The Simplex Method

>[!info]- (Definition) Basic Feasible Solution (BFS)
>A **Basic Feasible Solution** is the algebraic representation of an extreme point. It is a basic solution (obtained by setting $n-m$ variables to zero and solving for the remaining $m$ variables) that also satisfies all non-negativity constraints.

>[!tips]- (Theorem) Simplex Optimality Condition (for Minimization)
>For a **minimization** problem in the Simplex tableau, the current Basic Feasible Solution is **optimal** if and only if all coefficients in the objective function row (row 0, or the $z$-row) are **non-positive** ($\le 0$)

---

## Exercises

>[!question]- (Exercise) Solve with the Simplex Method
>Let's solve the previous problem, but framed as a minimization problem.
>Original Problem: Maximize $Z = 3x_1 + 5x_2$.
>This is equivalent to **Minimizing $W = -3x_1 - 5x_2$**.
>
>The problem is:
>$$
>\begin{align*}
>\text{Minimize } \quad W &= -3x_1 - 5x_2 \\
>\text{Subject to } \quad x_1 &\le 4 \\
> 2x_2 &\le 12 \\
> 3x_1 + 2x_2 &\le 18 \\
> x_1, x_2 &\ge 0
>\end{align*}
>$$

>[!success]- Solution
>
>**Step 1: Convert to Standard Form**
>We add slack variables $s_1, s_2, s_3$ and rewrite the objective function as $W + 3x_1 + 5x_2 = 0$.
>$$
>\begin{align*}
>W + 3x_1 + 5x_2 &= 0 \\
>x_1 + s_1 &= 4 \\
>2x_2 + s_2 &= 12 \\
>3x_1 + 2x_2 + s_3 &= 18
>\end{align*}
>$$
>
>**Step 2: Initial Simplex Tableau**
>The initial BFS is $(x_1, x_2, s_1, s_2, s_3) = (0, 0, 4, 12, 18)$ with $W=0$.
>
>| Basis | W | x1 | x2 | s1 | s2 | s3 | RHS | Ratio |
>| :---: |:-:|:--:|:--:|:--:|:--:|:--:|:---:|:---:|
>| W | 1 | 3 | **5** | 0 | 0 | 0 | 0 | |
>| s1 | 0 | 1 | 0 | 1 | 0 | 0 | 4 | - |
>| s2 | 0 | 0 | **2** | 0 | 1 | 0 | 12 | 12/2=6 |
>| s3 | 0 | 3 | 2 | 0 | 0 | 1 | 18 | 18/2=9 |
>
>**Iteration 1**
>- **Theory:** The optimality condition is not met because the $W$-row has positive coefficients (3 and 5). For minimization, we choose the **most positive** coefficient to determine the entering variable.
>- **Entering Variable:** $x_2$ (column with 5).
>- **Leaving Variable:** Ratio test: $\min(12/2, 18/2) = 6$. The minimum ratio is in the row of $s_2$. So, $s_2$ leaves.
>- **Pivot Element:** 2.
>- **Row Operations:**
>  1. New R3 (pivot row): R3 / 2
>  2. New R1: R1 - 5 * (New R3)
>  3. New R4: R4 - 2 * (New R3)
>
>**Tableau after Iteration 1**
>BFS is $(0, 6, 4, 0, 6)$ with $W=-30$.
>
>| Basis | W | x1 | x2 | s1 | s2 | s3 | RHS | Ratio |
>| :---: |:-:|:--:|:--:|:--:|:---:|:--:|:---:|:---:|
>| W | 1 | **3** | 0 | 0 | -5/2 | 0 | -30 | |
>| s1 | 0 | 1 | 0 | 1 | 0 | 0 | 4 | 4/1=4 |
>| x2 | 0 | 0 | 1 | 0 | 1/2 | 0 | 6 | - |
>| s3 | 0 | **3** | 0 | 0 | -1 | 1 | 6 | 6/3=2 |
>
>**Iteration 2**
>- **Theory:** Still not optimal (coefficient of $x_1$ is 3).
>- **Entering Variable:** $x_1$.
>- **Leaving Variable:** Ratio test: $\min(4/1, 6/3) = 2$. The minimum ratio is in the row of $s_3$. So, $s_3$ leaves.
>- **Pivot Element:** 3.
>- **Row Operations:**
>  1. New R4 (pivot row): R4 / 3
>  2. New R1: R1 - 3 * (New R4)
>  3. New R2: R2 - 1 * (New R4)
>
>**Final Tableau**
>
>| Basis | W | x1 | x2 | s1 | s2 | s3 | RHS |
>| :---: |:-:|:--:|:--:|:--:|:---:|:---:|:---:|
>| W | 1 | 0 | 0 | 0 | -3/2 | -1 | -36 |
>| s1 | 0 | 0 | 0 | 1 | 1/3 |-1/3| 2 |
>| x2 | 0 | 0 | 1 | 0 | 1/2 | 0 | 6 |
>| x1 | 0 | 1 | 0 | 0 |-1/3| 1/3 | 2 |
>
>**Conclusion**
>- **Theory:** The optimality condition is now met, as all coefficients in the $W$-row for the non-basic variables ($s_2, s_3$) are negative.
>- **Optimal Solution:**
>  - $x_1 = 2$
>  - $x_2 = 6$
>- **Optimal Value:** The optimal value for the minimization problem is $W = -36$.
>  - Since our original problem was to Maximize $Z = -W$, the maximum value is **Z = 36**.