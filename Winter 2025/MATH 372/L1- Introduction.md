# The Mathematical Modeling Process

The way we build a model reflects the steps of the scribing scientific process. We have a question based on a real-world problem, simplify reality and limit the number of variables to make a hypothesis and build a mathematical model. We then test the model and analyze our results to arrive at mathematical conclusions, and then we interpret the mathematics to derive a real-world conclusion.

## Fish in a Lake

Say we have a lake with fish. We want to study the population of fish in said lake. This is a vague question, and we should seek to make it for precise. For example, how many fish can be caught every year such that the fish population does not go extinct?

There are still several assumptions here. For example, we might only be considering only one species of fish in our particular lake with specific geographic properties.

Our first task is to find the primary factors involved in the real-world behavior, for example:

- The number of fish.
- Birth and death rates.
- Fishing.
- Nutrient consumption.
- Reproduction.

Here, we can model this problem as a differential equation. Selecting the appropriate model requires experience and familiarity with the relevant literature, and in this class, they will be given.

When writing dawn a mathematical model, it is important to distinguish what parameters are constants and which ones are variables. In this case, a system of ODEs is most suitable. Let $F = F (t)$ be the number of fish and $N = N (t)$ be the total nutrients in the lake at time $t$. We could then name:

- $r$ is the reproduction rate.
- $c$ is the nutrient consumption rate.
- $d$ is the death rate of the fish.
- $\varphi$ is a constant fishing rate.

An equation for $F$ could then be

$$
F' (t)  = rF (t) + cN (t) F (t) - dF (t) - \varphi.
$$

Here, $F$  and $N$  are variables, while the rest are parameters that are fixed for our model. Our question has now become: **What is the maximum number of fish such that $F (t) > 0$ for all time $t$?**.

We have an equation for $F$, but it is clear we still need another equation for $N (t)$ for the system to be complete. We need to add new parameters that affect the nutrient dynamics. We are also missing an initial condition. If we assume that the growth rate and reproduction rate are dependent, which is more realistic, we can replace both $rF (t)$ and $N (t)F (t)$ by $\rho N (t) F (t)$.