# Lecture Notes: Introduction to Linear Programming

---
## Chapter 1: Introduction

>[!info]- (Definition) Linear Programming (LP) Problem
>A Linear Programming (LP) problem is the task of optimizing (maximizing or minimizing) a linear **objective function** subject to a set of linear **constraints** (inequalities or equalities) and **non-negativity constraints** on the decision variables.
>
>The general form is:
>$$
>\begin{align*}
>\text{Maximize } \quad & \mathbf{c}^T \mathbf{x} \\
>\text{Subject to } \quad & A \mathbf{x} \le \mathbf{b} \\
> & \mathbf{x} \ge \mathbf{0}
>\end{align*}
>$$

>[!info]- (Definition) Standard Form
>An LP problem is in **Standard Form** if:
>1. The objective is a maximization.
>2. All constraints are equalities (except for non-negativity).
>3. The right-hand side vector $\mathbf{b}$ is non-negative.
>4. All variables are non-negative.
>
>We convert inequalities to equalities by adding **slack variables** (for $\le$ constraints) or subtracting **surplus variables** (for $\ge$ constraints).

---
## Chapter 2: Geometry of Linear Programming

>[!info]- (Definition) Convex Set
>A set $S$ is **convex** if for any two points $\mathbf{x}_1, \mathbf{x}_2 \in S$, the entire line segment connecting them is also in $S$. The feasible region of an LP problem is always a convex set.
>

>[!info]- (Definition) Extreme Point
>An **extreme point** (or vertex) of a convex set is a point that cannot be represented as a convex combination of two other distinct points in the set. In 2D, these are the corners of the feasible region.

>[!tips]- (Theorem) Fundamental Theorem of Linear Programming
>If an optimal solution to a Linear Programming problem exists, then at least one **extreme point** of the feasible region must be optimal.
>
>This theorem is the foundation of the Simplex method, which works by moving from one extreme point to an adjacent one, improving the objective function at each step, until an optimal solution is found.

---
## Chapter 3: The Simplex Method

>[!info]- (Definition) Basic Feasible Solution (BFS)
>A **Basic Feasible Solution** is the algebraic representation of an extreme point. It is a basic solution (obtained by setting $n-m$ variables to zero and solving for the remaining $m$ variables, where $n$ is the number of variables and $m$ is the number of constraints) that also satisfies all non-negativity constraints.

>[!tips]- (Theorem) Simplex Optimality Condition
>For a maximization problem in the Simplex tableau, the current Basic Feasible Solution is **optimal** if and only if all coefficients in the objective function row (row 0, or the $z$-row) are non-negative.

---
## Exercises

>[!question]- (Exercise) Solve with the Simplex Method
>Use the Simplex method to solve the following LP problem:
>$$
>\begin{align*}
>\text{Maximize } \quad Z &= 3x_1 + 5x_2 \\
>\text{Subject to } \quad x_1 &\le 4 \\
> 2x_2 &\le 12 \\
> 3x_1 + 2x_2 &\le 18 \\
> x_1, x_2 &\ge 0
>\end{align*}
>$$

>[!success]- Solution
>
>**Step 1: Convert to Standard Form**
>We introduce slack variables $s_1, s_2, s_3$ to convert the inequalities into equalities. The objective function is rewritten as $Z - 3x_1 - 5x_2 = 0$.
>$$
>\begin{align*}
>Z - 3x_1 - 5x_2 &= 0 \\
>x_1 + s_1 &= 4 \\
>2x_2 + s_2 &= 12 \\
>3x_1 + 2x_2 + s_3 &= 18
>\end{align*}
>$$
>
>**Step 2: Initial Simplex Tableau**
>The initial Basic Feasible Solution is $(x_1, x_2, s_1, s_2, s_3) = (0, 0, 4, 12, 18)$ with $Z=0$.
>
>| Basis | Z | x1 | x2 | s1 | s2 | s3 | RHS | Ratio |
>| :---: |:-:|:--:|:--:|:--:|:--:|:--:|:---:|:---:|
>| Z | 1 |-3 |-5 | 0 | 0 | 0 | 0 | |
>| s1 | 0 | 1 | 0 | 1 | 0 | 0 | 4 | - |
>| s2 | 0 | 0 | 2 | 0 | 1 | 0 | 12 | 12/2=6 |
>| s3 | 0 | 3 | 2 | 0 | 0 | 1 | 18 | 18/2=9 |
>
>**Iteration 1**
>- **Theory:** The optimality condition is not met because the $Z$-row has negative coefficients. We choose the most negative one to determine the entering variable.
>- **Entering Variable:** $x_2$ (column with -5).
>- **Leaving Variable:** Perform the ratio test: $\min(12/2, 18/2) = \min(6, 9) = 6$. The minimum ratio corresponds to the row of $s_2$. So, $s_2$ leaves the basis.
>- **Pivot Element:** The element at the intersection of the pivot column ($x_2$) and pivot row ($s_2$) is **2**.
>- **Row Operations:**
>  1. New R3 (pivot row): R3 / 2
>  2. New R1: R1 + 5 * (New R3)
>  3. New R2: R2 (no change needed)
>  4. New R4: R4 - 2 * (New R3)
>
>**Tableau after Iteration 1**
>The BFS is $(x_1, x_2, s_1, s_2, s_3) = (0, 6, 4, 0, 6)$ with $Z=30$.
>
>| Basis | Z | x1 | x2 | s1 | s2 | s3 | RHS | Ratio |
>| :---: |:-:|:--:|:--:|:--:|:---:|:--:|:---:|:---:|
>| Z | 1 |-3 | 0 | 0 | 5/2 | 0 | 30 | |
>| s1 | 0 | 1 | 0 | 1 | 0 | 0 | 4 | 4/1=4 |
>| x2 | 0 | 0 | 1 | 0 | 1/2 | 0 | 6 | - |
>| s3 | 0 | 3 | 0 | 0 |-1 | 1 | 6 | 6/3=2 |
>
>**Iteration 2**
>- **Theory:** The optimality condition is still not met (coefficient of $x_1$ is -3).
>- **Entering Variable:** $x_1$.
>- **Leaving Variable:** Ratio test: $\min(4/1, 6/3) = \min(4, 2) = 2$. The minimum ratio corresponds to the row of $s_3$. So, $s_3$ leaves.
>- **Pivot Element:** The element at the intersection of column $x_1$ and row $s_3$ is **3**.
>- **Row Operations:**
>  1. New R4 (pivot row): R4 / 3
>  2. New R1: R1 + 3 * (New R4)
>  3. New R2: R2 - 1 * (New R4)
>  4. New R3: R3 (no change needed)
>
>**Final Tableau**
>
>| Basis | Z | x1 | x2 | s1 | s2 | s3 | RHS |
>| :---: |:-:|:--:|:--:|:--:|:---:|:---:|:---:|
>| Z | 1 | 0 | 0 | 0 | 3/2 | 1 | 36 |
>| s1 | 0 | 0 | 0 | 1 | 1/3 |-1/3| 2 |
>| x2 | 0 | 0 | 1 | 0 | 1/2 | 0 | 6 |
>| x1 | 0 | 1 | 0 | 0 |-1/3| 1/3 | 2 |
>
>**Conclusion**
>- **Theory:** The optimality condition is now met, as all coefficients in the $Z$-row are non-negative.
>- **Optimal Solution:** We read the values from the `RHS` column for the variables in the `Basis` column.
>  - $x_1 = 2$
>  - $x_2 = 6$
>  - $s_1 = 2$ (meaning the first constraint has 2 units of slack)
>- **Optimal Value:** The optimal value of the objective function is found in the `RHS` of the $Z$-row.
>  - **Z = 36**