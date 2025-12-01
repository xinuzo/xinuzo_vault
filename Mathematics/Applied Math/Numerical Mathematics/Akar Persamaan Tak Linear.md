#

Tujuan: Mencari nilai $x$ sehingga $f(x) = 0$.

## 1. Metode Pengurung (Bracketing Methods)
Metode yang menjamin konvergensi karena akar dikurung dalam interval $[a, b]$ di mana $f(a)f(b) < 0$.

### A. Metode Bagi Dua (Bisection)
Membagi interval menjadi dua bagian sama besar secara iteratif.
* **Rumus:** $c = \frac{a+b}{2}$
* **Logika:** Jika $f(a)f(c) < 0$, akar ada di $[a, c]$, set $b=c$. Jika tidak, akar di $[c, b]$, set $a=c$.
* **Kekonvergenan:** Lambat (Linear).

### B. Metode Posisi Palsu (False Position / Regula Falsi)
Memanfaatkan kemiringan garis yang menghubungkan titik batas untuk estimasi akar.
* **Rumus:**
    $$c = b - \frac{f(b)(b-a)}{f(b)-f(a)}$$
* **Kelebihan:** Umumnya lebih cepat dari bagi dua, namun bisa terjebak jika kurva sangat cembung/cekung (salah satu titik ujung stagnan).

## 2. Metode Terbuka (Open Methods)
Tidak memerlukan pengurungan akar. Konvergensi tidak dijamin, tapi biasanya lebih cepat.

### A. Newton-Raphson
Menggunakan garis singgung (turunan) di titik tebakan awal.

[!tips] Rumus Newton-Raphson
$$x_{i+1} = x_i - \frac{f(x_i)}{f'(x_i)}$$



> [!failure] Kapan Newton-Raphson Gagal?
> 1.  **Turunan Nol:** Jika $f'(x_i) \approx 0$ (titik puncak/lembah), pembagian dengan nol terjadi (overflow).
> 2.  **Osilasi:** Pada fungsi tertentu, nilai $x$ bisa bolak-balik di sekitar akar tanpa pernah mendekat.
> 3.  **Tebakan Awal Buruk:** Jika $x_0$ terlalu jauh dari akar, metode bisa divergen ke akar lain atau ke tak hingga.

### B. Metode Secant
Modifikasi Newton-Raphson jika $f'(x)$ sulit dicari. Turunan didekati dengan beda hingga mundur.
* **Rumus:**
    $$x_{i+1} = x_i - \frac{f(x_i)(x_{i-1} - x_i)}{f(x_{i-1}) - f(x_i)}$$

### C. Lokalisasi Akar Polinom
Untuk polinom $P_n(x) = a_n x^n + \dots + a_0$.
* **Batas Cauchy:** Semua akar (real/kompleks) berada dalam lingkaran $|z| \le 1 + \frac{\max(|a_0|, \dots, |a_{n-1}|)}{|a_n|}$.

## 3. Laju Kekonvergenan

[!tips] Definisi Laju Konvergensi
Misal $e_{i+1}$ adalah galat iterasi ke $i+1$. Jika $\lim_{i \to \infty} \frac{|e_{i+1}|}{|e_i|^p} = C$, maka $p$ adalah orde konvergensi.

* **Bagi Dua / False Position:** Linear ($p=1$).
* **Secant:** Superlinear ($p \approx 1.618$, Rasio Emas).
* **Newton-Raphson:** Kuadratik ($p=2$, galat berkurang pangkat dua setiap iterasi).