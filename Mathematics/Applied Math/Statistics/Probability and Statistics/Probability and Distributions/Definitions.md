>[!tips] 1.1 Random Experiment, Sample Space
>A random experiment is an experiment that can be repeated under the same conditions and whose outcome cannot be predicted with certainty.
>The sample space, denoted by $\mathcal{C}$, is the collection of every possible outcome of a random experiment.

>[!tips] 1.1 Event
>An event is a subset of the sample space $\mathcal{C}$.

>[!tips] 1.1 Relative Frequency
>If an experiment is performed $N$ times and event $A$ occurs $f$ times, the ratio $f/N$ is the relative frequency of $A$. The probability $p$ is the number to which the relative frequency stabilizes as $N$ increases.

>[!tips] 1.2 Complement
>The complement of an event $A$, denoted $A^c$, is the set of all elements in $\mathcal{C}$ which are not in $A$.
>$$A^c = \{x \in \mathcal{C} : x \notin A\}$$

>[!tips] 1.2 Union and Intersection
>The union of $A$ and $B$, $A \cup B$, is the set of elements in $A$ or $B$ or both.
>The intersection of $A$ and $B$, $A \cap B$, is the set of elements in both $A$ and $B$.

>[!tips] 1.2 Disjoint
>Two events $A$ and $B$ are disjoint (mutually exclusive) if they have no elements in common, i.e., $A \cap B = \phi$.

>[!tips] 1.3 Probability Set Function
>A probability set function $P$ is a real-valued function defined on a collection of events $\mathcal{B}$ satisfying:
>1. $P(A) \ge 0$ for all $A \in \mathcal{B}$.
>2. $P(\mathcal{C}) = 1$.
>3. If $\{A_n\}$ is a sequence of pairwise disjoint events, then $P(\cup_{n=1}^{\infty} A_n) = \sum_{n=1}^{\infty} P(A_n)$.

>[!tips] 1.3 Equilikely Case
>If $\mathcal{C} = \{x_1, ..., x_m\}$ is finite and each outcome has the same probability $1/m$, then for any $A \subset \mathcal{C}$,
>$$P(A) = \frac{\#(A)}{m}$$

>[!tips] 1.4 Conditional Probability
>Let $A$ and $B$ be events with $P(A) > 0$. The conditional probability of $B$ given $A$ is
>$$P(B|A) = \frac{P(A \cap B)}{P(A)}$$

>[!tips] 1.4 Independence
>Two events $A$ and $B$ are independent if $P(A \cap B) = P(A)P(B)$.
>Events $A_1, ..., A_n$ are mutually independent if for every subcollection, the probability of the intersection is the product of the individual probabilities.

>[!tips] 1.5 Random Variable
>A function $X$ that assigns to each element $c \in \mathcal{C}$ one and only one number $X(c) = x$ is called a random variable. The space or range of $X$ is $\mathcal{D} = \{x : x = X(c), c \in \mathcal{C}\}$.

>[!tips] 1.5 Cumulative Distribution Function (cdf)
>The cumulative distribution function of a random variable $X$ is defined by
>$$F_X(x) = P(X \le x) = P(\{c \in \mathcal{C} : X(c) \le x\})$$

>[!tips] 1.6 Discrete Random Variable
>A random variable is discrete if its space is either finite or countable.

>[!tips] 1.6 Probability Mass Function (pmf)
>For a discrete random variable $X$, the pmf is given by $p_X(x) = P[X=x]$ for $x \in \mathcal{D}$.
>Properties: $0 \le p_X(x) \le 1$ and $\sum_{x \in \mathcal{D}} p_X(x) = 1$.

>[!tips] 1.7 Continuous Random Variable
>A random variable is continuous if its cdf $F_X(x)$ is a continuous function for all $x \in \mathbb{R}$.

>[!tips] 1.7 Probability Density Function (pdf)
>For a continuous random variable $X$, the pdf $f_X(x)$ satisfies
>$$F_X(x) = \int_{-\infty}^x f_X(t) dt$$
>and, where differentiable, $f_X(x) = \frac{d}{dx}F_X(x)$.

>[!tips] 1.7 Quantile (Percentile)
>For $0 < p < 1$, the quantile of order $p$ (or $(100p)$th percentile) is a value $\xi_p$ such that $P(X < \xi_p) \le p$ and $P(X \le \xi_p) \ge p$.
>For continuous cases: $\xi_p = F_X^{-1}(p)$.

>[!tips] 1.9 Mean
>The mean value (or expected value) of $X$ is $\mu = E(X)$.
>Discrete: $\mu = \sum_{x} x p(x)$.
>Continuous: $\mu = \int_{-\infty}^{\infty} x f(x) dx$.

>[!tips] 1.9 Variance and Standard Deviation
>The variance of $X$ is $\sigma^2 = E[(X - \mu)^2] = E(X^2) - \mu^2$.
>The standard deviation is $\sigma = \sqrt{\sigma^2}$.

>[!tips] 1.9 Moment Generating Function (mgf)
>The mgf of $X$ is $M(t) = E(e^{tX})$ for $-h < t < h$ ($h > 0$).
>$M(t)$ uniquely determines the distribution.
>$$M'(0) = \mu, \quad M''(0) = E(X^2)$$