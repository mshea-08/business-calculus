# Derivative Basics

## 5.1 Derivative Ideas

We learned back in Chapter 1 that linear functions have constant **slope**, which describes the steepness of the line. Other functions we have learned about do not have constant steepness. Take for example the function $f(x) = x^5-2x^4-x^3+2x^2-x$,

<center>
<iframe src="https://www.desmos.com/calculator/fnus02udos?embed" width="400" height="400" style="border: 1px solid #ccc" frameborder=0></iframe>
</center>

The "slope" of the function changes with $x$. When $x \approx 1/2$ the slope negative and not very steep, but when $x \approx 2$ the slope is positive and pretty steep. 

One way to approximate the slope at a point is to use a **secant line** near the point. A secant line is a linear function that intersects a curve at two points. 

Let's consider the quadratic function $f(x) = x^2/10$,

<center>
<iframe src="https://www.desmos.com/calculator/jh6zew4lht?embed" width="400" height="400" style="border: 1px solid #ccc" frameborder=0></iframe>
</center>

We see that as $x$ increases, the slope of the graph becomes steeper. The below graph contains a secant line through the point $(2,f(2)) = (2,0.4)$ and the blue point. You can toggle the blue point along the function to change the look of the secant line. 

<center>
<iframe src="https://www.desmos.com/calculator/pwv9n5ag8v?embed" width="400" height="400" style="border: 1px solid #ccc" frameborder=0></iframe>
</center>

As the second point gets closer to $(2,0.4)$, the slope of the secant line more closely matches the slope of $f(x)$ at $x=2$. What if we kept moving the second point closer and closer to $(2,0.4)$ until it was essentially the same point? This give us what is known as the **tangent line**. We can't yet formally define the tangent line, but broadly it is a line that matches the function at the designated point and has the same slope at the function at that point. 

<center>
<iframe src="https://www.desmos.com/calculator/h5oagssj9e?embed" width="400" height="400" style="border: 1px solid #ccc" frameborder=0></iframe>
</center>

## 5.2 Limits and Continuity

A **limit** is a way for us to mathematically what it means to get closer and closer to a point without truly be equal to it. We write, 

$$\lim_{x \to a} f(x)$$

to mean: What happens to the function $f(x)$ as $x$ gets arbitrarily close to, *but not equal to*, $a$? 
It's important to know that taking a limit is *not the same as* computing the value of the function at that point. In general,

$$\lim_{x\to a} f(x) \neq f(a).$$

One reason limits are interesting is the function may be **undefined** at the point $x=a$. Take for example the function 

$$f(x) = \frac{x^2-1}{x-1}$$

I cannot compute $f(1)$, since the denominator becomes 0, but I can still compute 

$$\lim_{x \to 1} \frac{x^2-1}{x-1} = 2.$$

So as $x \to 1$, the function gets close to the $y$-value $2$. Graphically this looks like, 

<center>
<iframe src="https://www.desmos.com/calculator/pie3tby7gr?embed" width="400" height="400" style="border: 1px solid #ccc" frameborder=0></iframe>
</center>

We use the open hole to signify that the function $f(x)$ does not exist when $x=1$, but it does exist for values arbitrarily close, e.g. for $x=0.9999999987$. Note that Desmos does not identify these **removable discontinuities** when you graph the function. 

Graphically, a limit tells us what happens to the $y$-value of the graph as we approach the $x$-value along the curve of the function. For a limit to exist, the value must be the same regardless of what direction on the line we approach the point from. This allows us to compute limits from the graph of the function.

<center>
<iframe src="https://www.desmos.com/calculator/hmqjrp8dmp?embed" width="400" height="400" style="border: 1px solid #ccc" frameborder=0></iframe>
</center>

Consider the above graph of a function, $f$. Based on the graph, $f(1) = 0$, but it we use the red dot to toggle allong the line, we see that 

$$\lim_{x\to 1} f(x) = 1.$$

!!! example "Example 1"
    Below is a graph of the function $f(x)$. Compute 

    a) $\lim_{x\to 2} f(x)$
    
    b) $\lim_{x\to 1} f(x)$

    c) $\lim_{x\to 0} f(x)$

    <center>
    <iframe src="https://www.desmos.com/calculator/bqi7egfuqh?embed" width="400" height="400" style="border: 1px solid #ccc" frameborder=0></iframe>
    </center>

    ??? success "Solution"

        a) If we follow the line to near when $x = 2$, we see that the $y$-value is near the value $2.5$. Therefore, 

        $$\lim_{x\to 2} f(x) = 2.5$$
        
        b) According to the graph, $f(1) = 1$, however if we actually follow the curve of the graph we find that 

        $$\lim_{x\to 1} f(x) = 0.5$$

        The reality of limits is that we don't care about the value of $f(1)$, we only care about values close to, *but not equal to* $x=1$. 

        c) If we follow the curve of the graph towards $x = 0$ from the left, the $y$-value approaches 0. However, if we follow the curve of the graph towards $x=0$ from the right, the $y$-value approaches $1$. It doesn't matter that $f(0) = 1$, since the $y$-value differs when approaching from the left versus the right, the limit **does not exist**. 

If we can graph the function easily, then the graph serves as an excellent tool for computing limits. An alternative method for computing limits is to use a table of values. This method usually requires a calculator. 

!!! example "Example 2"
    Use a table of values to estimate $\displaystyle\lim_{x \to 2} \frac{x^2 - 4}{x - 2}$.

    ??? success "Solution"
        Note that the function is undefined at $x = 2$ since the denominator is zero. We evaluate the function at values approaching $2$ from both sides,

        | $x$ | $1.9$ | $1.99$ | $1.999$ | $2$ | $2.001$ | $2.01$ | $2.1$ |
        |-----|-------|--------|---------|-----|---------|--------|-------|
        | $f(x)$ | $3.9$ | $3.99$ | $3.999$ | undefined | $4.001$ | $4.01$ | $4.1$ |

        The values approach $4$ from both sides, so we estimate

        $$\lim_{x \to 2} \frac{x^2 - 4}{x - 2} = 4$$

!!! example "Example 3"
    Use a table of values to estimate $\displaystyle\lim_{x \to 0} \frac{e^x - 1}{x}$.

    ??? success "Solution"
        The function is undefined at $x = 0$. We evaluate at values approaching $0$ from both sides,

        | $x$ | $-0.1$ | $-0.01$ | $-0.001$ | $0$ | $0.001$ | $0.01$ | $0.1$ |
        |-----|--------|---------|----------|-----|---------|--------|-------|
        | $f(x)$ | $0.95163$ | $0.99502$ | $0.99950$ | undefined | $1.00050$ | $1.00502$ | $1.05171$ |

        The values approach $1$ from both sides, so we estimate

        $$\lim_{x \to 0} \frac{e^x - 1}{x} = 1$$

In many cases, computing a limit is straightforward and we can simply substitute $x = a$ directly into the function. This works whenever the graph function is "well-behaved" at $x = a$, meaning it is defined there and has no breaks, holes, or jumps nearby. For example,

$$\lim_{x \to 2} 2x - 1 = 2(2) - 1 = 3.$$

Since $f(x) = 2x-1$ is just a line, we know it is well-behaved in the context given above. When direct substitution fails, e.g. when the function is undefined at the point, we need to use algebraic techniques to help simplify the expression. The examples below cover a few common algebraic methods. 

!!! example "Example 4"
    Compute $\displaystyle\lim_{x \to 3} \frac{x^2 - x - 6}{x - 3}$.

    ??? success "Solution"
        The function is undefined at $x = 3$. We factor the numerator,

        $$\lim_{x \to 3} \frac{x^2 - x - 6}{x - 3} = \lim_{x \to 3} \frac{(x-3)(x+2)}{x-3}$$

        Since $x \to 3$ but $x \neq 3$, we can cancel the $(x-3)$ factor,

        $$= \lim_{x \to 3} (x + 2) = 5$$

!!! example "Example 5"
    Compute $\displaystyle\lim_{x \to 3} \frac{\frac{1}{x} - \frac{1}{3}}{x - 3}$.

    ??? success "Solution"
        The function is undefined at $x = 3$. We simplify the numerator by finding a common denominator,

        $$\frac{1}{x} - \frac{1}{3} = \frac{3}{3x} - \frac{x}{3x} = \frac{3 - x}{3x}$$

        Substituting back in,

        $$\lim_{x \to 3} \frac{\frac{3-x}{3x}}{x-3} = \lim_{x \to 3} \frac{3-x}{3x(x-3)}$$

        Notice that $3 - x = -(x-3)$, so we can cancel $(x-3)$,

        $$= \lim_{x \to 3} \frac{-(x-3)}{3x(x-3)} = \lim_{x \to 3} \frac{-1}{3x} = \frac{-1}{3(3)} = -\frac{1}{9}$$

!!! example "Example 6"
    Compute $\displaystyle\lim_{x \to 4} \frac{\sqrt{x} - 2}{x - 4}$.

    ??? success "Solution"
        The function is undefined at $x = 4$. We multiply the numerator and denominator by the conjugate of the numerator, $\sqrt{x} + 2$,

        $$\lim_{x \to 4} \frac{\sqrt{x} - 2}{x - 4} \cdot \frac{\sqrt{x} + 2}{\sqrt{x} + 2} = \lim_{x \to 4} \frac{x - 4}{(x-4)(\sqrt{x} + 2)}$$

        Since $x \neq 4$ we can cancel $(x - 4)$,

        $$= \lim_{x \to 4} \frac{1}{\sqrt{x} + 2} = \frac{1}{\sqrt{4} + 2} = \frac{1}{4}$$

A function is "well-behaved" at $x = a$ if it is **continuous** at $x = a$. A function is continuous if and only if $\lim_{x\to a} f(x) = f(a)$. In layman's terms, a function is continuous (at $a$) if I can draw the graph of the function without needing to lift up my pencil or pen. 


If $\lim_{x \to a} f(x) \neq f(a)$ or either is undefined, we say that $f(x)$ has a **point of discontinuity** or simply that $f(x)$ is **not continuous** at $x = a$. In Chapter 3 we saw **removable discontinuities** (or holes) and **vertical asymptotes** when discussing rational functions. 

- A removable discontinuity occurs when the the limit exists, but the value of the function is different or does not exist. 
- A vertical asymptote occurs when the function value approaches either infinity around the point. 

Below is a depiction of a **jump discontinuity**,

<center>
<iframe src="https://www.desmos.com/calculator/5ikknjrhuy?embed" width="400" height="400" style="border: 1px solid #ccc" frameborder=0></iframe>
</center>

A jump discontinuity occurs when the function approaches different values to the right and left of the point. In the above, when we approach $x=0$ from the left the $y$-value apporach $0$, but if we appraoch from the right the $y$-value approaches 1. 

!!! example "Example 7"
    Determine the points of discontinuity in the graph below, 

    <center>
    <iframe src="https://www.desmos.com/calculator/rh0nrfjhm1?embed" width="400" height="400" style="border: 1px solid #ccc" frameborder=0></iframe>
    </center>

    ??? success "Solution"
        The graph has removable discontinuities at $x = 0$ and $x = 1$. The graph has a jump discontinuity at $x = 2$. 

Polynomial, exponential, and logarithmic functions are continuous for all values in their domain. As we learned in Chapter 3, rational functions may have points of discontinuity. Any piecewise function can have points of discontinuity.  

## 5.3 Derivative at a Point

As we choose points closer and closer to our point of interest, the secant line approaches the tangent line at the point. 

<center>
<iframe src="/secant_slider.html" width="400" height="400" frameborder="0" scrolling="no"></iframe>
</center>

The slope of the tangent line is known as the **instantaneous rate of change** or the **derivative** of $f$ at $a$. The derivative is defined explicitly as a limit. We use the notation $f'(a)$ to denote the derivative of $f$ at $a$. Note that this is just a number. 

$$f'(a) = \lim_{h \to 0} \frac{f(a+h) - f(a)}{h}$$

Note that the quotient 

$$\frac{f(a+h) - f(a)}{h}$$ 

is just the slope of the secant line depicted in the applet above. Taking the limit as $h \to 0$ thus gives us the slope of the tangent line. 

!!! example "Example 8"
    Compute the derivative of the function $f(x) = x^2$ at $x = 1$. 

    ??? success "Solution"
        Using the limit we get, 

        $$f'(1) = \lim_{h\to 0} \frac{(1+h)^2 - 1^2}{h} = \lim_{h\to 0} \frac{1+2h+h^2 - 1}{h} = \lim_{h\to 0} \frac{2h+h^2}{h}$$

        Factor the numerator and cancel. 

        $$f'(1) = \lim_{h\to 0} \frac{h(2+h)}{h} = \lim_{h \to 0} 2+h = 2.$$

Once we can compute the derivative at a point, we are able to compute the tangent line. 

!!! example "Example 9"
    Compute the line tangent to the function $f(x) = x^2$ at $x = 1$. 

    ??? success "Solution"
        In the previous example we computed that $f'(1) = 2$, this is the slope of the tangent line. We also know the tangent line must pass through the point $(1,f(1)) = (1,1)$. Using point-slope form we get, 

        $$y - 1 = 2(x-1).$$

!!! example "Example 10"
    Compute the line tangent to the function $g(x) = 1-x^2$ at $x = 3$.

    ??? success "Solution"
        We use the limit definition of the derivative to find the slope of the tangent line,

        $$g'(3) = \lim_{h \to 0} \frac{g(3+h) - g(3)}{h}$$

        First compute $g(3)$ and $g(3+h)$,

        $$g(3) = 1 - 9 = -8$$

        $$g(3+h) = 1-(3+h)^2 = 1 - (9 + 6h + h^2) = -8 - 6h - h^2$$

        Now substitute into the limit,

        $$g'(3) = \lim_{h \to 0} \frac{(-8 - 6h - h^2) - (-8)}{h} = \lim_{h \to 0} \frac{-6h - h^2}{h} = \lim_{h \to 0} \frac{h(-6 - h)}{h}$$

        Cancel $h$,

        $$= \lim_{h \to 0} (-6 - h) = -6$$

        The slope of the tangent line at $x = 3$ is $-6$. Using point-slope form with the point $(3, -8)$,

        $$y + 8 = -6(x - 3)$$

!!! example "Example 11"
    Compute the line tangent to the function $f(x) = \sqrt{x}$ at $x = 4$.

    ??? success "Solution"
        We use the limit definition of the derivative to find the slope of the tangent line,

        $$f'(4) = \lim_{h \to 0} \frac{f(4+h) - f(4)}{h} = \lim_{h \to 0} \frac{\sqrt{4+h} - 2}{h}$$

        We multiply the numerator and denominator by the conjugate $\sqrt{4+h} + 2$,

        $$= \lim_{h \to 0} \frac{\sqrt{4+h} - 2}{h} \cdot \frac{\sqrt{4+h} + 2}{\sqrt{4+h} + 2} = \lim_{h \to 0} \frac{(4+h) - 4}{h(\sqrt{4+h} + 2)} = \lim_{h \to 0} \frac{h}{h(\sqrt{4+h}+2)}$$

        Cancel $h$,

        $$= \lim_{h \to 0} \frac{1}{\sqrt{4+h}+2} = \frac{1}{\sqrt{4}+2} = \frac{1}{4}$$

        The slope of the tangent line at $x = 4$ is $\frac{1}{4}$. Using point-slope form with the point $(4, 2)$,

        $$y - 2 = \frac{1}{4}(x - 4)$$

It's worth noting that the derivative does not always exist for a point along a function. In order for the derivative to exist at a point, the tangent line must be well defined. If the derivative exist at $a$, we say that $f$ is **differentiable** at $a$. 

The derivative of $f$ at $a$ does not exist if the the function $f$ is not continuous at $a$. Even if a function is continous, it does not guarentee that it is differentiable. If a function has a *corner* or *cusp* it is not differentiable at those points. In these cases, the tangent line is not well defined. Two examples below (from left to right) are the function $y = |x|$ and $y = x^{2/3}$. 

<center>
<iframe src="https://www.desmos.com/calculator/od2ftagt45?embed" width="300" height="300" style="border: 1px solid #ccc" frameborder=0></iframe>
<iframe src="https://www.desmos.com/calculator/eddtrxs37e?embed" width="300" height="300" style="border: 1px solid #ccc" frameborder=0></iframe>
</center>

If a function has a vertical tangent line at a point, then the derivative does not exist. An example of this is the cube root function, $y = \sqrt[3]{x}$. 

<center>
<iframe src="https://www.desmos.com/calculator/potfajkgop?embed" width="400" height="400" style="border: 1px solid #ccc" frameborder=0></iframe>
</center>

### 5.3.1 Application of the Derivative

The derivative at a point has many practical applications. If $s(t)$ describes the (one dimensional)position of an object at time $t$, then $s'(t)$ gives the **instantaneous velocity** at time $t$. Consider a particle moving along a standard number line, where its position is given by $s(t)$. If $s'(t)$ is positive, the particle is moving to the right and if $s'(t)$ is negative, the particle is moving to the left. 

In economics, if $C(x)$ is the total cost of producing $x$ units, then $C'(x)$ is called the **marginal cost**. The marginal cost is the approximate cost of producing one additional unit. There are alternative mathematical definitions of marginal cost, but they hold the same purpose and all yeild similar results. For example, the marginal cost may alternatively be computed as

$$MC(x) = C(x+1) - C(x).$$

From the definition, we see that this is the *exact* cost of producing one additional unit.

Similarly, if $R(x)$ is the total revenue, we define $R'(x)$ to be the **marginal revenue**. It is, approximately, the revenue added by selling one additional unit. 

In general, derivatives describe the instantaneous rate of change. So given any function, the derivative can be interpreted in this manner. For example if $P(t)$ describes the population of country in months, then $P'(t)$ describes the instantaneous change in population per year. The list of derivative interpretations goes on. 

!!! example "Example 12"
    The position of a particle moving along a straight line is given by $s(t) = t^2 + 3t$ 
    feet, where $t$ is measured in seconds. Find the instantaneous velocity at $t = 2$.

    ??? success "Solution"
        The instantaneous velocity is $s'(2)$,

        $$s'(2) = \lim_{h \to 0} \frac{s(2+h) - s(2)}{h}$$

        Compute $s(2)$ and $s(2+h)$,

        $$s(2) = 4 + 6 = 10$$

        $$s(2+h) = (2+h)^2 + 3(2+h) = 4 + 4h + h^2 + 6 + 3h = 10 + 7h + h^2$$

        Substitute into the limit,

        $$s'(2) = \lim_{h \to 0} \frac{(10 + 7h + h^2) - 10}{h} = \lim_{h \to 0} \frac{7h + h^2}{h} = \lim_{h \to 0} \frac{h(7+h)}{h} = \lim_{h \to 0}(7 + h) = 7$$

        The instantaneous velocity at $t = 2$ seconds is $7$ feet per second.

!!! example "Example 13"
    A company's total cost of producing $x$ units is given by $C(x) = 2x^2 + 10x + 50$ 
    dollars. Find the marginal cost at $x = 5$.

    ??? success "Solution"
        The marginal cost is $C'(5)$,

        $$C'(5) = \lim_{h \to 0} \frac{C(5+h) - C(5)}{h}$$

        Compute $C(5)$ and $C(5+h)$,

        $$C(5) = 2(25) + 10(5) + 50 = 50 + 50 + 50 = 150$$

        $$C(5+h) = 2(5+h)^2 + 10(5+h) + 50 = 2(25 + 10h + h^2) + 50 + 10h + 50$$

        $$= 150 + 30h + 2h^2$$

        Substitute into the limit,

        $$C'(5) = \lim_{h \to 0} \frac{(150 + 30h + 2h^2) - 150}{h} = \lim_{h \to 0} \frac{30h + 2h^2}{h} = \lim_{h \to 0}(30 + 2h) = 30$$

        The marginal cost at $x = 5$ units is $\$30$ per unit. This means that producing 
        one additional unit beyond 5 costs approximately $\$30$.

## 5.4 Derivative as a Function

In the prior section, we computed the derivative at a particular point which gave us the slope of the tangent line, or the instantaneous rate of change. If we compute the derivative for any point, then we can think about the derivative as a function of $x$ itself. 

!!! example "Example 14"
    Compute the derivative of the function $f(x) = x^2$. 

    ??? success "Solution"

        The procedure is the same as before, but now we leave $x$ arebitrary. Write the derivative as, 

        $$f'(x) = \lim_{h\to 0} \frac{f(x+h) - f(x)}{h}$$

        We compute, 

        $$f(x+h) = (x+h)^2 = x^2 + 2xh + h^2$$

        $$f(x+h) - f(x) = x^2 + 2xh + h^2 - x^2 = 2xh + h^2$$

        Now plug the above into the derivative definition, 

        $$f'(x) = \lim_{h\to 0} \frac{2xh+h^2}{h} = \lim_{h\to 0} \frac{h(2x+h)}{h} = \lim_{h\to 0} 2x+h = 2x$$

        So, $f'(x) = 2x$. 

For a function $y=f(x)$ the notation $f'(x)$, $y'$, $\frac{df}{dx}$, or $\frac{dy}{dx}$ is used interchangably to denote the derivative of the function. The notation that looks like a fraction is called Leibniz notation. It can be useful, especially when dealing with functions containing parameters or multiple variables. 

If we graph a function and its derivative side by side, the points on the graph correspond. The $y$-value on the graph of the derivative tells us the slope on the original graph. The following applet illustrates this for the function $f(x) = x^2$. 

<center>
<iframe src="/derivative_applet.html" width="800" height="400" frameborder="0" scrolling="no"></iframe>
</center>

!!! example "Example 15"
    Below is a graph of the function $f(x)$. Indicate where on the graph $f'(x)=0$.

    <center>
    <iframe src="https://www.desmos.com/calculator/ktowpfhtpu?embed" width="400" height="400" style="border: 1px solid #ccc" frameborder=0></iframe>
    </center>

    ??? success "Solution"
        When $f'(x) = 0$ it means that the tangent line is *horizontal*. This occurs at the following three points, 

        <center>
        <iframe src="https://www.desmos.com/calculator/xu3lzre3lz?embed" width="400" height="400" style="border: 1px solid #ccc" frameborder=0></iframe>
        </center>

!!! example "Example 16"
    Below is a graph of $f'(x)$. For what value of $x$ is the slope of $f(x)$ the steepest?
    
    <center>
    <iframe src="https://www.desmos.com/calculator/ua2uqcqilt?embed" width="400" height="400" style="border: 1px solid #ccc" frameborder=0></iframe>
    </center>

    ??? success "Solution"
        The graph of $y = f(x)$ is the steepest when $f'(x)$ has the greatest $y$-value. This occurs when $x=2$ and $f'(x) = 4$. 

## Exercises 

### 5.1 Exercises

**Problem 1.** Find the equation of the secant line to $f(x) = x^2 + 2x$ through the points where $x = 1$ and $x = 3$.

**Problem 2.** Find the equation of the secant line to $f(x) = x^3 - 4x$ through the points where $x = -1$ and $x = 2$.

**Problem 3.** Match the slopes to the labeled points on the function: (i) 2, (ii) 0, (iii) -4, (iv) 6.

<center>
<iframe src="https://www.desmos.com/calculator/vp1bauwdyv?embed" width="400" height="400" style="border: 1px solid #ccc" frameborder=0></iframe>
</center>

**Problem 4.** On the above graph sketch the tangent line at point C. 

### 5.2 Exercises

For problems 5-8, use the following graph of $f(x)$ to determine whether the following statement about limits are true or false. Justify your answer. If the are false, state the correct answer. 

<center>
<iframe src="https://www.desmos.com/calculator/uh1smja6em?embed" width="400" height="400" style="border: 1px solid #ccc" frameborder=0></iframe>
</center>

<div class="grid cards" markdown>

- **Problem 5.**

    $$\lim_{x\to 2} f(x) = -1$$

- **Problem 6.**

    $$\lim_{x \to 1} f(x) \text{ does not exist}$$

- **Problem 7.**

    $$\lim_{x\to -1} f(x) = -1$$

- **Problem 8.**

    $$\lim_{x\to -2} f(x) = -2$$

</div>

Use a table of values to compute the following limits. 

<div class="grid cards" markdown>

- **Problem 9.**

    $\displaystyle\lim_{x \to 1} \frac{x^3 - 1}{x - 1}$

- **Problem 10.**

    $\displaystyle\lim_{x \to 0} \frac{e^{2x} - 1}{x}$

- **Problem 11.**

    $\displaystyle\lim_{x \to 2} \frac{x^3 - 8}{x - 2}$

- **Problem 12.**

    $\displaystyle\lim_{x \to 0} \frac{(1+x)^3 - 1}{x}$

</div>

Compute the following limits algebraically.

<div class="grid cards" markdown>

- **Problem 13.**

    $\displaystyle\lim_{x \to 1} 2x^2 - 3x + 1$

- **Problem 14.**

    $\displaystyle\lim_{x \to 0} \frac{x^2 - x}{x}$

- **Problem 15.**

    $\displaystyle\lim_{x \to 3} \frac{x^2-6x+9}{x-3}$

- **Problem 16.**

    $\displaystyle\lim_{x \to 2} \frac{\sqrt{x+2}-2}{x-2}$

- **Problem 17.**

    $\displaystyle\lim_{x \to -2} \frac{x^2 + 5x + 6}{x + 2}$

- **Problem 18.**

    $\displaystyle\lim_{x \to 0} \frac{\frac{1}{x+2} - \frac{1}{2}}{x}$

- **Problem 19.**

    $\displaystyle\lim_{x \to 5} \frac{\sqrt{x-1}-2}{x-5}$

- **Problem 20.**

    $\displaystyle\lim_{x \to 4} \frac{x^2 - 3x - 4}{x - 4}$

</div>

**Problem 21.** The graph of $f(x)$ is given below. State all points of discontinuity and determine their type (removable, vertical asymptote, or jump).

<center>
<iframe src="https://www.desmos.com/calculator/0ri41th2cs?embed" width="400" height="400" style="border: 1px solid #ccc" frameborder=0></iframe>
</center>

**Problem 22.** The graph of $f(x)$ is given below. State all points of discontinuity and determine their type (removable, vertical asymptote, or jump).

<center>
<iframe src="https://www.desmos.com/calculator/nvyopbnsm3?embed" width="400" height="400" style="border: 1px solid #ccc" frameborder=0></iframe>
</center>

The **absolute value** of a number is the distance from that number to 0. For example, $|3| = 3$ and $|-3| = 3$. Formally we write, 

$$|x| = \begin{cases}
x & x \geq 0 \\
-x & x < 0
\end{cases}$$

It helps to remember that the absolute value of any number is always positive. 

**Problem 23.** Sketch the function $f(x) = |x|/x$ by using a table of values. State any points of discontinuity. 

**Problem 24.** Determine whether the following statements are true or false. Briefly justify your answer:

a) Polynomials are continuous for all values of $x$. 

b) If $f(x)$ is not defined at $x = a$, then $f(x)$ is discontinuous at $x=a$. 

c) If $f(x)$ is discontinuous at $x=a$, then $f(x)$ is not defined at $x=a$. 

d) If $\lim_{x\to a} f(x)$ exists, then $f(x)$ is continuous at $x=a$. 

### 5.3 Exercises

Compute the derivative of each function at the given point using the limit definition.

<div class="grid cards" markdown>

- **Problem 25.**

    $f(x) = x^2 - 3x$, at $x = 2$

- **Problem 26.**

    $f(x) = 4x^2 + 1$, at $x = 1$

- **Problem 27.**

    $f(x) = x^3$, at $x = 2$

- **Problem 28.**

    $f(x) = \dfrac{1}{x}$, at $x = 2$

- **Problem 29.**

    $f(x) = \sqrt{x+1}$, at $x = 3$

- **Problem 30.**

    $f(x) = \frac{1}{x-1}$, at $x = -1$

</div>

Find the equation of the tangent line to each function at the given point.

<div class="grid cards" markdown>

- **Problem 31.**

    $f(x) = x^2 + 1$, at $x = 2$

- **Problem 32.**

    $f(x) = 3x^2 - x$, at $x = 1$

- **Problem 33.**

    $f(x) = \sqrt{x}$, at $x = 9$

- **Problem 34.**

    $f(x) = \dfrac{1}{x}$, at $x = 3$

</div>

**Problem 35.** The position of a car along a straight road is given by $s(t) = t^2 + 5t$ feet, where $t$ is in seconds. Find the instantaneous velocity at $t = 3$ seconds. 

**Problem 36.** A company's total cost of producing $x$ units is $C(x) = 3x^2 + 20x + 100$ dollars. Find the marginal cost at $x = 4$ units and interpret your answer.

**Problem 37.** The revenue from selling $x$ units is given by $R(x) = 80x - 2x^2$ dollars. Find the marginal revenue at $x = 15$ units and interpret your answer.

**Problem 38.** A ball is dropped from a height of $200$ feet and its height after $t$ seconds is given by $h(t) = 200 - 16t^2$ feet. Find the instantaneous velocity of the ball at $t = 2$ seconds.

### 5.4 Exercises

Compute the derivative of the following functions using the limit definition

<div class="grid cards" markdown>

- **Problem 39.**

    $f(x) = x^2 + 2x$

- **Problem 40.**

    $y = \sqrt{x}$

- **Problem 41.**

    $f(x) = \frac{1}{x}$

- **Problem 42.**

    $g(x) = x^3$

</div>

**Problem 43.** A javelin is thrown into the air and its height in meters after $t$ seconds is modeled by the function $h(t) = −4.9t^2+18t+2$. Take the derivative of the height function to compute the equation for the vertical velocity of the javelin. 

**Problem 44.** A company's monthly revenue in thousands of dollars after spending $t$ thousand dollars on advertising is modeled by $R(t) = -2t^2 + 24t + 50$. Take the derivative of the revenue function to find the equation for the marginal revenue with respect to advertising spend.

**Problem 45.** Match the graph of the function to the correct derivative.

| Function | | Derivative | |
|---|---|---|---|
| A | <iframe src="https://www.desmos.com/calculator/tccg44g1py?embed" width="300" height="300" style="border: 1px solid #ccc" frameborder=0></iframe> | 1 | <iframe src="https://www.desmos.com/calculator/hi7k4uriuq?embed" width="300" height="300" style="border: 1px solid #ccc" frameborder=0></iframe> |
| B | <iframe src="https://www.desmos.com/calculator/zfyvfwgtr8?embed" width="300" height="300" style="border: 1px solid #ccc" frameborder=0></iframe> | 2 | <iframe src="https://www.desmos.com/calculator/fmbiyr2eve?embed" width="300" height="300" style="border: 1px solid #ccc" frameborder=0></iframe>|
| C | <iframe src="https://www.desmos.com/calculator/ituxdok5pz?embed" width="300" height="300" style="border: 1px solid #ccc" frameborder=0></iframe> | 3 | <iframe src="https://www.desmos.com/calculator/gmvfpaunbb?embed" width="300" height="300" style="border: 1px solid #ccc" frameborder=0></iframe> |