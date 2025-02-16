## Measures of Location & Spread

### Quartiles & Percentiles

For discrete Data: ($D_N$ denotes $N^{th}$ data point)
$$
\begin{equation}
Q_1 =
\left\{

\begin{array}{lr}
{\displaystyle \frac{\displaystyle D_{\textstyle \frac{n}{4}}+D_{ \textstyle (\frac{n}{4}+1)}}{2}}, & \text{if }  \frac{n}{4} \in \mathbb{Z} \\

D_{\textstyle\lceil \frac{n}{4}\rceil}, & \text{if } \frac{n}{4} \notin\mathbb{Z}

\end{array}
\right\}
\end{equation}
$$

$$
\begin{equation}
Q_2 =
\left\{

\begin{array}{lr}
\displaystyle \displaystyle D_{\textstyle \frac{n+1}{2}}, & \text{if }  \frac{n+1}{2} \in \mathbb{Z} \\

\displaystyle \frac{D_{\textstyle\lceil \frac{n+1}{2}\rceil }+D_{\textstyle\lfloor \frac{n+1}{2}\rfloor}}{2}, & \text{if } \frac{n+1}{2} \notin\mathbb{Z}

\end{array}
\right\}
\end{equation}
$$

$$
\begin{equation}
Q_3 =
\left\{

\begin{array}{lr}
{\displaystyle \frac{\displaystyle D_{\textstyle \frac{3n}{4}}+D_{ \textstyle (\frac{3n}{4}+1)}}{2}}, & \text{if }  \frac{3n}{4} \in \mathbb{Z} \\

D_{\textstyle\lceil \frac{3n}{4}\rceil}, & \text{if } \frac{3n}{4} \notin\mathbb{Z}

\end{array}
\right\}
\end{equation}
$$

$$P_n \text{ (nth percentile) }: D_{\left(\textstyle\frac{n \times s}{100}\right)}$$

### Variance & Standard Deviation

$$σ^2 = \frac{Σ(x-\bar{x})^2}{n}$$ where $σ^2$ is variance and $σ$ is standard deviation

### Coding

Coding is a function to take data $x$ and translate into a different domain $y$. For A-Level the only coding formula is: $$y = \frac{x-a}{b}$$
This implies:
$$\bar{y} = \frac{\bar{x}-a}{b}$$
$$\displaystyle σ_y = \frac{σ_x}{b}$$


# Flashcards

#z_Legacy/Maths/A-Levels/Stats/Location-And-Spread 

How are $Q_1, Q_2, Q_3, P_n$ calculated
?
$Q_1 = \left\{\begin{array}{lr}{\displaystyle \frac{\displaystyle D_{\textstyle \frac{n}{4}}+D_{ \textstyle (\frac{n}{4}+1)}}{2}}, & \text{if }  \frac{n}{4} \in \mathbb{Z} \\ D_{\textstyle\lceil \frac{n}{4}\rceil}, & \text{if } \frac{n}{4} \notin\mathbb{Z}\end{array}\right\} \quad Q_2 = \left\{\begin{array}{lr}\displaystyle \displaystyle D_{\textstyle \frac{n+1}{2}}, & \text{if }  \frac{n+1}{2} \in \mathbb{Z} \\ \displaystyle \frac{D_{\textstyle\lceil \frac{n+1}{2}\rceil }+D_{\textstyle\lfloor \frac{n+1}{2}\rfloor}}{2}, & \text{if } \frac{n+1}{2} \notin\mathbb{Z}\end{array}\right\} \quad Q_3 = \left\{\begin{array}{lr}{\displaystyle \frac{\displaystyle D_{\textstyle \frac{3n}{4}}+D_{ \textstyle (\frac{3n}{4}+1)}}{2}}, & \text{if }  \frac{3n}{4} \in \mathbb{Z} \\ D_{\textstyle\lceil \frac{3n}{4}\rceil}, & \text{if } \frac{3n}{4} \notin\mathbb{Z}\end{array}\right\} \quad P_n \text{ (nth percentile) }: D_{\left(\textstyle\frac{n \times s}{100}\right)}$ 

How is data coded form $x \rightarrow y$ and what is $\bar y$ and $\sigma_y$
?
Coding is a function to take data $x$ and translate into a different domain $y$. For A-Level the only coding formula is: $$y = \frac{x-a}{b}$$
This implies:
$$\bar{y} = \frac{\bar{x}-a}{b}$$
$$\displaystyle σ_y = \frac{σ_x}{b}$$ 