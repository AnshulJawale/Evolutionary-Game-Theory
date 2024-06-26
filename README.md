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

It can be said that a strategy $s$ is an ESS if it cannot be invaded by any other strategy $s'$. <br>
Lets say we have a population of only doves. Now if we add a hawk to this population, the hawk will get a higher payoff on average and thus have more chances of replicating than doves. Thus slowly number of doves will go down and hawks will invade the population. Hence the dove strategy can be invaded and is not an ESS. Similiarly the hawk strategy can also be invaded.

## Common Games 
### [Hawk-Dove Game](https://github.com/AnshulJawale/Evolutionary-Game-Theory/blob/main/hawk_dove.ipynb)

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

### [War of Attrition]()

Similiar to a bidding system, the war of attrition is a dynamic timing game in which players choose a time to stop, and fundamentally trade off the strategic gains from outlasting other players and the real costs expended with the passage of time. Each player chooses a time $t$ to give up and look for other resources and the one who stays for the longest time wins resource of value $V$. Utility of player i is given by : 

$$ U_i(t) =
      \begin{cases}
        \dfrac{V}{n} - t       & \quad \text{if } i \text{ wins and }n\text{ is the number of players choosing time }t\\
        -t  & \quad \text{if }i\text{ loses}
      \end{cases}
$$

Where $V$ is value of the resource, $n$ is the number of players with the highest time chosen.

### [Social Behaviour]()

![Social Behaviour](https://upload.wikimedia.org/wikipedia/commons/thumb/e/eb/Game_Theory_Strategic_Social_Alternatives.jpg/450px-Game_Theory_Strategic_Social_Alternatives.jpg)

### [Iterated Prisoners Dilemma](https://github.com/AnshulJawale/Evolutionary-Game-Theory/blob/main/iterated_prisoners_dilemma.ipynb)

The prisoner's dilemma is a game theory thought experiment that involves two rational agents, each of whom can cooperate for mutual benefit or betray their partner ("defect") for individual reward.

#### Axelrod's tournament
  Axelrod's Tournament, proposed by political scientist Robert Axelrod in his book "The Evolution of Cooperation" (1984), is a seminal study in evolutionary game theory. It aimed to explore strategies for cooperation and the emergence of cooperation in repeated prisoner's dilemma interactions.
