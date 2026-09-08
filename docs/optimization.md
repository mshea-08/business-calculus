# Optimization

## 7.1 Second Derivative and Concavity 

When we take the derivative of a function, we get back a new function. That means we can repeat the process as many times as we want, resulting in what we call **higher order derivatives**. To denote higher order derivative we can use additional primes. For example, the second derivative of the function $y=f(x)$ can be denoted by $f''(x)$ or $y''$. For much higher order derivatives it is inconvenient to put a bunch of primes, so the order is put in as a superscript in parentheses. For example, the 8-th derivative of $f(x)$ can be denoted as $f^{(8)}(x)$. Parentheses indicate that we mean a derivative *not* a power of the function. In Liebniz notation, the second derivative of $y=f(x)$ is denoted as 

$$\frac{d^2y}{dx^2} \text{ or } \frac{d^2f}{dx^2}.$$

Higher derivatives follow the same pattern. 

!!! example "Example 1"
    Find the second derivative of $y = xe^x$. 

    ??? success "Solution"
        Let's take the first derivative using the product rule, 

        $$y' = e^x + xe^x$$

        Now we differentiate again to find the second derivative. We again should use the product rule on the second term,

        $$y'' = e^x + e^x + xe^x = 2e^x + xe^x$$

!!! example "Example 2"
    Find the second derivative of the function 

    $$f(x) = \frac{1}{x^2-1}$$

    ??? success "Solution"
        Taking the first derivative using the quotient rule gives, 

        $$f'(x) = \frac{-2x}{(x^2-1)^2}$$

        To take the second derivative we need the quotient and the chain rule (for the derivative of the denominator). Note that, 

        $$\frac{d}{dx}(-2x) = -2$$

        and

        $$\frac{d}{dx}((x^2-1)^2) = 2(x^2-1)\cdot 2x = 4x(x^2-1).$$

        So we get,

        $$f''(x) = \frac{(x^2-1)^2\cdot(-2) - (-2x)\cdot4x(x^2-1)}{(x^2-1)^4} = \frac{-2(x^2-1)^2+8x^2(x^2-1)}{(x^2-1)^4}.$$

We learned back in Chapter 5 that the (first) derivative represents the slope of the function. The second derivative tells us about the **concavity** of the function. A graph is **concave up** if the graph bends upwards to make a "cup" shape. The following graphs are all concave up on the visible domain. 

<center>
<iframe src="https://www.desmos.com/calculator/5avn9vmdrd?embed" width="300" height="300" style="border: 1px solid #ccc" frameborder=0></iframe>
<iframe src="https://www.desmos.com/calculator/xuppwinoja?embed" width="300" height="300" style="border: 1px solid #ccc" frameborder=0></iframe>
</center>

A graph is **concave down** if it bends downward to make a "hill" shape. The following graphs are all concave up on the visible domain. 

<center>
<iframe src="https://www.desmos.com/calculator/0uuzgj1ggk?embed" width="300" height="300" style="border: 1px solid #ccc" frameborder=0></iframe>
<iframe src="https://www.desmos.com/calculator/yxmig1qqdh?embed" width="300" height="300" style="border: 1px solid #ccc" frameborder=0></iframe>
</center>

The idea of concavity is nicely explained by looking at graphs, but we should also present a more precise mathematical definition using the second derivative:

- The function $y=f(x)$ is concave up at the point $x=a$ if $f''(a) > 0$. 
- The function $y=f(x)$ is concave down at the point $x=a$ if $f''(a) < 0$. 

If $f''(a) = 0$ or $f''(x)$ is undefined, then it is neither concave down or concave up. Locally it looks like a straight line (horizontal or vertical). If $f''(x)$ switches signs at $x=a$, then we call $a$ an **inflection point**. For example, $x=0$ is an inflection point of the function $y = x^3$. Another way to visualize concavity is to draw a small segment of the tangent line. If it lies below the curve, the curve is concave up. If it lies above the curve, the curve is concave down. Slide the point around below to see how the concavity switches at $x=0$. 

<center>
<iframe src="https://www.desmos.com/calculator/hccssnusfo?embed" width="500" height="500" style="border: 1px solid #ccc" frameborder=0></iframe>
</center>

For $x$ to be an inflection point either $f''(x) = 0$ or $f''(x)$ is undefined. Note that if $f(x)$ is also underfined we do not call $x$ an inflection point. For example, the function $f(x) = 1/x$ does not have an inflection point at $x=0$, since it does not exists.

!!! example "Example 3"
    For which of the following functions $y=f(x)$ does the graph have an inflection point at $x = 0$? a) $f(x) = e^x$, b) $f(x) = x^4$, c) $f(x) = x^{1/3}$.

    ??? success "Solution"
        a) For a point to be an inflection point either $f''(x) = 0$ or $f''(x)$ is undefined. Since $f''(0) = e^0 = 1$, there is no inflection point at $x=0$. 

        b) Since $y''=12x^2$, it is true that $f''(0) = 0$ however there is no change of sign as $f''(x) > 0$ for all other values of $x$. Therefore, $x=0$ is not an inflection point. If we look at the graph, we see a "flattening out" of the function, however the concavity never is down. 

        <center>
        <iframe src="https://www.desmos.com/calculator/vqsgwhrg18?embed" width="400" height="400" style="border: 1px solid #ccc" frameborder=0></iframe>
        </center>

        c) The second derivative is, $f''(x) = -\frac{2}{9}x^{-5/3}$. It is true that $f''(0)$ is undefined, so let's check the sign of the second derivative before and after this point. If $x = 1$, then $f''(1) = -2/9 < 0$. If $x = -1$, then $f''(1) = 2/9 > 0$ (the cube root of a negative number is negative). Therefore, $x=0$ is an inflection point of $y=x^{1/3}$. 

        <center>
        <iframe src="https://www.desmos.com/calculator/3mnz3p0io6?embed" width="400" height="400" style="border: 1px solid #ccc" frameborder=0></iframe>
        </center>


## 7.2 Maxima and Minima of Functions

A functions has a **local maximum** at a point, if that point is higher than all immediate neighbors. For example, The function $y = x^3-2x^2$ has a local maximum at $x=0$. 

<center>
<iframe src="https://www.desmos.com/calculator/fgfxf1gt5c?embed" width="400" height="400" style="border: 1px solid #ccc" frameborder=0></iframe>
</center>

Notice that the graph has a "peak" when $x=0$, although there are other parts of the graph that sit above the point $(0,0)$, for example the point $(3,9)$ is on the graph (but out of the picture). We call a point a **global maximum** if it is higher than all other points in the domain. For example, the point $(0,1)$ is a global maximum of the functions $y = 1-x^2$. 

<center>
<iframe src="https://www.desmos.com/calculator/nrjhpijmnj?embed" width="400" height="400" style="border: 1px solid #ccc" frameborder=0></iframe>
</center>

Implicitly, the domain is all allowed inputs to the function. For the function $y=1-x^2$, this is all real numbers. For the function $y=1/x$ this is all real numbers except zero. We might ask for the global maximum over a *specified* domain, e.g. $0 \leq x \leq 1$. This is often the case in applied settings, which we will investigate later. 

!!! note "Global Versus Local"
    Note that a global maximum is also a local maximum, but the reverse is not necessarily true. 

Similarly, a **local minimum** is a point that is lower than all immediate neighbors and a **global minimum** is the lowest point across the entire domain. We use the term **extrema** to denote both maxima and minima. 

!!! example "Example 4"
    Assume the entire domain of the function is shown in the graph below. Denote all local and global extrema.
    

## 7.3 Applied Optimization

## 7.4 Implicit Differentiation and Related Rates

## Exercises