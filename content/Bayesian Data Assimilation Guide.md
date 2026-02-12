This guide isn't complete yet I will keep updating it adding new information about the other filters/techniques and maybe expand on what I've already done but for now this should be enough to get you up to understanding the problem and the Kalman filter in the linear all gaussian case as well as ensemble Kalman filter.

I will also add more on the linear Kalman filter soon by deriving a second way *(by leading with the assumption we have a linear update and minimising variance)* this will make the Kalman filter more natural as it might seem like more of an algebraic coincidence rather than the natural way to go about things. This proof doesn't use Bayes' theorem but still arrives at the exact same formulae.

# The Problem We are Trying to Solve
We are trying to model a *dynamic* system - a system that evolves over time. This could be anything really, such as the weather, some position and velocity of an object, a population over time, volatility of a stock. Just anything that *changes over time*. We are looking specifically at dynamic systems that are governed by/can be modelled with *differential equations*. We might look at non differential equation systems that use a *state transition matrix*

The problem is that we don't know the initial state of the system exactly. But we can make observations/measurements however our observations aren't exact, they have error/noise. (*This could be due to a sensor only having finite precision.*) So we can't completely trust our measurements and if we are slightly off this error can compound over time as we make predictions and could become wildly off from the true value. 

Another problem that we have to deal with is that our model may not be perfect. Even if we did know the **exact** state of the system at some point our model might not be able to perfectly predict the true value and again this error may compound over time. This could be due to the fact there are external conditions we can't account for or that the system is too complicated to model every single part so we simplify a bit. E.g. we can't model every single particle in a system. It is too complicated to deal with, we don't have enough computation power and we can't make measurements of the whole system.

# The Solution / Core Loop of Bayesian Data Assimilation
Instead of the model making predictions of the single value of the state. 
We model the state as a *random variable* and keep track of the *probability distribution*. That is instead of predicting that the current state of the system is a specific value we talk about what the probability that the true state value falls within some region is. And we take the mean of this distribution to be our guess for the true state. This also allows us to model how confident we are in the guess.

The two core functions of any model is
1. How we take our current distribution estimate and get a new distribution of the state at some later time.
2. When we receive an observation of the state (may not be of every variable we are trying to model), How do we update a distribution. *To what extent do we prefer either the noisy observation or our noisy prediction more? How do we combine these two to get a more accurate prediction of the state?*

# Prerequisites
## Brief Note on Vectors, Matrices and Linear Algebra
### Vectors
The system that we are trying to model will have more than 1 variable. Instead of treating them as separate variables we group together as a *vector*. However a vector is not "something with direction and magnitude". This only applies to certain *vector spaces* that have geometric meaning but vectors are not inherently geometric objects. In the case of our project the vectors we are dealing with are just the most natural mathematical way to group things and they do not have any geometric meaning/properties unless specified.

The definition of a vector is much more abstract but really it boils down to if something can be added together and multiplied by a scalar (vector times vector multiplication is not required). Many different mathematical objects such as functions can be vectors. A *vector space* refers to a whole set of vectors but don't worry too much about the details of this.
For the purpose of the project a vector we will only be talking about vectors in $\mathbb{R}^{n}$ so they can be thought of as simply a list of real numbers. In code this will simply be a 1D array of floats *(more specifically an `np.array`)* And the *dimension* of the vector is just the length of the list. The set of $n$ dimensional vectors is denoted as $\mathbb{R}^{n}$. For a vector $\mathbf{x}$ with 5 variables we can say that $\mathbf{x}  \in \mathbb{R}^{5}$.
### Matrices
Matrices are a two dimensional grid of numbers *(The actual definition is a bit more abstract than this but this definition is enough for the project)*. Generally this grid is a square but can be non-square although those only come up very briefly in the project with the *observation map*. We can have an $m\times n$ matrix ($m$ rows, $n$ columns) and we denote the set of these matrices as $\mathbb{R}^{m\times n}$. *However* $\mathbb{R}^{m\times n} \not\equiv \mathbb{R}^{n\times m}$. It is also not an actual multiplication in the *"exponent"*. $\mathbb{R}^{3\times 5} \not\equiv \mathbb{R}^{15}$. *Although they are isomorphic*.
However it is often better to think of a matrix as a list of vectors. An $m\times n$ matrix can either be interpreted as $m$ different $n$ dimensional *row* vectors or $n$ different $m$ dimensional *column* vectors.
In code this will be a 2D array of floats again more specifically an `np.array`.

In this project matrices are used for three purposes
1. As a function on vectors - focus on column vectors.
2. A way to represent systems of equations - focus on row vectors.
3. The covariance matrix - just a grid of numbers. It's matrix properties and the properties of it's row and column vectors aren't really relevant.

For the project knowing much about matrices as functions or systems of equations isn't too vital but it is helpful in some cases. The most common occurrence of matrices is the covariance. Matrices as functions on vectors comes up quite a bit as the *state transition matrix* but depending on the system we are modelling it is not always possible. Representing systems of equations with matrices is only applicable with a very specific type of equation system and for most cases won't work.
### *"Linear"*
The word linear will come up a few times in this project. This does not refer to a linear polynomial $y=mx +c$. It refers to a linear function which is a function $f: V\to W$ ($V, W$ are vector spaces) that satisfies
1. $f(x+y) = f(x)+f(y), \quad\forall x, y \in V$
2. $f(cx) = cf(x), \quad\forall x \in V, c \in \mathbb{R}$
This definition isn't really important all you really need to know is that linear refers to a *"nice"* type of function that can be represented as a matrix. 
If a linear function's domain and codomain are the same vector space. Such as $f: \mathbb{R}^{3}\to \mathbb{R}^{3}$ then $f$ is a ***linear transform***

Annoyingly $f(x) = mx + c, c \neq0$ isn't actually linear with this definition it's *affine*. But don't really worry about this.
### Matrices as functions
I won't go into too much detail as it's not really necessary but matrices are *linear transforms* on vectors. Because of the properties of linear functions they can be determined, by where the *basis vectors* end up after the transformation. For $\mathbb{R}^{n}$ these are the unit vectors $\begin{pmatrix}1 \\ 0 \\ \vdots \\ 0\end{pmatrix}, \begin{pmatrix}0 \\ 1 \\ \vdots \\ 0\end{pmatrix},\dots,\begin{pmatrix}0 \\ 0 \\ \vdots \\ 1\end{pmatrix}$
A matrices column vectors are where each of the basis vectors end up after the transform.
Matrix-Vector multiplication is how these functions are applied. E.g. $A \in \mathbb{R}^{n \times n}, \mathbf{v} \in \mathbb{R}^{n}$ then $A\mathbf{v}$ is the result of applying the linear transform $A$ on the vector $\mathbf{v}$. And matrix multiplication is function composition so if $A \in \mathbb{R}^{n \times n}, B \in \mathbb{R}^{n \times n}$ then $AB$ is a new matrix and is the composition of functions of $A, B$. Like regular functional composition it is read right to left. We apply $B$ first then $A$.

### Matrices as Systems of Equations
The linear system of equations:

$$
\begin{aligned} a_{1}x + b_{1}y + c_{1}z& = v_{1} \\
a_{2}x + b_{2}y + c_{2}z& = v_{2} \\ 
a_{3}x + b_{3}y + c_{3}z& = v_{3}
\end{aligned}
$$

Is equivalent to this matrix equation

$$
\begin{aligned}
\begin{pmatrix} a_{1} & b_{1} & c_{1} \\ a_{2} & b_{2} & c_{2} \\ a_{3} & b_{3} & c_{3} \end{pmatrix} \begin{pmatrix} x \\ y \\ z \end{pmatrix} &= \begin{pmatrix} v_{1} \\ v_{2} \\ v_{3} 
\end{pmatrix} 
\\
\end{aligned}
$$

Notice how we have just taken each row of coefficients and put the as a row vector.
If we have a linear system of equations $A\mathbf{x} = \mathbf{v}$ we can solve it by *inverting* the matrix. to get $\mathbf{x}=A^{-1}\mathbf{v}$. inverting a matrix by hand is complicated but you don't need to worry about it in code it can be done with `np.linalg.solve(A, np.eye(len(A))`, `np.linalg.inv(A)`, or `np.linalg.pinv(A)`.
Solve has the best performance and stability so use that unless you have reason to use something different.

## Differential Equations
There are different types: Ordinary differential equations (ODEs), Partial (PDEs) and stochastic (SDEs). We will mainly be looking at ODEs for now.
An ODE is an equation consisting of derivatives (and higher order derivatives e.g. second and third derivative - *however I haven't dealt with any of these in the context of Bayesian data assimilation yet*)
If we have an ODE in multiple variables such as the Lorenz equations 
$$
\begin{aligned}\frac{dx}{dt}&=\sigma(y-x)\\\frac{dy}{dt}&=x(\rho-z)-y\\\frac{dz}{dt}&=xy-\beta z\end{aligned}
$$

We can group the variables into a vector $\mathbf{v} = \begin{pmatrix}x \\ y \\ z\end{pmatrix}$ and write the equation as 
$$
\frac{d\mathbf{v}}{dt} = \mathbf{f}(\mathbf{v}, t)
$$
 where $f$ is a vector function e.g. $f:\mathbb{R}^{3}\to\mathbb{R}^{3}$ 
$$
f\begin{pmatrix}
x \\
y \\
z
\end{pmatrix} = \begin{pmatrix}
\sigma(y-x) \\
x(\rho - z) - y \\
xy-\beta z
\end{pmatrix}
$$

And if the set of equations is *linear* then we can write the function as a matrix and get $\frac{d\mathbf{v}}{dt} = A\mathbf{v}$.

For the project we won't really be solving ODEs analytically (exactly) we will be using approximations using methods like Euler's method or RK4.

## Continuous Random Variables
I've copied all of the following from my previous notes. You don't need to learn all of this in detail you just need to understand at a high level what a probability distribution is and what variance/covariance is for both single and multiple variables. We don't really care about actual probabilities (using integrals) we just care about the *distribution*. 

### Definition
A continuous random variable is a random variable $X$ which can take any real value in an interval. For continuous random variables $\mathbb{P}(X=x) = 0 , \forall x \in \mathbb{R}$. Instead probabilities are defined over an interval e.g. for $a<b \in \mathbb{R}$ we consider $\mathbb{P}(a\leq x\leq b)$.

### Probability Density Function
In order to do this we have a ***probability density*** function $f_{X}(x)$ which satisfies
1. $f_{X}(x) \geq 0$
2. $\int_{a}^{b}f_{X}(x)dx = \mathbb{P}(a\leq x \leq b)$
3. $\int_{-\infty}^{\infty}f_{X}(x)dx = \mathbb{P}(\infty\leq x \leq \infty) = 1$ *as total probability sums to $1$

### Expected Value
The ***Expected Value*** denoted $\mathbb{E}[X]$ of $X$ is the mean value of $X$.
It is defined/found as 
$$
\int_{-\infty}^{\infty}xf_{X}(x)dx
$$

This comes from a generalisation of the discrete case $\mathbb{E}[X] = \sum x\mathbb{P}(X=x)$.

### Variance
***Variance*** is defined as 
$$
\operatorname{Var}(X):=\mathbb{E}[(X-\mathbb{E}[X])^{2}]=\mathbb{E}[X^{2}]-(\mathbb{E}[X])^{2}
$$

Since $\mathbb{E}[X]$ is the mean, $X-\mathbb{E}[X]$ is the deviation of $X$ from the mean. So variance is the *mean squared distance of $X$ from the mean*. It is a measure of **Spread** of the variable/data.

It has the properties that:
1. $\operatorname{Var}(X)\geq0, \operatorname{Var}(X) = 0 \iff X=c$.
2. Weight larger deviations more than small ones. *Hence the squaring.*

We then define standard deviation as 
$$
\sigma = \sqrt{\operatorname{Var(X)} }
$$

To go from squared distance to distance to get spread in the original units. *However it is **NOT** quite the average distance*. But we use it over $\mathbb{E}[\ |X-\mathbb{E}[X]| \ ]$ as the standard deviation has some nicer properties.

### Dealing with Multiple Random Variables
When we have multiple random variables we consider it as a vector in $\mathbb{R}^{n}$. E.g. $\mathbf{X} = (X_{1}, X_{2}, \dots, X_{n}) \in \mathbb{R}^{n}$. We can consider how individual variables in $\mathbf{X}$ are distributed by just consider $X_{i}$ as a single continuous random variable.
But also many concepts generalise nicely to $n$ variables at once.

#### Joint Probability Density Function
Again we don't really care about actual probabilities or the integral that much but for the sake understanding of how distributions work over a vector/multiple variables and completion:
A ***Joint Probability Density Function*** is 
$$
f_{\mathbf{X}}(\mathbf{X}): \mathbb{R}^{n} \to \mathbb{R}, \quad f_{\mathbf{X}}\geq0
$$
 Where 
$$
\forall A\subset \mathbb{R}^{n},\ \mathbb{P}(\mathbf{X}\in A) = \int_{A}f_{\mathbf{X}}(\mathbf{x})d\mathbf{x}
$$

This $\int_{A}$ means to integrate over a region/volume. Basically it takes the case of an integral finding an *area* under a curve over a *range* and generalises it to finding the $n$-dimensional volume over a *region*. 
Thinking of it too geometrically isn't really helpful here though. It is just a generalisation of the idea that we can't assign individual probabilities for a continuous variable and we have to talk the probability that the variable lies within a given regions. Here a *region* is just the generalisation of a range into $n$ variables. 

## Bayes Theorem

$$
P(A|B) = \frac{P(B|A)P(A)}{P(B)}
$$

**Terminology**
1. $P(A)$ is called the ***Prior***. This is what our current belief/hypothesis is about $A$ is *before* we see the data/evidence. It is our starting point.
2. $P(B|A)$ is called the ***Likelihood***. It is the probability of observing the evidence if our hypothesis was true. Effectively it measures how well our hypothesis/current beliefs are *compatible* with the evidence $B$ we just observed.
3. $P(B)$ is called the ***Evidence*** *or* ***Marginal Likelihood***. This is the probability of observing $B$ across *all* possible hypotheses. It serves as a normalisation constant. 
4. $P(A|B)$ is called the ***Posterior***. This is our updated belief in our hypothesis $A$ *after* accounting for the new evidence $B$.

*Note*
Often Bayes' Theorem is written as $\text{Posterior} \propto\text{Likelihood}\times\text{Prior}$ and we leave out the normalisation factor $P(B)$ (*the evidence*). As it is often hard to compute as well as the fact that we don't have to compute it if we have *conjugacy* that is the posterior PDF is in the same *family* as the prior PDF but just with new parameter values.

This theorem is the case for having one specific event but it can be easily generalised for a full probability distribution by replacing all the probability functions $P$ with a distribution $p$. *(Continuous distributions are always denoted by a lowercase $p$)*.

Bayes theorem allows us to take our current belief about the state and when we make a new observation update our distribution to be more accurate according to the observation we just made.

## Normal Distribution
The normal distribution is the most common distribution in the project. Don't worry about knowing the actual function for it. All you need to know is that it is symmetric at the mean and the probability density exponentially decays as you move further from the mean. The (co)variance controls how fast this decays.
It works with multiple variables using vectors and a covariance matrix. It is a very simple distribution that comes up all the time in the real world.
A key property that makes it useful in this context is that applying a *linear (or affine) transform* to a normal distribution you get another normal distribution.
It is denoted as $\mathcal{N}(\mu, \Sigma)$ where $\mu$ is the mean and $\Sigma$ is the covariance matrix. If we are only dealing with one variable then the variance is the standard deviation squared so we write $\mathcal{N}(\mu, \sigma^{2})$
If we want the actual value (probability density) at a specific point we can write $\mathcal{N}(x;\mu,\Sigma )$ basically $x$ is the value we are plugging into the function $\mu, \Sigma$ are the parameters and the semi-colon just serves to separate them making it clear which is which.
The normal distribution is often called a *Gaussian*. These are the exact same things.


***
# Setup and Notation
## Model Equation
The state vector will be denoted $\mathbf{x}$ and $\mathbf{x}_{t}$ is the state vector at time $t$. Remember this is a ***random variable*** not a single value. The amount of variables/the state dimension is $n$.

We will have a model that takes in the previous state and predicts the next state 
$$
\mathbf{x}_{t+1}=f(\mathbf{x}_{t})+\mathbf{w}_{t}, \quad f:\mathbb{R}^{n}\to \mathbb{R}^{n}, \ \mathbf{w}_{t}\sim\mathcal{N}(0, Q)
$$

$\mathbf{x}_{t+1}, \mathbf{x}_{t}, \mathbf{w}_{t}$ are all random variables here. $f(\mathbf{x}_{t})$ is the function that predicts the next state given the current one. This also makes a key assumption called the a *Markov Assumption* which is $p(\mathbf{x}_{t+1}|\mathbf{x}_{0:t})=p(\mathbf{x}_{t+1}|\mathbf{x}_{t})$. This means that the next state is only dependant on the previous state and nothing else.

The $+\mathbf{w}_{t}$ term is a zero-mean gaussian. It doesn't affect the mean of $\mathbf{x}_{t+1}$ it serves as a term to spread out the distribution of $\mathbf{x}_{t+1}$ as the model may not be perfect so after each model step we may want to increase the variance on our guess to represent growing uncertainty. 
*If you want to set model uncertainty to zero you should instead make it really small e.g. `Q = 1e-7 * np.eye(NUM_VARIABLES) * TIME_STEP` as making it zero can cause errors*

*When modelling ODEs with discrete steps, $Q$ is timestep dependant so in code you should  have `Q=... * TIME_STEP`* 

You can also think of this equation as telling us that for a ***fixed*** $\mathbf{x}_{t}$, $\mathbf{x}_{t+1}$ is modelled by a normal with mean $f(x)$ and the variance $Q$ which is the variance we get each model step due to model limitations. This can also be written as $\mathbf{x}_{t+1}|\mathbf{x}_{t} \sim \mathcal{N}(f(\mathbf{x}_{t}), Q)$. This just means that the probability distribution of $\mathbf{x}_{t+1}$ given a *fixed* $\mathbf{x}_{t}$ is modelled by this normal.

Just for extra detail: If we explicitly want to get our new distribution we use  the Chapman-Kolmogorov equation *(Only valid under Markov Assumption)* 
$$
p(\mathbf{x}_{t+1})=\int \mathcal{N}(\mathbf{x}_{t+1};f(\mathbf{x}_{t}), Q)p(\mathbf{x}_{t})d\mathbf{x}_{t}
$$

This is a generalisation of the discrete case $P(A) = \Sigma P(A|B)P(B)$ Basically, across all possible $B$, sum $P(A|B)$ weighted by the probability of $B$ actually occurring. Replacing $P(A) \to p(\mathbf{x}_{t+1}), P(B)\to p(\mathbf{x}_{t}), P(A|B)\to p(\mathbf{x}_{t+1}|x_{t})=\mathcal{N}(\mathbf{x}_{t+1};f(\mathbf{x}_{t}), Q)$ and replacing the discrete sum with an integral gets us the exact same form as above. 

We almost never actually use this integral directly. We either use it implicitly *(like with linear Kalman)* or approximate it directly or indirectly with *Monte-Carlo sampling* in Ensemble Kalman Filter.

## Observations
Don't worry about this too much but:
When we make observations about the state we write it as 
$$
\mathbf{z}_{t}=\mathcal{H}(\mathbf{x}_{t})+\mathbf{v}_{t}, \quad \mathbf{v}_{t}\sim\mathcal{N}(0, R_{t})
$$

Similar intuition with what the equation actually represents than with the model equation. However even though $\mathbf{z}_{t}$ is a random variable we only get a single value for it when we observe it.

The $\mathcal{N}(0, R)$ just represents the noise in our measurements. $\mathcal{H}$ is the observation map and it tells us given a true state $\mathbf{x}_{t}$ what vector we actually measure. It can be non-linear but for now we will assume that we can either observe a variable directly or not observe at all. *(In more complex cases you can only observe a non-linear transformed version of the variable)*. So $H$ is a linear function and is therefore a matrix (although generally non-square. *(We now denote it with a regular $H$ as it is a matrix)*. 
All you need to know about it, is that when we can't measure all variables we and we want to perform an update step we need to *map our state into the observation space*. Basically we apply $H$ and now we have a vector that is the same format/of the same variables as the measurement and now we can perform calculations between our observation and current state guess.
***
# Kalman Filter
The Kalman Filter is a subset of Bayesian Data Assimilation but it covers both propagating our distribution through the model and the update step with Bayes'. It is enough on it's own to work for the project. We can also look at particle filters, which replace Kalman Filters. Or 4D variational methods which can be built on top of Kalman Filters *(although I don't really know anything about this).*

There are many variations on the Kalman filter: Extended, unscented, ensemble etc... They achieve the exact same thing as a regular Kalman filter but they deal with more complex cases and different assumptions e.g. non-linear models and/or non-gaussian distributions. They do this in varying different ways.

## Linear Kalman Filter
This is the original Kalman Filter. It assumes that every distribution is gaussian and the model is linear. 

### Propagation
For our model equation we have 
$$
\mathbf{x}_{t+1}=A\mathbf{x}_{t}+\mathbf{w}_{t}, \quad\mathbf{w}_{t} \sim \mathcal{N}(0, Q)
$$

The nice thing about every distribution being gaussian is that if a random variable is modelled by a Gaussian then any **linear** (*or affine*) transformation of that variable will also be modelled by a Gaussian.
So if $\mathbf{x}_{t} \sim \mathcal{N}(\mu, P)$. $P$ *is used to denote our guess covariance*. We can apply a simple formula to get $A\mathbf{x}_{t} \sim \mathcal{N}(A\mu, APA^{\top})$. 
Then we have that $\mathbf{x}_{t+1}\sim \mathcal{N}(A\mu, APA^{\top})+\mathcal{N}(0, Q)$. If we have a random variable being the sum of two independent normally distributed variables then the resultant distribution is a simple gaussian where you add the mean and covariance of each so we have $\mathbf{x}_{t+1}\sim \mathcal{N}(A\mu,APA^{\top}+Q)$. So 

## Update
When we receive an observation. we want to update our distribution with Bayes' theorem in the following form 
$$
p(\mathbf{x}_{t}|\mathbf{z}_{1:t})=\frac{p(\mathbf{z}_{t}|\mathbf{x}_{t})p(\mathbf{x}_{t}|\mathbf{z}_{1:t-1})}{p(\mathbf{z}_{t}|\mathbf{z}_{1:t-1})}
$$

Here the colon in the subscript denotes a list e.g. $a_{1:t} = a_{1}, a_{2}, \dots a_{t}$.
Identifying the 4 key components
1. **Posterior** - $p(\mathbf{x}_{t}|\mathbf{z}_{1:t})$. This is $p(\text{Current State}|\text{All measurements})$ basically updating our distribution on the state to include the information gained by out measurements.
2. **Likelihood** - $p(\mathbf{z}_{t}|\mathbf{x}_{t})$. This is the probability of our measurement if $\mathbf{x}_{t}$ was the real state. Comes directly from the observation model/noise. $\mathbf{z}_{t}=H\mathbf{x}_{t}+\mathbf{v}_{t}, \quad \mathbf{v}_{t}\sim \mathcal{N}(0, R_{t})$. Therefore $\mathbf{z}_{t}|\mathbf{x_{t}}\sim \mathcal{N}(H\mathbf{x}_{t}, R_{t})$
3. **Prior** - $p(\mathbf{x}_{t}|\mathbf{z}_{1:t-1})$. This is the probability distribution we had before seeing the current measurement. It was the result of propagating the posterior at $t-1$ through our model as we saw earlier. Our current belief modelled by $\mathcal{N}(\mu_{t}, P_{t})$
4. **Evidence** - $p(\mathbf{z}_{t}|\mathbf{z}_{1:t-1})$. The probability of observing $\mathbf{z}_{t}$ under the model. *In practice we often don't compute/care about this*.

Substituting in our distributions and ignoring the normalising evidence constant we get 
$$
p(\mathbf{x}_{t}|\mathbf{z}_{1:t})\propto \mathcal{N}(\mathbf{z}_{t};H\mathbf{x}_{t}, R_{t})\mathcal{N}(\mathbf{x}_{t};\mu_{t}^{-}, P_{t}^{-})
$$

The following is lots of algebra, you don't really need to know this but we have an exact formula for the above expression so we can easily find our posterior but for completion here is some proof:
Also note here we are actually multiplying the *probability density functions* here this is ***NOT*** the same as finding the product of two normally distributed variables.
The product of two normals is proportional to a normal so using this fact we don't have to compute this directly and we can use the formula $\mathcal{N}(\mu_{1}, \Sigma_{1})\mathcal{N}(\mu_{2}, \Sigma_{2})\propto\mathcal{N}(\mu_{3}, \Sigma_{3})$ where 

$$
\begin{aligned}
\Sigma_{3} &= (\Sigma_{1}^{-1}+\Sigma_{2}^{-1})^{-1} \\
\mu_{3} &= \Sigma_{3}(\Sigma_{1}^{-1}\mu_{1}+\Sigma_{2}^{-1}\mu_{2})
\end{aligned}
$$

However our two normals are currently in different variables ($\mathbf{x}_{t}$ and $\mathbf{z}_{t}$). But we can get them in the same variable by, instead of viewing $p(\mathbf{z}_{t} | \mathbf{x}_{t})$ as a function in $\mathbf{z}$ for a fixed $\mathbf{x}$, we view it as a function in $\mathbf{x}$ for fixed $\mathbf{z}$. Then with some complicated algebra we get that $p(\mathbf{z}_{t}|\mathbf{x}_{t}) \propto \mathcal{N}(\mathbf{x}_{t};(H^{\top}R_{t}^{-1}H)^{-1}H^{\top}R_t^{-1}\mathbf{z}_{t}, (H^{\top}R_{t}^{-1}H)^{-1})$ so now we have:

$$
\begin{aligned}
\Sigma_{1} &=(H^{\top}R_t ^{-1}H)^{-1}, &&\mu_{1} = \Sigma_{1}H^{\top}R^{-1}_{t}\mathbf{z_{t}}\\
\Sigma_{2} &= P_{t}^{-}, &&\mu_{2}=\mu_{t}^{-}
\end{aligned}
$$
 

Putting this together we get that $P_{t}= ((P_{t}^{-})^{-1} + H^{\top}R_{t}^{-1}H)^{-1}$ and $\mu_{t}=P_{t}(H^{\top}R^{-1}\mathbf{z}_{t}+(P_{t}^{-})^{-1}\mu_{t}^{-})$. So we have a closed formula for the new mean and covariance once we receive an observation.
Here we can do some more algebra and get the following 

$$
\begin{aligned}
\mathbf{y}_{t}&=\mathbf{z}_{t}-H\mu_{t}^{-} \quad &\text{(Innovation)}\\
S &= HP_{t}^{-}H^{\top}+R_{t}\quad &\text{(Innovation Covariance)}\\
K & =P_{t}^{-}H^{\top}S^{-1}\quad &\text{(Kalman Gain)}\\
\mu_{t} & =\mu_{t}^{-}+K\mathbf{y}_{t}\quad &\text{(Posterior Mean)}\\
P_{t} &=(I-KH)P_{t}^{-}\quad &\text{(Posterior Covarainve)}

\end{aligned}
$$


The innovation vector is effectively the error in our prediction. $\text{Innovation}=\text{Observation}-\text{Prediction}$. Since it is the subtraction of two normally distributed variables it is modelled by a normal itself that is $\mathbf{y}_{t}|\mathbf{z}_{1:t-1}\sim \mathcal{N}(0, S)$. *However* we only receive on observation so we only have a single value for it not the whole distribution. We can see $S$ is the sum of two terms $HP_{t}^{-}H^{\top}$ this is our prior uncertainty *(projected into measurement space)* meaning we have uncertainty on what the error is as we are uncertain in our prediction. We also have the $+R_{t}$ term which reflects our observation uncertainty. 
Then we have Kalman gain matrix which is essentially a measure of how much we trust the model vs how much we trust the measurement. This is calculated based on the prior uncertainty covariance and the measurement covariance uncertainty.
And we can update our mean and covariance accordingly. Note that this form with using the Kalman gain is ***algebraically equivalent*** to how we derived it from Bayes'. In this specific case you could get away with using the *"intermediate step"* of the Kalman gain and use the gaussian multiplication formula we found above. However the idea of Kalman gain is used in the other variations of the Kalman filters and it also give nice intuition for how it works. 

This exact formula can also be derived by first assuming that we have a linear update e.g. $\mu_{t}=\mu_{t}^{-}+K\mathbf{y}_{t}$ then we find optimal $K$ by minimising the posterior covariance. 

## Ensemble Kalman Filter
The ensemble Kalman filter is one way to use the Kalman filter we've just derived but with different assumptions. The ensemble filter works with *non-linear* models and since non-linearity do not preserve gaussians our distributions will have to be non-gaussian. However we will still model observation noise and model uncertainty as gaussians it's just that our actual state estimate distribution can't be gaussian.

### Propagate
To get around this instead of transforming a whole distribution. We will take random samples (called particles) from our distribution and now that we have an array consisting of single fixed values (particles) of possible state vectors we will apply our state transition to each of them individually to get a new set of particles.

But since we only have particles we will can only approximate the features of our distribution. Instead of having one mean that we can nicely propagate through the model like in linear Kalman we have an array of particles and we take their mean which is simply a discrete arithmetic mean.

## Update
For the update step we will use the linear Kalman filter like before by treating our distribution as a gaussian. To do this we simply compute the mean and covariance of the particles and then treat our distribution as though it was modelled by a gaussian with that mean and covariance. To actually perform this update we compute the Kalman gain with the exact same formula but using the covariance of the particle distribution as our prior covariance.
Then for each particle $\mathbf{x}_{t}^{(i)-}$ we have 

$$
\mathbf{x}_{t}^{(i)} = \mathbf{x}_{t}^{(i)-} + K_{t}(\mathbf{z}_{t}^{(i)}-H\mathbf{x}_{t}^{(i)})
$$

Here although we have only one measurement $\mathbf{z}_{t}$ we form a whole array of perturbed measurements with $\mathbf{z}_{t}^{(i)} = \mathbf{z}_{t}+\mathbf{w}_{t}^{(i)}, \quad \mathbf{w}_{t}^{(i)}\sim \mathcal{N}(0, R)$. Basically for each particle we add a little bit of noise to the observation we received using the distribution in which we believe observation noise follows. *In this case* $\mathcal{N}(0, R)$. 
The reason we inject this noise is that we would be updating the particles to have the correct mean but we need to have some method for the particle distribution's covariance to increase due to observation covariance so we add random noise to reflect this. Without this there is no way for the ensemble to *"see"* the randomness in the measurements.