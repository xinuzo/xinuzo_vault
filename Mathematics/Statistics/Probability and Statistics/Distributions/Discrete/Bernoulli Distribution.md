>[!tips] (Definition) Bernoulli Experiment
>A **Bernoulli** **experiment** is a **random experiment**, the outcome of which can be classified in but one of **two mutually exclusive and exhaustive ways**, for instance, success or failure (e.g., female or male, life or death, nondefective or defective).

A sequence of **Bernoulli trials** occurs when a **Bernoulli experiment** is performed **several independent times** so that the probability of success, say $p$, remains the same from trial to trial.

>[!tips] (Definition) Bernoulli Distribution
>Let $X$ be a random variable associated with **Bernoulli trial**, written $X \sim Ber(p)$, defined by:
>$$X(\text{success})=1 \text{, }X(\text{fail})=0$$ \
>then the **p.m.f of X** is
> $$p(x)=p^{x}(1-p)^{x}, \quad x=0,1,\dots$$ 

it is easy to show that $\mu=p$ and $\sigma^2=p(1-p)$ .

>[!success]- Proof of $\mu$ and $\sigma^2$
>$μ =E[X]=(0)(1−p)+(1)(p)=p$ \
>$σ^2 =Var(X)=p^{2}(1−p)+(1−p)^{2}p = p(1−p).$


