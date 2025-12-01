# 

Menghitung $I = \int_a^b f(x) dx$.

## 1. Metode Newton-Cotes (Titik Spasi Sama)

### A. Aturan Trapesium
Mengaproksimasi fungsi dengan garis lurus (polinom orde 1).
* **Rumus:** $I \approx \frac{h}{2} [f(x_0) + f(x_1)]$

> [!success]- Penurunan Rumus Trapesium
> Integralkan polinom interpolasi Newton orde 1 ($P_1(x) = f(a) + \frac{f(b)-f(a)}{b-a}(x-a)$) dari $a$ ke $b$.
> $\int_a^b P_1(x) dx = (b-a) \frac{f(a)+f(b)}{2}$. Karena $h=b-a$, maka $I \approx \frac{h}{2}(f_0 + f_1)$.

### B. Aturan Simpson 1/3
Mengaproksimasi dengan parabola (polinom orde 2). Butuh 3 titik (jumlah segmen genap).
* **Rumus:** $I \approx \frac{h}{3} [f_0 + 4f_1 + f_2]$

### C. Aturan Simpson 3/8
Mengaproksimasi dengan polinom orde 3. Butuh 4 titik (jumlah segmen kelipatan 3).
* **Rumus:** $I \approx \frac{3h}{8} [f_0 + 3f_1 + 3f_2 + f_3]$

### D. Aturan Boole
Untuk 5 titik.
* **Rumus:** $I \approx \frac{2h}{45} [7f_0 + 32f_1 + 12f_2 + 32f_3 + 7f_4]$

### E. Rumus Komposit (Gabungan)
Untuk interval luas, bagi menjadi $N$ segmen.
* **Trapesium Komposit:**
    $$I \approx \frac{h}{2} [f_0 + 2 \sum_{i=1}^{N-1} f_i + f_N]$$
* **Simpson 1/3 Komposit:**
    $$I \approx \frac{h}{3} [f_0 + 4 \sum_{ganjil} f_i + 2 \sum_{genap} f_i + f_N]$$



## 2. Integrasi Romberg
Memperbaiki akurasi Trapesium secara rekursif menggunakan Ekstrapolasi Richardson.
$$I_{j,k} \approx \frac{4^{k-1} I_{j+1, k-1} - I_{j, k-1}}{4^{k-1} - 1}$$

## 3. Kuadratur Gauss-Legendre
Mengubah variabel integrasi ke domain $[-1, 1]$ dan menentukan titik evaluasi ($x$) serta bobot ($w$) yang optimal, bukan spasi rata.
Transformasi variabel: $x = \frac{b+a}{2} + \frac{b-a}{2} z$.

* **Rumus:** $I \approx \frac{b-a}{2} \sum_{i=1}^n w_i f(z_i)$
* **2 Titik:**
    * $z = \pm \frac{1}{\sqrt{3}} \approx \pm 0.577$
    * Bobot $w = 1$
* **3 Titik:**
    * $z = 0$ ($w=8/9$)
    * $z = \pm \sqrt{0.6}$ ($w=5/9$)