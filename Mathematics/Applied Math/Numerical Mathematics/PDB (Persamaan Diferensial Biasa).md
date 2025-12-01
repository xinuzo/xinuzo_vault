# PDB: Masalah Nilai Awal (MNA) & Batas (MNB)

Bentuk: $\frac{dy}{dx} = f(x, y)$ dengan $y(x_0) = y_0$.

## 1. MNA (Metode Satu Langkah)

### A. Metode Euler
Paling dasar, error besar $O(h)$.
$$y_{i+1} = y_i + f(x_i, y_i)h$$

### B. Metode Heun (Euler yang Diperbaiki)
Prediktor-Korektor sederhana.
1.  Prediksi: $y^0_{i+1} = y_i + f(x_i, y_i)h$
2.  Koreksi: $y_{i+1} = y_i + \frac{f(x_i, y_i) + f(x_{i+1}, y^0_{i+1})}{2}h$

### C. Deret Taylor
Menyertakan turunan orde tinggi ($f', f'', \dots$). Akurat tapi sulit menurunkan fungsi $f(x,y)$ secara analitik berulang kali.

### D. Runge-Kutta (RK4)
Metode standar "kuda beban" numerik. Akurasi $O(h^4)$ tanpa menghitung turunan analitik.
$$y_{i+1} = y_i + \frac{1}{6}(k_1 + 2k_2 + 2k_3 + k_4)h$$
Dimana $k_1, k_2, k_3, k_4$ adalah evaluasi slope di berbagai titik dalam interval langkah.

## 2. MNA (Metode Banyak Langkah / Prediktor-Korektor)
Menggunakan informasi dari beberapa titik sebelumnya ($i, i-1, i-2 \dots$).

### A. Adams-Bashforth-Moulton
* **Prediktor (Adams-Bashforth):** Ekstrapolasi eksplisit.
* **Korektor (Adams-Moulton):** Interpolasi implisit untuk memperbaiki nilai.

### B. Milne-Simpson
Menggunakan rumus integrasi Newton-Cotes terbuka dan tertutup. Rentan terhadap ketidakstabilan.

### C. Metode Hamming
Modifikasi Milne untuk kestabilan yang lebih baik.

## 3. MNB (Masalah Nilai Batas)
Diketahui nilai di ujung $y(a)$ dan $y(b)$, bukan $y(a)$ dan $y'(a)$.

### A. Metode Penembakan (Shooting Method)
Mengubah MNB menjadi masalah MNA. Kita "menebak" nilai $y'(a)$ (sudut tembakan), lalu mengintegrasikan ke $b$. Jika $y(b)$ tidak kena target, koreksi sudut tembakan (biasanya dengan interpolasi linear/secant).

### B. Metode Beda Hingga (Finite Difference)
Mengganti turunan dalam persamaan diferensial dengan aproksimasi beda pusat.
Misal $y'' = f(x,y)$.
Ganti $y''$ dengan $\frac{y_{i+1} - 2y_i + y_{i-1}}{h^2}$.
Ini akan menghasilkan Sistem Persamaan Linear (Tridiagonal) yang diselesaikan serentak.