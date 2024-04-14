# Evolutionary Game Theory

Evolutionary game theory is a branch of game theory that studies the evolution of strategies in biological populations over time. It applies concepts from biology, mathematics, and economics to understand how behaviors evolve through natural selection.

## Evolutionary Games

Evolutionary games model strategic interactions among individuals in a population, where strategies are represented by different behaviors or actions. These games typically involve a set of players, each choosing a strategy, and receiving payoffs based on the interactions with other players.

### Replicator Dynamics

Replicator dynamics describe the change in the frequency of strategies over time within a population. It is a key concept in evolutionary game theory and is often used to model the evolution of strategies based on their relative success or fitness.

Mathematically, replicator dynamics can be represented by the following equation for a strategy $i$:

$$
\frac{dx_i}{dt} = x_i (u_i(x) - \bar{u}(x))
$$

Where:
- $\frac{dx_i}{dt}$ is the change in the frequency of strategy i in between consecutive generations
- $x_i$ is the frequency of strategy $i$ in the population.
- $u_i(x)$ is the average payoff of strategy $i$ against the population's current composition $x$.
- $\bar{u}(x)$ is the average payoff of the population against itself.

### Evolutionary Stable Strategies (ESS)

An evolutionary stable strategy is a strategy that, if adopted by a population, cannot be invaded by any alternative strategy that is initially rare. ESS represents a stable equilibrium point in the evolution of strategies within a population.

Mathematically, a strategy $s$ is an ESS if:

$$
\forall s' \neq s: \bar{u}(s, s) > \bar{u}(s', s)
$$

Where $\bar{u}(s, s)$ represents the average payoff of strategy $s$ against itself.

## Common Games 

-   ### [Hawk-Dove Game](https://github.com/AnshulJawale/hawk_dove.ipynb)

    The Hawk-Dove game models conflict over a resource, where individuals can choose to be aggressive (Hawk) or passive (Dove). The payoff matrix is typically:

    $$
    \begin{array}{|c|c|c|}
    \hline
    & \text{Hawk} & \text{Dove} \\
    \hline
    \text{Hawk} & (V/2 - C, V/2 - C) & (V, 0) \\
    \hline
    \text{Dove} & (0, V) & (V/2, V/2) \\
    \hline
    \end{array}
    $$

    Where:
    - $V$ represents the value of the resource.
    - $C$ represents the cost of engaging in conflict.



## TODO Next

Other games involved in evolutionary game theory : the War of Attrition, Prisoner's Dilemma, Iterated Prisoner's Dilemma, selfish gene game. (and their simulations in python maybe)
