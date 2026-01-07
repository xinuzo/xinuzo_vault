>[!tips] 7.79 Evaluation of Improper Integrals
>If $f(x) = p(x)/q(x)$ and $q(x)$ has no real zeros and deg $q \ge$ deg $p + 2$:
>$$\int_{-\infty}^\infty f(x) dx = 2\pi i \sum \text{Res } f(z) \text{ (in upper half plane)}$$
>

>[!tips] 7.80 Jordan's Lemma
>If $f(z)$ is analytic in the upper half plane outside a circle $R_0$, and $|f(z)| \le M_R \to 0$ as $R \to \infty$, then for $a > 0$:
>$$\lim_{R \to \infty} \int_{C_R} f(z) e^{iaz} dz = 0$$
>Used for integrals of type $\int_{-\infty}^\infty f(x) \sin(ax) dx$.

>[!tips] 7.85 Definite Integrals of Trig Functions
>Integrals of the form $\int_0^{2\pi} F(\sin \theta, \cos \theta) d\theta$ can be converted to contour integrals on the unit circle $|z|=1$ using $z = e^{i\theta}$, $\sin \theta = (z - z^{-1})/2i$, $d\theta = dz/iz$.

>[!tips] 7.87 Rouché's Theorem
>If $f(z)$ and $g(z)$ are analytic inside and on $C$, and $|f(z)| > |g(z)|$ on $C$, then $f(z)$ and $f(z) + g(z)$ have the same number of zeros inside $C$.