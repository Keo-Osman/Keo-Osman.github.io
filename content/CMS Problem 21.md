#Questions/Maths 

![[CMS-21.png|750]]
**i)** First consider the triangle $CDE$ where $C$ is the centre of $A$ and $D,E$ are the centres of 2 of the smaller circles. We know that $DE = 2$ since it is 2 radii long and $CD=CE=r+1$ so by the cosine rule (using $DE = a = 2$, $CD = b = c = r+1$ we get 


$$
\cos A = \frac{(r+1)^2+(r+1)^2-2^2}{2(r+1)(r+1)} = 1-\frac{2}{(r+1)^2}
$$



Since the number of circles $n$ is $\displaystyle \frac{360}{A}$ *as the triangles formed by centres of smaller circle are equal and cut the larger circle into equal sections* we get 


$$
n = \frac{360}{\cos^{-1}\left(1-\displaystyle\frac{2}{(r+1)^2}\right)}
$$



rearranging for $r$ we get 


$$
r = \sqrt{\frac{2}{1-\cos\displaystyle\frac{360}{n}}}-1
$$




---
**ii)** The area of $B$ is $\pi(r+2)^2$ and the combined area of the circles is $n\pi$ therefore $F = \displaystyle\frac{n}{(r+2)^2}$ rearranging we get $r = \displaystyle\sqrt{\displaystyle\frac{n}{F}} - 2$ plugging in the expression for n we found earlier we get 


$$
r = \left(\sqrt{\displaystyle\frac{\displaystyle\frac{360}{\cos^{-1}\left(1-\displaystyle\frac{2}{(r+1)^2}\right)}}{2412-984\sqrt{6}-1392\sqrt{3}+1704\sqrt{2}}}\right)-2
$$



After iterating we get $r \approx 2.837$ which by plugging into our equation for n yields $n = 11.999...$ since $n$ has to be an integer we can conclude that $n = 12$ plugging this back into the equation for $r$ and simplifying we get the exact value for $r = \sqrt{2} + \sqrt{6} - 1$ 