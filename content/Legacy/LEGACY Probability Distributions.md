A probability distribution fully describes the probability of any outcome in the sample space.

### Binomial Distribution

When you are carrying out a number of trials you can define a random variable $X$ to represent the number of successful trials.

You can model $X$ with a binomial distribution $X∼B(n,p)$ if:

- There are a fixed amount of trials $n$
- There are only 2 possible outcomes
- There is a fixed chance of success $p$
- The trials are independent

For $X∼B(n,p)$: $P(X=r) = \binom{n}{r}p^r(1-p)^{n-r}$ (on Calculator as binomial PD)

### Cumulative Probability

The cumulative probability function for a random variable $X$ tells you $P(X≤x)$ *(For binomial it's Binomial CD)*

**Calculations:**

|   $P(X≤n)$  |  $P(X≤n)$  |
| ---        | ---       |
|  $P(X<n)$   |$P(X≤n-1)$     |
|$P(X≥n)$|$1-P(X≤n-1)$|
|$P(X≥n)$|$1-P(X≤n-1)$|
|$P(X>n)$| $1-P(X≤n)$|

