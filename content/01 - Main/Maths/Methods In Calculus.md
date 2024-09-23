# A-Level Further Pure 1

## Leibnitz's Theorem and nth Derivatives

For $y=uv$

$$
\\frac{d^n y}{dx^n} = \sum_{k=0}^n \binom{n}{k} \frac{d^k u}{dx^k} \frac{d^{n-k} v}{dx^{n-k}}
$$

(This can be proved with induction with repeated differentiation)

## L'Hôpital's Rule

If either:

* $\displaystyle \lim\_{x \to a} f(x) = \lim\_{x \to a} g(x) = 0$
* $\displaystyle \lim\_{x \to a} f(x) = \pm \infty$ & $\displaystyle \lim\_{x \to a} g(x) = \pm \infty$
  Then:
  $$
  \\lim\_{x \to a} \frac{f(x)}{g(x)} = \frac{f'(x)}{g'(x)} \quad \text{(provided that } \lim\_{x \to a} \frac{f(x)}{g(x)} \text{ exists)}
  $$
  You can also use the following rule in conjunction to evaluate more limits:
* If $\displaystyle \lim\_{x \to a} f(x)$ exists, then $\displaystyle \lim\_{x \to a} e^{f(x)} = e^{\left( \displaystyle \lim\_{x \to a} f(x)\right)}$

