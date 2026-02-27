>[!question] PR 1 25/02/2026
>Show that Dominant Strategy Equilibrium $\implies$ Nash Equilibrium, but the converse is not ture. 

>[!note] [**DSEq**] Dominant Strategy Equilibrium
The strategy $s^*$ is a **dominant strategy** if it is a player’s **strictly best response** to any strategies the other players might pick, in the sense that whatever strategies they pick, his payoff is highest with $s^*$. Mathematically, \
$$ \pi_{i}(s^*_{i},s_{-i})> \pi_{i}(s'_{i},s_{-i}) \quad \forall s_{-i} \quad \forall s'_{i} \neq s^*_{i}$$
**dominant-strategy equilibrium** is a strategy profile consisting of each player’s **dominant strategy**.

>[!note]  [**NashEq**] Nash Equilibrium
>No player has incentive to deviate from his strategy given that the other players do not deviate. Formally, \
>$$\forall i, \quad \pi_{i}(s^*_{i},s^*_{-i})\geq \pi_{i}(s'_{i},s^*_{-i}) \quad \forall s'_{i}$$

>[!success]- Solution
>The converse counter example is in the book. There is a cell which is weak dominant strategy but not **NashEq** by definition
>
>($\implies$) Given a strategy profile $S$ that is **DSEq**, then $S = (s^*_{i},s^*_{-i})$ for some $i$, and each element in $S$ is a **dominant strategy**. We then have \
>$$ \forall i \quad \pi_{i}(s^*_{i},s_{-i})> \pi_{i}(s'_{i},s_{-i}) \quad \forall s_{-i} \quad \forall s'_{i} \neq s^*_{i}$$ 
> Since this condition applies for all $s_{-i}$, it also applies for  $s^*_{{-i}}$ Therefore, 
> $$\forall i, \quad \pi_{i}(s^*_{i},s^*_{-i})\geq \pi_{i}(s'_{i},s^*_{-i}) \quad \forall s'_{i}$$
> Hence, **DSEq** $\implies$ **NashEq** $\blacksquare$

