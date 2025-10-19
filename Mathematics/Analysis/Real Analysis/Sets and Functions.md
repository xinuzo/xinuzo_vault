Bartle 4th Edition
##   Sets
### Basic Concepts

A **set** is a collection of distinct objects, considered as an object in its own right. The objects in the set are called **elements** or **members**.

- **Notation**: We write $x \in A$ to denote that $x$ is an element of set $A$.
- **Subset**: $A \subseteq B$ if every element of $A$ is also an element of $B$.
- **Proper Subset**: $A \subset B$ if $A \subseteq B$ and $A \neq B$.
- **Power Set**: The power set $\mathcal{P}(A)$ of a set $A$ is the set of all subsets of $A$. If $|A| = n$, then $|\mathcal{P}(A)| = 2^n$.

---

### Set Operations

Let $A$ and $B$ be subsets of a universal set $U$.

- **Union**: $A \cup B = \{x \mid x \in A \text{ or } x \in B\}$.
- **Intersection**: $A \cap B = \{x \mid x \in A \text{ and } x \in B\}$.
- **Complement**: $A^c = \{x \in U \mid x \notin A\}$.
- **Difference**: $A \setminus B = A \cap B^c = \{x \mid x \in A \text{ and } x \notin B\}$.

---

### Key Theorems on Set Operations

> [!tip] Theorem: De Morgan's Laws
> For any two sets $A$ and $B$:
> 1. $(A \cup B)^c = A^c \cap B^c$
> 2. $(A \cap B)^c = A^c \cup B^c$
> *In words: The complement of the union is the intersection of the complements, and the complement of the intersection is the union of the complements.*

> [!tip] Theorem: Distributive Laws
> For any three sets $A$, $B$, and $C$:
> 1. $A \cap (B \cup C) = (A \cap B) \cup (A \cap C)$
> 2. $A \cup (B \cap C) = (A \cup B) \cap (A \cup C)$

---

### Cardinality of Sets

**Cardinality** refers to the number of elements in a set, denoted $|A|$.

- **Finite Set**: A set with a finite number of elements.
- **Infinite Set**: A set that is not finite.
- **Countably Infinite**: An infinite set that can be put into a one-to-one correspondence with the set of natural numbers $\mathbb{N}$. Examples: $\mathbb{N}, \mathbb{Z}, \mathbb{Q}$.
- **Uncountable**: An infinite set that cannot be put into a one-to-one correspondence with $\mathbb{N}$. Examples: $\mathbb{R}, \mathcal{P}(\mathbb{N})$.

> [!tip] Theorem: Cantor's Theorem
> For any set $A$, the cardinality of its power set $\mathcal{P}(A)$ is strictly greater than the cardinality of $A$ itself.
> $$ |A| < |\mathcal{P}(A)| $$
> *This implies that there is no "largest" infinity.*

>[!tips] 1.2.1 Well-Ordering Property of N
> Every nonempty subset (I{N has a least element. A more detailed statement of this property is as follows: If Sis a subset of N and if S =1- 0, then there exists m E S such that m -:::: k for all k E S. On the basis of the Well-Ordering Property, we shall derive a version of the Principle of Mathematical Induction that is expressed in terms of subsets of N. 

1.2.2 Principle of Mathematical Induction 
Let S be a subset of N that possesses the two properties: (1) The number I E S. (2) For every k E N, if k E S, then k + I E S. Then we have S = N.

Proof. Suppose to the contrary that S =1- N. Then the set N\S is not empty, so by the Well Ordering Principle it has a least element m. Since I E S by hypothesis (I), we know that m > 1. But this implies that m - 1 is also a natural number. Since m - I < m and since m is the least element in N such that m ¢:. S, we conclude that m - I E S. We now apply hypothesis (2) to the element k := m - I in S, to infer that k + I = ( m - 1) + 1 = m belongs to S. But this statement contradicts the fact that m ¢:. S. Since m was obtained from the assumption that N\S is not empty, we have obtained a contradiction. Therefore we must have S = N.
##   Functions

### Definition and Properties

A **function** $f$ from a set $A$ to a set $B$, denoted $f: A \to B$, is a rule that assigns to **each** element $x \in A$ exactly **one** element $y \in B$.

- **Domain**: The set $A$ of all possible inputs.
- **Codomain**: The set $B$ of all possible outputs.
- **Image (or Range)**: The set of all actual outputs of the function, denoted $f(A) = \{f(x) \mid x \in A\}$. Note that $f(A) \subseteq B$.

---

### Types of Functions

Let $f: A \to B$ be a function.

1.  **Injective (One-to-One)**: $f$ is injective if distinct inputs have distinct outputs.
    $$ \forall x_1, x_2 \in A, \quad f(x_1) = f(x_2) \implies x_1 = x_2 $$
    *Think of the "horizontal line test" on a graph.*

2.  **Surjective (Onto)**: $f$ is surjective if every element in the codomain is the output for at least one input. The range is equal to the codomain.
    $$ \forall y \in B, \quad \exists x \in A \text{ such that } f(x) = y $$

3.  **Bijective**: $f$ is bijective if it is both **injective** and **surjective**. A bijection creates a perfect pairing between the elements of the domain and the codomain.

---

### Composition and Inverse Functions

- **Function Composition**: Given $f: A \to B$ and $g: B \to C$, the composite function $g \circ f: A \to C$ is defined by:
  $$ (g \circ f)(x) = g(f(x)) $$

> [!tip] Theorem: Properties of Composition
> Let $f: A \to B$ and $g: B \to C$.
> 1. If $f$ and $g$ are both injective, then $g \circ f$ is injective.
> 2. If $f$ and $g$ are both surjective, then $g \circ f$ is surjective.
> 3. If $f$ and $g$ are both bijective, then $g \circ f$ is bijective.

- **Inverse Function**: If $f: A \to B$ is a bijective function, then its inverse function $f^{-1}: B \to A$ exists. It is the unique function such that for all $x \in A$ and $y \in B$:
  $$ f^{-1}(y) = x \iff f(x) = y $$

> [!tip] Theorem: Existence of an Inverse Function
> A function $f: A \to B$ has an inverse function $f^{-1}: B \to A$ if and only if $f$ is **bijective**.

---

### Functions and Sets (Image and Preimage)

- **Image of a Set**: Let $f: A \to B$ and $S \subseteq A$. The image of $S$ under $f$ is:
  $$ f(S) = \{f(x) \mid x \in S\} $$

- **Preimage of a Set**: Let $f: A \to B$ and $T \subseteq B$. The preimage (or inverse image) of $T$ under $f$ is:
  $$ f^{-1}(T) = \{x \in A \mid f(x) \in T\} $$
  *Note: The notation $f^{-1}(T)$ is used even if the inverse function $f^{-1}$ does not exist.*

> [!tip] Theorem: Properties of Image and Preimage
> Let $f: A \to B$, and let $S_1, S_2 \subseteq A$ and $T_1, T_2 \subseteq B$.
> 1. $f(S_1 \cup S_2) = f(S_1) \cup f(S_2)$
> 2. $f(S_1 \cap S_2) \subseteq f(S_1) \cap f(S_2)$ (Equality holds if $f$ is injective)
> 3. $f^{-1}(T_1 \cup T_2) = f^{-1}(T_1) \cup f^{-1}(T_2)$
> 4. $f^{-1}(T_1 \cap T_2) = f^{-1}(T_1) \cap f^{-1}(T_2)$

### Excercises
too lazy bro, it's easy anyway
