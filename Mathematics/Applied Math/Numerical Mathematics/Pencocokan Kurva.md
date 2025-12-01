

Tujuan: Mencari kurva terbaik yang mewakili tren data (tidak harus melewati setiap titik).

## 1. Regresi Linear (Kuadrat Terkecil)
Model: $y = a_0 + a_1 x$
Error kuadrat ($S_r$): $\sum (y_i - a_0 - a_1 x_i)^2$

> [!success]- Penurunan Rumus (Untuk n titik)
> Kita ingin meminimalkan $S_r$. Turunkan parsial terhadap $a_0$ dan $a_1$ lalu samakan dengan 0.
>
> 1. $\frac{\partial S_r}{\partial a_0} = -2 \sum (y_i - a_0 - a_1 x_i) = 0$
>    $\sum y_i - n a_0 - a_1 \sum x_i = 0 \Rightarrow n a_0 + a_1 \sum x_i = \sum y_i$
>
> 2. $\frac{\partial S_r}{\partial a_1} = -2 \sum (y_i - a_0 - a_1 x_i)x_i = 0$
>    $\sum x_i y_i - a_0 \sum x_i - a_1 \sum x_i^2 = 0 \Rightarrow a_0 \sum x_i + a_1 \sum x_i^2 = \sum x_i y_i$
>
> Didapat SPL (Persamaan Normal):
> $$
> \begin{bmatrix} n & \sum x_i \\ \sum x_i & \sum x_i^2 \end{bmatrix} \begin{bmatrix} a_0 \\ a_1 \end{bmatrix} = \begin{bmatrix} \sum y_i \\ \sum x_i y_i \end{bmatrix}
> $$

### Rumus $a_1$ dan $a_0$
$$a_1 = \frac{n \sum x_i y_i - \sum x_i \sum y_i}{n \sum x_i^2 - (\sum x_i)^2}$$
$$a_0 = \bar{y} - a_1 \bar{x}$$

## 2. Linearitas Data (Transformasi)
Agar model non-linear bisa diselesaikan dengan regresi linear:
* **Eksponensial** ($y = \alpha e^{\beta x}$):
    $\ln y = \ln \alpha + \beta x \Rightarrow$ Plot $\ln y$ vs $x$.
* **Pangkat** ($y = \alpha x^\beta$):
    $\log y = \log \alpha + \beta \log x \Rightarrow$ Plot $\log y$ vs $\log x$.
* **Laju Pertumbuhan/Saturasi** ($y = \frac{\alpha x}{\beta + x}$):
    Balik persamaan: $1/y = 1/\alpha + (\beta/\alpha)(1/x) \Rightarrow$ Plot $1/y$ vs $1/x$.