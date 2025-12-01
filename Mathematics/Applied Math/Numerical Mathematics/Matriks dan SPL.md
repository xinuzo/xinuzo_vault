# 

Bentuk: $A\mathbf{x} = \mathbf{b}$

## 1. Metode Langsung (Eliminasi)

### A. Eliminasi Gauss
Mengubah matriks menjadi segitiga atas (Upper Triangular) lalu substitusi mundur.
* **Kompleksitas:** $O(n^3/3)$.

### B. Strategi Penumpuan (Pivoting)
Diperlukan jika elemen pivot ($a_{kk}$) bernilai 0 atau sangat kecil (menghindari galat pembulatan besar).
1.  **Penumpuan Parsial (Partial Pivoting):** Menukar baris $k$ dengan baris di bawahnya yang memiliki $|a_{ik}|$ terbesar pada kolom yang sama.
2.  **Penumpuan Parsial Berskala (Scaled Partial Pivoting):** Memilih pivot berdasarkan rasio elemen terhadap nilai maksimum di barisnya masing-masing.

### C. Matriks Tridiagonal (Algoritma Thomas)
Khusus matriks pita (tridiagonal). Sangat efisien ($O(n)$).
* Proses: Dekomposisi LU khusus tanpa pivoting.

### D. Dekomposisi LU
Memecah $A = L U$. Solusi dicari dengan $L\mathbf{y}=\mathbf{b}$ lalu $U\mathbf{x}=\mathbf{y}$.

> [!tips] Jenis-Jenis Dekomposisi
> * **Doolittle:** Diagonal $L$ bernilai 1 ($l_{ii}=1$).
> * **Crout:** Diagonal $U$ bernilai 1 ($u_{ii}=1$).
> * **Cholesky:** Untuk matriks simetri definit positif. $A = L L^T$ (Diagonal $L$ dan $U$ sama, $u_{ii} = l_{ii}$).



[Image of Matrix LU Decomposition]


## 2. Metode Iteratif
Digunakan untuk matriks besar dan jarang (sparse).

### A. Jacobi
Nilai $x$ baru dihitung berdasarkan nilai $x$ iterasi sebelumnya *secara total*.
$$x_i^{(k+1)} = \frac{1}{a_{ii}} (b_i - \sum_{j \ne i} a_{ij} x_j^{(k)})$$

### B. Gauss-Seidel
Nilai $x$ baru langsung digunakan untuk menghitung elemen berikutnya dalam iterasi yang sama.
$$x_i^{(k+1)} = \frac{1}{a_{ii}} (b_i - \sum_{j < i} a_{ij} x_j^{(k+1)} - \sum_{j > i} a_{ij} x_j^{(k)})$$
*(Catatan: Anda menyebutkan Gauss-Legendre di prompt, namun dalam konteks SPL pasangan Jacobi biasanya adalah Gauss-Seidel. Gauss-Legendre adalah metode integrasi).*

> [!tips] Syarat Konvergensi Iteratif
> Matriks harus **Dominan Diagonal Secara Mutlak (Diagonally Dominant):**
> $|a_{ii}| > \sum_{j \ne i} |a_{ij}|$