1. Find a parametrization $r(t)$ of the curve $C$ you're trying to integrate over, and the interval $[a;b]$ over which this parameter is integrated
2. Take the derivative $r'(t)$ of the curve
3. Substitute the parameters of the curve into your vector field: $f(x,y)\implies f(r(t))$
4. Take the dot product of $r'(t)$ and $f(r(t))$ to get the value of the vector field over a short section of your curve:
5. Take the integral of $f(r(t))\cdot r'(t)$ over the interval of the curve you're interested in: $\int_{a}^{b} f(r(t))\cdot r'(t) \, dt$

![[Line_integral_of_scalar_field.gif]]

***
## Example 1

We have a vector field $\vec{F}=xy\hat{\mathbf{x}}-y^{2}\hat{\mathbf{y}}$, and we want to find its sum over the curve $y=2x^{2}$ from $(0,0)$ to $(1,2)$.

1. We write the curve as $\vec{r}=(x,2x^{2})$ since $x=x$ and $y=2x^{2}$
2. We take its derivative with respect to $x$: $\vec{r}'=(1,4x)dx$
3. We rewrite the vector field using the parameters of our curve: $\vec{F}=(2x^{3},-4x^{4})$
4. We take the dot product: $\vec{F}\cdot \vec{r}'=2x^{3}dx-16x^{5}dx$
5. Notice that when parametrizing the curve, we wrote everything in terms of $x$, so we are interested now in only the variation of $x$ from $0<x<1$: $\int_{0}^{1} (2x^{3}-16x^{5}) \, dx=-\frac{13}{6}$
Therefore the sum of the vector field $\vec{F}$ over the parabola $y=2x^{2}$ is $-\frac{13}{6}$.
## Example 2
