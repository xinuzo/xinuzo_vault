> [!question] Isomorphism of $\mathbb{C}$ and $\mathbb{R}[x]/(x^2+1)$
> Show that the field of complex numbers $\mathbb{C}$ is isomorphic to the quotient ring of polynomials with real coefficients modulo $x^2+1$.
> $$\mathbb{R}[x] / (x^2 + 1) \cong \mathbb{C}$$

> [!success]- Solution
> We use the **First Isomorphism Theorem for Rings**.
> 
> **1. Define a Homomorphism**
> Let $\phi: \mathbb{R}[x] \to \mathbb{C}$ be the evaluation homomorphism that maps $x$ to the imaginary unit $i$:
> $$\phi(f(x)) = f(i)$$
> 
> **2. Show Surjectivity (Onto)**
> For any complex number $z = a + bi \in \mathbb{C}$ (where $a, b \in \mathbb{R}$), consider the polynomial $f(x) = a + bx \in \mathbb{R}[x]$.
> Applying the map:
> $$\phi(a + bx) = a + b(i) = z$$
> Since every complex number has a pre-image, $\text{Im}(\phi) = \mathbb{C}$.
> 
> **3. Find the Kernel**
> The kernel consists of all polynomials $f(x)$ such that $f(i) = 0$.
> * We know $x^2 + 1$ is in the kernel because $i^2 + 1 = 0$.
> * Since $x^2 + 1$ is irreducible over $\mathbb{R}$, it is the minimal polynomial for $i$.
> * Any polynomial with root $i$ must be a multiple of the minimal polynomial.
> 
> Therefore, $\ker(\phi) = (x^2 + 1)$.
> 
> **4. Conclusion**
> By the First Isomorphism Theorem ($R / \ker(\phi) \cong \text{Im}(\phi)$):
> $$\mathbb{R}[x] / (x^2 + 1) \cong \mathbb{C}$$
> 
> *Intuitively, this means declaring "$\boldsymbol{x^2 = -1}$" in polynomials creates a system algebraically identical to the complex numbers.*

> [!question] Isomorphism of Matrix Subring and $\mathbb{C}$
> Let $S$ be the set of all matrices of the form $\begin{pmatrix} a & b \\ -b & a \end{pmatrix}$ with $a, b \in \mathbb{R}$.
> Show that $S$ is isomorphic to the field of complex numbers $\mathbb{C}$ under matrix addition and multiplication.

> [!success]- Solution
> We define a mapping $\phi: S \to \mathbb{C}$ and show it is a bijective ring homomorphism.
> 
> **1. Define the Map**
> Let $\phi \left( \begin{pmatrix} a & b \\ -b & a \end{pmatrix} \right) = a + bi$.
> 
> **2. Check Addition (Homomorphism)**
> Let $A = \begin{pmatrix} a & b \\ -b & a \end{pmatrix}$ and $B = \begin{pmatrix} c & d \\ -d & c \end{pmatrix}$.
> $$A + B = \begin{pmatrix} a+c & b+d \\ -(b+d) & a+c \end{pmatrix}$$
> Applying the map:
> $$\phi(A+B) = (a+c) + (b+d)i = (a+bi) + (c+di) = \phi(A) + \phi(B)$$
> 
> **3. Check Multiplication (Homomorphism)**
> Matrix multiplication of $A$ and $B$:
> $$AB = \begin{pmatrix} a & b \\ -b & a \end{pmatrix} \begin{pmatrix} c & d \\ -d & c \end{pmatrix} = \begin{pmatrix} ac-bd & ad+bc \\ -bc-ad & -bd+ac \end{pmatrix}$$
> Note that the bottom-left term is $-(ad+bc)$, preserving the form of $S$.
> 
> Applying the map to the product:
> $$\phi(AB) = (ac-bd) + (ad+bc)i$$
> 
> Now compare this to the product in $\mathbb{C}$:
> $$\phi(A)\phi(B) = (a+bi)(c+di) = ac + adi + bci + bdi^2$$
> Since $i^2 = -1$:
> $$= (ac-bd) + (ad+bc)i$$
> 
> Since $\phi(AB) = \phi(A)\phi(B)$, the map preserves multiplication.
> 
> **4. Conclusion (Bijectivity)**
> * **Surjective:** For any $z = x+yi \in \mathbb{C}$, the matrix $\begin{pmatrix} x & y \\ -y & x \end{pmatrix}$ exists in $S$.
> * **Injective:** If $\phi(A) = 0$, then $a+bi = 0$, implying $a=0, b=0$. Thus $A$ is the zero matrix.
> 
> Therefore, $S \cong \mathbb{C}$.