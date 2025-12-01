# Hampiran Turunan (Diferensiasi Numerik)

Berasal dari deret Taylor: $f(x+h) = f(x) + f'(x)h + \frac{f''(x)}{2!}h^2 + \dots$

## 1. Rumus Selisih (Finite Difference)

### A. Beda Maju (Forward Difference)
$$f'(x_i) \approx \frac{f(x_{i+1}) - f(x_i)}{h}$$
* Error: $O(h)$

### B. Beda Mundur (Backward Difference)
$$f'(x_i) \approx \frac{f(x_i) - f(x_{i-1})}{h}$$
* Error: $O(h)$

### C. Beda Pusat (Central Difference)
Mengurangkan Taylor maju dan mundur.
$$f'(x_i) \approx \frac{f(x_{i+1}) - f(x_{i-1})}{2h}$$
* Error: $O(h^2)$ (Lebih akurat).

## 2. Derivatif Orde Tinggi (Well-known Formulas)
Didapat dari manipulasi deret Taylor.

> [!tips] Turunan Kedua (Beda Pusat)
> $$f''(x_i) \approx \frac{f(x_{i+1}) - 2f(x_i) + f(x_{i-1})}{h^2}$$
> Error: $O(h^2)$