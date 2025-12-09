
### 1. Kendala Persamaan Linear

Masalah: $\min f(\mathbf{x})$ dengan kendala $A\mathbf{x} = \mathbf{b}$.

> [!tips] Syarat Perlu & Cukup (Lokal)
> 
> Syarat Perlu Orde-1 (Lagrange):
> 
> Jika $\mathbf{x}^*$ adalah minimizer lokal, maka ada vektor $\lambda$ sedemikian rupa sehingga:
> 
> $$\nabla f(\mathbf{x}^*) + A^T \lambda = \mathbf{0}$$
> 
> Syarat Cukup Orde-2:
> 
> Misalkan $\mathbf{x}^*$ memenuhi syarat perlu di atas. Jika matriks Hessian tereduksi (Reduced Hessian) adalah Definit Positif, maka $\mathbf{x}^*$ adalah minimizer lokal yang ketat.
> 
> $$Z^T \nabla^2 f(\mathbf{x}^*) Z \succ 0$$
> 
> Di mana $Z$ adalah matriks basis untuk ruang nol (null space) dari $A$ (yaitu $AZ = 0$).

> [!success]- Bukti Singkat / Ide Pembuktian
> 
> Ide Bukti:
> 
> Strategi utamanya adalah Reduksi Variabel atau dekomposisi ruang.
> 
> 1. Karena $A\mathbf{x}=\mathbf{b}$, kita bisa menulis solusi sebagai $\mathbf{x} = \mathbf{x}_p + Z\mathbf{v}$, di mana $\mathbf{x}_p$ adalah solusi partikular dan $\mathbf{v}$ adalah variabel bebas di ruang nol.
>     
> 2. Substitusi ini mengubah masalah terkendala menjadi masalah **tanpa kendala** terhadap variabel $\mathbf{v}$: $\phi(\mathbf{v}) = f(\mathbf{x}_p + Z\mathbf{v})$.
>     
> 3. Terapkan syarat perlu/cukup kalkulus biasa ($\nabla \phi = 0$ dan $\nabla^2 \phi \succ 0$) pada fungsi baru ini.
>     
> 4. $\nabla \phi(\mathbf{v}) = Z^T \nabla f(\mathbf{x})$. Syarat $\nabla \phi = 0$ mengimplikasikan $\nabla f$ tegak lurus terhadap $Z$, yang berarti $\nabla f$ berada di ruang baris $A$ ($\nabla f = -A^T\lambda$).
>     

---

### 2. Kendala Persamaan Tak Linear

Masalah: $\min f(\mathbf{x})$ dengan kendala $h_i(\mathbf{x}) = 0, \, i=1,\dots,m$.

> [!tips] Syarat Perlu & Cukup
> 
> Definisi Lagrangian: $\mathcal{L}(\mathbf{x}, \lambda) = f(\mathbf{x}) + \sum \lambda_i h_i(\mathbf{x})$.
> 
> Syarat Perlu (FONC):
> 
> $\nabla_{\mathbf{x}} \mathcal{L}(\mathbf{x}^*, \lambda^*) = 0$ dan $h(\mathbf{x}^*) = 0$. (Syarat: Regularity / LICQ terpenuhi).
> 
> **Syarat Cukup (SOSC):**
> 
> 1. Memenuhi syarat perlu.
>     
> 2. Hessian Lagrangian $\nabla_{xx}^2 \mathcal{L}(\mathbf{x}^*, \lambda^*)$ bersifat Definit Positif pada Ruang Singgung.
>     
>     $$\mathbf{y}^T \nabla_{xx}^2 \mathcal{L} \mathbf{y} > 0, \quad \forall \mathbf{y} \neq 0 \text{ s.t. } \nabla h(\mathbf{x}^*)^T \mathbf{y} = 0$$
>     

> [!success]- Bukti Singkat / Referensi
> 
> Ide Bukti:
> 
> Menggunakan Teorema Fungsi Implisit atau ekspansi Taylor pada permukaan kendala (surface manifold).
> 
> 1. **Lintasan:** Tinjau sebuah lintasan (kurva) $\mathbf{x}(t)$ yang berada di permukaan kendala $h(\mathbf{x})=0$ dan melewati $\mathbf{x}^*$ pada $t=0$.
>     
> 2. **Orde 1:** Agar $\mathbf{x}^*$ minimum, turunan $f$ sepanjang kurva harus nol: $\frac{d}{dt}f(\mathbf{x}(t)) = \nabla f^T \dot{\mathbf{x}} = 0$. Karena $\nabla h^T \dot{\mathbf{x}} = 0$, maka $\nabla f$ harus sejajar dengan $\nabla h$ (kombinasi linear).
>     
> 3. Orde 2: Turunan kedua sepanjang kurva harus positif. Ini menghasilkan suku $\mathbf{y}^T \nabla^2 f \mathbf{y} + \text{suku kurvatur dari kendala}$. Suku kurvatur ini diserap oleh Lagrange multiplier, membentuk Hessian Lagrangian $\nabla^2 \mathcal{L}$.
>     
>     Referensi: Nocedal & Wright, Numerical Optimization, Chapter 12.
>     

---

### 3. Kendala Pertidaksamaan Linear

Masalah: $\min f(\mathbf{x})$ dengan kendala $A\mathbf{x} \ge \mathbf{b}$.

> [!tips] Syarat Perlu & Cukup
> 
> Syarat Perlu (KKT Linear):
> 
> Sama seperti KKT umum, namun syarat regularitas (Constraint Qualification) otomatis terpenuhi karena kendala linear (Linearity Constraint Qualification).
> 
> **Syarat Cukup:**
> 
> 1. Memenuhi KKT.
>     
> 2. **Jika f(x) konveks:** Syarat perlu KKT otomatis menjadi syarat cukup (Global Minimum).
>     
> 3. Jika f(x) non-konveks: Hessian tereduksi pada himpunan kendala aktif ($\mathcal{A}$) harus definit positif.
>     
>     $$Z_{\mathcal{A}}^T \nabla^2 f(\mathbf{x}^*) Z_{\mathcal{A}} \succ 0$$
>     
>     (Hanya memperhitungkan baris $A$ yang aktif/tight sebagai persamaan).
>     

> [!success]- Bukti Singkat
> 
> Ide Bukti (Kasus Konveks):
> 
> Menggunakan sifat Supporting Hyperplane dan konveksitas.
> 
> 4. Jika $f$ konveks, maka $f(\mathbf{y}) \ge f(\mathbf{x}^*) + \nabla f(\mathbf{x}^*)^T(\mathbf{y}-\mathbf{x}^*)$.
>     
> 5. Dari kondisi stasioner KKT: $\nabla f(\mathbf{x}^*) = A^T \mu$ dengan $\mu \ge 0$.
>     
> 6. Substitusi: $f(\mathbf{y}) \ge f(\mathbf{x}^*) + \mu^T A(\mathbf{y}-\mathbf{x}^*)$.
>     
> 7. Analisis kelayakan (feasibility) menunjukkan bahwa suku terakhir $\ge 0$, sehingga $f(\mathbf{y}) \ge f(\mathbf{x}^*)$.
>     

---

### 4. KKT (Kendala Pertidaksamaan Tak Linear)

Masalah: $\min f(\mathbf{x})$ s.t. $h(\mathbf{x})=0, g(\mathbf{x}) \le 0$.

> [!tips] Syarat Perlu & Cukup
> 
> Syarat Perlu (Karush-Kuhn-Tucker / KKT):
> 
> Agar $\mathbf{x}^*$ menjadi kandidat minimizer, harus memenuhi 4 kondisi (asumsi LICQ terpenuhi):
> 
> 1. **Stationarity:** $\nabla f + \sum \lambda_i \nabla h_i + \sum \mu_j \nabla g_j = 0$
>     
> 2. **Primal Feasibility:** $h(\mathbf{x}) = 0, g(\mathbf{x}) \le 0$
>     
> 3. **Dual Feasibility:** $\mu_j \ge 0$
>     
> 4. **Complementary Slackness:** $\mu_j g_j(\mathbf{x}) = 0$
>     
> 
> **Syarat Cukup (Second Order Sufficient Condition / SOSC):**
> 
> 1. Memenuhi syarat KKT.
>     
> 2. Hessian Lagrangian definit positif pada Critical Cone ($C$).
>     
>     $$\mathbf{w}^T \nabla_{xx}^2 \mathcal{L} \mathbf{w} > 0, \quad \forall \mathbf{w} \in C, \mathbf{w} \neq 0$$
>     
>     (Critical cone adalah himpunan arah $w$ yang tegak lurus gradien kendala aktif yang multiplier-nya positif).
>     

> [!success]- Bukti Singkat / Referensi
> 
> Ide Bukti (Farkas' Lemma):
> 
> Pembuktian syarat perlu KKT sangat bergantung pada Lemma Farkas (teorema alternatif untuk pertidaksamaan linear).
> 
> 1. Secara geometris, agar tidak ada arah penurunan ("descent direction") yang layak (feasible), gradien negatif $-\nabla f$ harus berada di dalam "kerucut" yang dibentuk oleh gradien kendala aktif.
>     
> 2. Lemma Farkas menjamin keberadaan multiplier $\mu \ge 0$ jika kondisi geometri tersebut terpenuhi.
>     
> 3. Untuk syarat cukup orde-2, pendekatannya mirip dengan kasus persamaan tak linear, tetapi ruang nol-nya diganti dengan critical cone untuk menangani sifat satu arah dari pertidaksamaan.
>     
>     Referensi: Materi pada menunjukkan penggunaan matriks ruang nol $Z$ pada kendala aktif untuk memeriksa kedefinitan Hessian Lagrangian, yang merupakan implementasi praktis dari SOSC.
>