
### Excercises

  > [!question] Prove inf and sup $S_{4}$ 
  > Let $S_{4}={1-\frac{(-1)^{n}}{n} : n \in \mathbb{N}}.$  Find $inf \,S_{4} \,\text{and} \,sup \, S_{4}$

>[!success]- Solution
> **Claim:** $\sup(S) = 2$.   
>  We must show $s_n \le 2$ for all $n \in \mathbb{N} \text{ (i.e 2 is the upperbound of} \, S_{4})$. 
>   - If $n$ is odd, $s_n = 1 + \frac{1}{n}$. Since $n \ge 1$, then $\frac{1}{n} \le 1$, so $s_n \le 1+1=2$. 
>   - If $n$ is even, $s_n = 1 - \frac{1}{n}$. Since $n \ge 2$, then $s_n < 1 < 2$. 
>   - Thus, 2 is an upper bound for $S$. 
**We now show 2 is the least upper bound:** 
>   - For any $\epsilon > 0$, we must find an element $s_k \in S$ such that $s_k > 2 - \epsilon$. 
>   - Choose $s_k = s_1 = 2$. 
>   - The condition $2 > 2 - \epsilon$ simplifies to $\epsilon > 0$, which is true by definition. 
>   - Thus, no number smaller than 2 can be an upper bound. Since 2 is the least upper bound, $\sup(S) = 2$. 
> 
>  **Claim:** $\inf(S) = \frac{1}{2}$. 
>**1/2 is a lower bound:** 
>   - We must show $s_n \ge \frac{1}{2}$ for all $n \in \mathbb{N}$. 
>   - If $n$ is odd, $s_n = 1 + \frac{1}{n} > 1 > \frac{1}{2}$. 
>   - If $n$ is even, $s_n = 1 - \frac{1}{n}$. Since $n \ge 2$, then $\frac{1}{n} \le \frac{1}{2}$, which implies $s_n = 1 - \frac{1}{n} \ge 1 - \frac{1}{2} = \frac{1}{2}$. > Thus, 1/2 is a lower bound for $S$. 
**1/2 is the greatest lower bound:** 
>   - For any $\epsilon > 0$, we must find an element $s_k \in S$ such that $s_k < \frac{1}{2} + \epsilon$. 
>   - Choose $s_k = s_2 = \frac{1}{2}$. 
>   - The condition $\frac{1}{2} < \frac{1}{2} + \epsilon$ simplifies to $0 < \epsilon$, which is true by definition. 
>   - Thus, no number larger than 1/2 can be a lower bound. Since 1/2 is the greatest lower bound, $\inf(S) = \frac{1}{2}$.

