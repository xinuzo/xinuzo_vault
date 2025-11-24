> [!tips] (Definition) Uniform Distribution
> A distribution where all intervals of the same length on the distribution's support are equally probable.
> $$X \sim U(a, b)$$
> **P.D.F.:**
> $$f(x) = \frac{1}{b-a}, \quad a < x < b$$
> **MGF:**
> $$M(t) = \begin{cases} \frac{e^{tb}-e^{ta}}{t(b-a)} & t \neq 0 \\ 1 & t=0 \end{cases}$$
> **Mean & Variance:**
> $$\mu = \frac{a+b}{2}, \quad \sigma^2 = \frac{(b-a)^2}{12}$$

> [!success]- Proof of $\mu$ and $\sigma^2$
> $$E[X] = \int_a^b x \frac{1}{b-a} dx = \frac{1}{b-a} \left[ \frac{x^2}{2} \right]_a^b = \frac{b^2-a^2}{2(b-a)} = \frac{a+b}{2}$$
> $$E[X^2] = \int_a^b x^2 \frac{1}{b-a} dx = \frac{1}{b-a} \left[ \frac{x^3}{3} \right]_a^b = \frac{b^3-a^3}{3(b-a)} = \frac{a^2+ab+b^2}{3}$$
> $$\sigma^2 = \frac{a^2+ab+b^2}{3} - \left(\frac{a+b}{2}\right)^2 = \frac{4(a^2+ab+b^2) - 3(a^2+2ab+b^2)}{12} = \frac{(b-a)^2}{12}$$