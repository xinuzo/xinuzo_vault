
## Definitions and Theorems
![[Pasted image 20250930131038.png]]
source: MathPi/Youtube

> [!tips] (Definition) Group (Grup)
> Sebuah **grup** adalah pasangan $(G, *)$ di mana $G$ adalah sebuah himpunan dan $*$ adalah sebuah operasi biner (seperti penjumlahan atau perkalian) pada $G$ yang memenuhi empat sifat:
> 1.  **Tertutup (Closure):** Untuk setiap $a, b \in G$, hasil operasi $a * b$ juga berada di dalam $G$.
> 2.  **Asosiatif (Associativity):** Untuk setiap $a, b, c \in G$, berlaku $(a * b) * c = a * (b * c)$.
> 3.  **Elemen Identitas (Identity Element):** Terdapat sebuah elemen $e \in G$ (disebut elemen identitas) sedemikian sehingga untuk setiap $a \in G$, berlaku $e * a = a * e = a$.
> 4.  **Elemen Invers (Inverse Element):** Untuk setiap $a \in G$, terdapat sebuah elemen $a^{-1} \in G$ (disebut invers dari $a$) sedemikian sehingga $a * a^{-1} = a^{-1} * a = e$.

> [!tips] (Definition) Coset (Koset)
> Diberikan sebuah grup $G$ dan sebuah subgrup $H$. Untuk sembarang elemen $g \in G$:
> 1.  **Koset Kiri** dari $H$ yang diwakili oleh $g$ adalah himpunan $gH = \{gh \mid h \in H\}$.
> 2.  **Koset Kanan** dari $H$ yang diwakili oleh $g$ adalah himpunan $Hg = \{hg \mid h \in H\}$.
>

> [!tips] (Definition) Normal Subgroup 
> Sebuah subgrup $N$ dari grup $G$ disebut **subgrup normal** jika koset kiri dan koset kanannya selalu sama untuk semua elemen $g \in G$. Artinya, $gN = Ng$ untuk setiap $g \in G$.
>
> Subgrup normal sangat penting karena mereka memungkinkan pembentukan grup kuosien. Dalam grup Abelian (komutatif), semua subgrup adalah normal.

> [!tips] (Definition) Quotient Group
> Diberikan sebuah grup $G$ dan sebuah **subgrup normal** $N$. **Grup kuosien** (atau grup faktor), dinotasikan $G/N$, adalah himpunan **semua koset** dari $N$ di $G$, yang dilengkapi dengan operasi biner $*$ yang didefinisikan sebagai $(aN) * (bN) = (ab)N$.
>
> Grup kuosien pada dasarnya "meruntuhkan" semua elemen subgrup normal $N$ menjadi elemen identitas yang baru.

> [!tips] (Definition) Ring 
> Sebuah **cincin** adalah himpunan $R$ yang dilengkapi dengan dua operasi biner, biasanya disebut penjumlahan (+) dan perkalian ($\cdot$), yang memenuhi sifat-sifat berikut:
> 1.  $(R, +)$ adalah grup Abelian (komutatif).
> 2.  Perkalian bersifat asosiatif: $(a \cdot b) \cdot c = a \cdot (b \cdot c)$.
> 3.  Berlaku sifat distributif: $a \cdot (b+c) = (a \cdot b) + (a \cdot c)$ dan $(a+b) \cdot c = (a \cdot c) + (b \cdot c)$.

> [!tips] (Definition) Ideal
> Sebuah subhimpunan tak kosong $I$ dari sebuah cincin $R$ disebut **ideal kiri** jika:
> 4.  Untuk setiap $a, b \in I$, berlaku $a - b \in I$.
> 5.  Untuk setiap $r \in R$ dan $a \in I$, berlaku $r \cdot a \in I$.
> Disebut **ideal kanan** jika syarat kedua diganti menjadi $a \cdot r \in I$. Disebut **ideal dua sisi** (atau **ideal** saja) jika ia adalah ideal kiri sekaligus ideal kanan.
>
> Ideal memainkan peran dalam cincin yang mirip dengan peran subgrup normal dalam grup; mereka memungkinkan pembentukan cincin kuosien.

> [!tips] (Definition) Quotient Ring (Cincin Kuosien)
> Diberikan sebuah cincin $R$ dan sebuah **ideal dua sisi** $I$. **Cincin kuosien** (atau cincin faktor), dinotasikan $R/I$, adalah himpunan **semua koset jumlahan** $a+I = \{a+i \mid i \in I\}$ dari $I$ di $R$. Operasi penjumlahan dan perkalian pada $R/I$ didefinisikan sebagai:
> 6.  $(a+I) + (b+I) = (a+b) + I$
> 7.  $(a+I) \cdot (b+I) = (a \cdot b) + I$
>
> Sama seperti grup kuosien, cincin kuosien "meruntuhkan" semua elemen ideal $I$ menjadi elemen nol yang baru.
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