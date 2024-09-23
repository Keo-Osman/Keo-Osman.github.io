# A-Level Further Core 1
## Series
- The sum of a constant series $\sum_{r=1}^n m=mn$
- The sum $g$ the first $n$ natural numbers, $\sum_{r=1}^n r=\frac{1}{2} n(n+1)$
- To find a series that doesn't start at one use the formula $$\sum_{r=k}^n f(r)=\sum_{r=1}^n f(r)-\sum_{r=1}^{k-1} f(r)$$
- For more complicated series:
$$
\begin{aligned}
& \sum_{r=1}^n k f(r)= k\sum_{r=1}^n f(r) \\
& \sum_{r=1}^n(f(r)+g(r))=\sum_{r=1}^n f(r)+\sum_{r=1}^n g(r)
\end{aligned}
$$
- The sum of the first $n$ squares $$\sum_{r=1}^n r^2=\frac{1}{6}n(n+1)(2 n+1)$$
- The sum $g$ the first $n$ cubes $$\sum_{r=1}^n r^3=\frac{1}{4} n^2(n+1)^2$$

***

## Flashcards
#Maths/A-Level-Further-Core/Series, #Maths/Topics/Series  

What is the sum of a constant series $\displaystyle\sum_{r=1}^n m$?
?
The sum of a constant series is $\displaystyle\sum_{r=1}^n m=mn$ <!--SR:!2024-10-20,56,310-->

What is the sum of the first $n$ natural numbers?
?
The sum of the first $n$ natural numbers is:
$\displaystyle\sum_{r=1}^n r=\frac{1}{2} n(n+1)$ <!--SR:!2024-10-26,60,310-->

How can you find the sum of a series that doesn't start at one?
?
To find a series that doesn't start at one, use the formula:
$$\sum_{r=k}^n f(r)=\sum_{r=1}^n f(r)-\sum_{r=1}^{k-1} f(r)$$ <!--SR:!2024-09-19,31,290-->

How do you compute $$
\sum_{r=1}^n k f(r)$$
?
$$k\sum_{r=1}^n f(r)$$ <!--SR:!2024-10-26,60,310-->

How do you compute $$\sum_{r=1}^n(f(r)+g(r))$$
?
$$\sum_{r=1}^n f(r)+\sum_{r=1}^n g(r)$$ <!--SR:!2024-10-21,57,310-->

What is the sum of the first $n$ squares?
?
The sum of the first $n$ squares is: $$\sum_{r=1}^n r^2=\frac{1}{6}n(n+1)(2n+1)$$ <!--SR:!2024-09-19,1,210-->

What is the sum of the first $n$ cubes?
?
The sum of the first $n$ cubes is: $$\sum_{r=1}^n r^3=\frac{1}{4} n^2(n+1)^2$$ <!--SR:!2024-09-21,7,250-->

# A-Level Further Core 2
## The method of difference

If the general term of a series can be describes as $u_r = f(r) - f(r+1)$ then $$\sum_{r=1}^{n}{u_r} = f(1) - f(n+1)$$
This is because when summing the $-f(n+1)$ for $n = a$ cancels with the next term’s: $f(n)$ where $n = a+1$ so you get $f(a+1) - f(a+1) = 0$ so every term cancels except the first and last

## Maclaurin Series

- The Maclaurin series of a function is an approximation for a function at x=0. * (many common functions are exactly equal their Maclaurin expansion and are called analytical functions)*
- The Maclaurin series for a function $f(x)$ that is infinitely differentiable at $x = 0$ is given by:

$$f(x) = f(0) + f'(0)x + \frac{f''(0)}{2!}x^2 + \frac{f'''(0)}{3!}x^3 + ...$$

$$= \sum_{n=0}^{\infty} \frac{f^{(n)}(0)}{n!}x^n$$$$\text{where } f^{(n)}(0) \text{ is the }n\text{th derivative of} f(x) \text{ evaluated at } x = 0$$


## Flashcards
#Maths/A-Level-Further-Core/Series, #Maths/Topics/Series

What is the method of difference used for in series?
?
The method of difference is used when we cannot find the general term of the series. We express $u_n = f(n)$ as a difference between two functions to simplify the summation. <!--SR:!2024-10-06,44,290-->

What is the Maclaurin series for a function $f(x)$ that is infinitely differentiable at $x = 0$?
?
$$f(x) = \sum_{n=0}^{\infty} \frac{f^{(n)}(0)}{n!}x^n$$ <!--SR:!2024-10-03,41,290-->