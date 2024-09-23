# Definition

Conic sections are graphs that are obtained by slicing a cone (with an inverted cone on top) with a plane
![Conic Sections](https://math.libretexts.org/@api/deki/files/3246/CNX_Calc_Figure_11_05_002.jfif?revision=1&size=bestfit&width=843&height=452)

# A-Level Further Pure 1 (Conic Sections 1)

## Parabolas

A parabola is a family of curves that are obtained by slicing a cone with a plane parallel to its slant such as $y = x^2$

Another parabola is $y^2 = 4ax$ or parametrically $x = at^2$, $y = 2at$ for $t \in \mathbb{R}$. This curve is symmetric around the x-axis.

You can also describe a parabola as a locus of points based on a point called the "focus" and a line called the "directrix"

* A parabola is the locus of points P such that $SP = PX$ where S is the focus and X is some arbitrary point on the directrix

For parabola $y^2 = 4ax$:

* The focus S is $(a, 0)$
* The directrix has equation $x + a = 0$
* The vertex (turning point) is $(0, 0)$

## Rectangular Hyperbolas

A rectangular hyperbola is obtained when the slice intersects both nappes (halves) of the cone.

* A hyperbola has 2 sections called branches
* A rectangular hyperbola is a hyperbola such that the asymptotes meet at right angles
* The Cartesian equation is $xy = c^2$
* The parametric equations are $x = ct$, $y = \frac{c}{t}$, $t \neq 0$, $t \in \mathbb{R}$

(This is a specific type of rectangular hyperbola such that the asymptotes are $x=0$  can obtain this by rotating 45° using a rotation matrix on the standard rectangular hyperbola equation)

## Tangents & Normals

* For general parabola $y^2 = 4ax$, the gradient is:

$$\frac{dy}{dx} = \frac{2a}{y}$$

(This can be obtained by parametric or implicit differentiation)

* For hyperbola $xy = c^2$ / $y = \frac{c^2}{x}$:

$$\frac{dy}{dx} = -\frac{c^2}{x^2}$$

To find equation of tangent or normal, use equation:

$$y - y_1 = m_T(x - x_1) \quad , \quad y - y_1 = m_N(x - x_1)$$

where $M_T$ denotes the gradient of a tangent and $M_N$ denotes the gradient of a normal $M_N = -\frac{1}{M_T}$

You can also use the parametric equations for normal & tangent:

For parabola $y^2 = 4ax$ at point $P(at^2, 2at)$:

Normal:
$$y + tx = 2at + at^3$$

Tangent:
$$ty = x + at^2$$

For rectangular hyperbola $xy = c^2$ at point $P(ct, \frac{c}{t})$:

Normal:
$$x + t^2y = 2ct$$

Tangent:
$$t^3x - ty = c(t^4 - 1)$$

# A-Level Further Pure 1 (Conic Sections 2)

## Ellipses

An ellipse is the graph you get from slicing one nappe to get a "closed curve". A circle is a special type of ellipse where the plane is parallel to the cone.
**The standard Cartesian equation is (centred $0,0$)**
$$\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1$$

*When $x = 0$, $\displaystyle  \frac{y^2}{b^2} = 1 \Rightarrow y = \pm b$. When $y = 0$, $\frac{x^2}{a^2} = 1 \Rightarrow x = \pm a$*

**The parametric equations are:**
$$x = a \cos t, y = b \sin t, 0 \leq t < 2\pi$$

## Hyperbolas

$$\frac{x^2}{a^2} - \frac{y^2}{b^2} = 1$$

*When $y = 0$, $x^2 = a^2 \Rightarrow x = \pm a$*

As $x, y \rightarrow \infty$, $\displaystyle  \frac{x^2}{a^2} \approx \frac{y^2}{b^2}$ so the asymptotes are $y = \pm \frac{b}{a}x$
*When $a = b$ this creates rectangular hyperbola with equation $x^2 - y^2 = a^2$ (this is different to $xy = c^2$ as they are the same but just rotated 45° by a linear transform rotation matrix) with asymptotes $y = \pm x$*
**The parametric equations for a standard hyperbola are:**

$$x = \pm a \cosh t, \space y = b \sinh t, t \in \mathbb{R} \quad \text{or }\quad x = a \sec \theta, \space y = b \tan \theta, \space -\pi \leq \theta < \pi, \theta \neq \pm \frac{\pi}{2}$$

## Eccentricity

For all points $P$$ on a conic section, the ratio of the distance P from a fixed point F (the focus) and fixed straight line $D$ (the directrix) is constant. This ratio e is called the eccentricity.

* If $0 \leq e < 1$, P describes an ellipse
* If $e = 1$, P describes a parabola
* If $e > 1$, P describes a hyperbola

### Ellipses

For an ellipse with equation $\displaystyle\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1$, $a > b$:

* Eccentricity, $0 < e < 1$ is given by $b^2 = a^2(1-e^2)$
* The foci at $(\pm ae, 0)$
* The directrices are $\displaystyle  x = \pm \frac{a}{e}$ (ellipses are symmetric)
  *The focus is on the major axis. In this case the x-axis because $a > b$*

For $b > a$:

* Eccentricity is given by $a^2 = b^2(1-e^2)$
* Foci are at $(0, \pm be)$
* Directrices are $\displaystyle y = \pm \frac{b}{e}$

### Hyperbola

For a hyperbola with equation $\displaystyle\frac{x^2}{a^2} - \frac{y^2}{b^2} = 1$:

* Eccentricity $e > 1$ is given by $b^2 = a^2(e^2-1)$
* Foci are at $(\pm ae, 0)$
* Directrices are $\displaystyle x = \pm \frac{a}{e}$

## Tangents & Normals

### Ellipse

The equation of a normal to an ellipse $\displaystyle \frac{x^2}{a^2} + \frac{y^2}{b^2} = 1$ at $P(a \cos t, b \sin t)$ is:

$$ax \sin t - by \cos t = (a^2 - b^2) \cos t \sin t$$

The equation of the tangent at $P(a \cos t, b \sin t)$ is:

$$bx \cos t + ay \sin t = ab$$

You can obtain these results with parametric differentiation any $\displaystyle \frac{dy}{dx} = \frac{dy/dt}{dx/dt}$

### Hyperbolas

For hyperbola $\displaystyle \frac{x^2}{a^2} - \frac{y^2}{b^2} = 1$:

* At $P(a \cosh t, b \sinh t)$ the tangent is $ay \sinh t + bx \cosh t = ab \cosh t$
* At $P(a \sec \theta, b \tan \theta)$ the tangent is $bx \sec \theta - ay \tan \theta = ab$
* At $P(a \cosh t, b \sinh t)$ the normal is $ax \sinh t - by \cosh t = (a^2 + b^2) \sinh t \cosh t$

