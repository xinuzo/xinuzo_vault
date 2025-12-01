#

Bentuk: $\frac{\partial T}{\partial t} = k \frac{\partial^2 T}{\partial x^2}$
Indeks: $i$ untuk ruang ($x$), $n$ untuk waktu ($t$).

## 1. FTCS (Forward Time Central Space) - Skema Eksplisit
Turunan waktu (maju), turunan ruang (pusat).
* **Rumus:**
    $$\frac{T_i^{n+1} - T_i^n}{\Delta t} = k \frac{T_{i+1}^n - 2T_i^n + T_{i-1}^n}{(\Delta x)^2}$$
* **Pengerjaan:** Kita bisa langsung menghitung $T_i^{n+1}$ (waktu masa depan) hanya dari data waktu sekarang ($n$).
* **Syarat Stabil:** $\lambda = \frac{k \Delta t}{(\Delta x)^2} \le 0.5$. Jika tidak, solusi meledak.

## 2. BTCS (Backward Time Central Space) - Skema Implisit
Turunan waktu (mundur), turunan ruang (pusat pada waktu $n+1$).
* **Rumus:**
    $$\frac{T_i^{n+1} - T_i^n}{\Delta t} = k \frac{T_{i+1}^{n+1} - 2T_i^{n+1} + T_{i-1}^{n+1}}{(\Delta x)^2}$$
* **Pengerjaan:** Menghasilkan sistem persamaan linear yang harus diselesaikan setiap langkah waktu (biasanya tridiagonal).
* **Kelebihan:** Stabil tanpa syarat (unconditionally stable) untuk $\Delta t$ berapapun.

## 3. Crank-Nicolson
Rata-rata dari FTCS dan BTCS.
* **Rumus:**
    $$\frac{T_i^{n+1} - T_i^n}{\Delta t} = \frac{k}{2} \left[ \frac{\delta^2 T^n}{(\Delta x)^2} + \frac{\delta^2 T^{n+1}}{(\Delta x)^2} \right]$$
* **Pengerjaan:**
    $$- \lambda T_{i-1}^{n+1} + (2+2\lambda) T_i^{n+1} - \lambda T_{i+1}^{n+1} = \lambda T_{i-1}^n + (2-2\lambda) T_i^n + \lambda T_{i+1}^n$$
    Di mana $\lambda = \frac{k \Delta t}{(\Delta x)^2}$.
* **Kelebihan:** Stabil tanpa syarat dan error lebih kecil ($O(\Delta t^2, \Delta x^2)$) dibanding FTCS/BTCS.



> [!tips] Contoh Pengerjaan Crank-Nicolson
> 1.  Tentukan grid $\Delta x$ dan $\Delta t$. Hitung $\lambda$.
> 2.  Susun persamaan untuk setiap node internal $i$.
> 3.  Masukkan kondisi batas (Boundary Conditions) pada ujung kiri dan kanan.
> 4.  Bentuk matriks tridiagonal $A \mathbf{T}^{n+1} = \mathbf{b}$ (dimana $\mathbf{b}$ berisi nilai dari waktu $n$).
> 5.  Selesaikan dengan Algoritma Thomas untuk mendapatkan suhu di langkah waktu berikutnya.