# Interpolasi & Ekstrapolasi

Tujuan: Mencari fungsi yang **tepat melewati** semua titik data yang diketahui.

## 1. Interpolasi Lagrange
Tidak memerlukan penyelesaian SPL, langsung menggunakan fungsi basis.
* **Rumus Umum Polinom Orde $n$:**
    $$f_n(x) = \sum_{i=0}^n L_i(x) f(x_i)$$
* **Fungsi Basis $L_i(x)$:**
    $$L_i(x) = \prod_{j=0, j \ne i}^n \frac{x - x_j}{x_i - x_j}$$

## 2. Interpolasi Beda Terbagi Newton (Newton's Divided Difference)
Lebih disukai karena koefisien bisa dihitung secara tabelar dan rekursif.
* **Bentuk Umum:**
    $$f_n(x) = b_0 + b_1(x-x_0) + b_2(x-x_0)(x-x_1) + \dots + b_n(x-x_0)\dots(x-x_{n-1})$$
* **Rumus Koefisien ($b$):**
    * $b_0 = f(x_0)$
    * $b_1 = f[x_1, x_0] = \frac{f(x_1)-f(x_0)}{x_1-x_0}$
    * $b_2 = f[x_2, x_1, x_0] = \frac{f[x_2, x_1] - f[x_1, x_0]}{x_2 - x_0}$
    * Secara umum: $b_n = f[x_n, \dots, x_0]$