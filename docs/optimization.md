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

Similarly, a **local minimum** is a point that is lower than all immediate neighbors and a **global minimum** is the lowest point across the entire domain. The function below has a local minimum at $x = 4/3$, the function has no global minimum. 

<center>
<iframe src="https://www.desmos.com/calculator/fgfxf1gt5c?embed" width="400" height="400" style="border: 1px solid #ccc" frameborder=0></iframe>
</center>

The function $y = x^4$ is an example of a function with a global minimum. It has a global minimum at $x = 0$. We use the term **extrema** to denote both maxima and minima. 

!!! example "Example 4"
    Assume the entire domain of the function is shown in the graph below. Denote all local and global extrema.

    <iframe src="https://www.desmos.com/calculator/vs5gxswcsd?embed" width="400" height="400" style="border: 1px solid #ccc" frameborder=0></iframe>

    ??? success "Solution"
        There maximum are at $x=-4,\, 0, \, 4$ where the latter is a *global* max. There are also two local min at $x=-2,\, 2$. 

### 7.2.1 Critical Points

A **critical point** is any point on the graph where the derivative is equal to 0 (or does not exist, but we will only focus on the 0 case).

!!! example "Example 5"
    Compute all the *critical points* of the function $y = \frac{1}{3}x^3 + \frac{1}{2}x^2 - 6x + 1$.

    ??? success "Solution"
        Let's take the derivative of $y$. 

        $$y' = x^2 + x - 6$$

        Now compute when $y' = 0$,

        $$0 = x^2 + x - 6 = (x-2)(x+3)$$

        So the critical points are $x = 2$ and $x = -3$. 

*All* extrema are critical points **but not all critical points are extrema**. In Example 5, we can check from plotting the function that both $x=2$ and $x=-3$ are in fact extrema. 

<center>
<iframe src="https://www.desmos.com/calculator/gmutmhdtqf?embed" width="400" height="400" style="border: 1px solid #ccc" frameborder=0></iframe>
</center>

This isn't always the case though. The function $y = x^3$ has a critical point at $x=0$ but not an extrema. 

<center>
<iframe src="https://www.desmos.com/calculator/67ccqzriej?embed" width="400" height="400" style="border: 1px solid #ccc" frameborder=0></iframe>
</center>

Without graphing, how can we check whether or not a critical point is also an extrema? There are a couple options we can try. 

**Option 1: Second Derivative Test.** If our function is smooth, we can compute the second derivative of the function at the same point and use the concavity to determine whether we have a max or a min. 

* If $f'(x) = 0$ and $f''(x) > 0$ (concave up), then $x$ is a minimum. 
* If $f'(x) = 0$ and $f''(x) < 0$ (concave down), then $x$ is a maximum.
* If $f'(x) = 0$ and $f''(x) = 0$, then the second derivative test is **inconclusive**.

The second derivative test is often the fasted option, but doesn't always work. 

!!! example "Example 6"
    Use the second derivative test to determine whether $x=2$ and $x=-3$ are maximum or minimum of the function $y = \frac{1}{3}x^3 + \frac{1}{2}x^2 - 6x + 1$.

    ??? success "Solution"
        In example 5 we found the first derivative was, 

        $$y' = x^2 + x - 6$$

        Now let's compute the second derivative,

        $$y'' = 2x+1$$

        At $x = 2$, $y'' = 2(2)+1 = 5$, so $x=2$ is a minimum. At $x=-3$, $y''=2(-3)+1 = -5$, so $x=-3$ is a maximum. 

The second derivative test will not tell us the difference between local and global maximum. To do that, we must actually compute the $y$-value of the points. The second derivative test will not help us show $x=0$ is a minimum of the function $y=x^4$. 

**Option 2: First Derivative Test.** The goal of the first derivative test is to check the *sign* of the derivative before and after the critical point.

Suppose $x=a$ is a critical point of $f(x)$. If the derivative of $f$ switches from positive to negative at the critical point $x=a$, then $a$ is a maximum. If the derivative of $f$ switches from negative to positive at $x=a$, then $a$ is a minimum. If the derivative does not switch signs around the point $x=a$, then $x=a$ is not an extrema of the function $f$. 

!!! example "Example 7"
    Show that $x=0$ is a critical point, but not an extremum of the function $f(x) = x^3$. 

    ??? success "Solution"
        The derivative of $f(x) = x^3$ is $f'(x) = 3x^2$. To find the critical points, we want to know all values of $x$ that satisfy, 

        $$0 = x^2$$

        The only $x$ that solves this is $x=0$. For $x < 0$, $f'(x) > 0$. Additionally for $x > 0$, $f'(x) > 0$. This means the derivative is both positive before and after $x=0$, so it is *not* an extremum of the function.


## 7.3 Applied Optimization

Often times is applications are goal is to maximize or minimize *something*. In these cases, it will be valuable to utilize the appropriate derivative when possible. We have already introduced concepts like marginal cost, revenue, and profit, so now let's use them as tools for finding maximum and minimum. 

!!! example "Example 8"
    A concert promoter has found that if she sells tickets for $50 each, she can sell 1200 tickets, but for each $5 she raises the price, 50 less people attend. What *price* should she sell the tickets at to maximize her revenue?

    ??? success "Solution"
        The goal is to **maximize** revenue. So the first step is to express revenue as a function. Revenue, $R = pq$ where $p$ is the price per ticket and $q$ is the quantity sold. Since we want the *price* that maximizes revenue, let's write $q$ as a function of $p$. 

        The relationship between $q$ and $p$ is linear and given by the phrasing: "if she sells tickets for $50 each, she can sell 1200 tickets, but for each $5 she raises the price, 50 less people attend." Let's write a table of values from this:

        | price | quantity |
        | --- | --- |
        | 50 | 1200 |
        | 55 | 1150 |
        | 60 | 1100 |
        | 65 | 1050 |

        We can use two of the points to compute the slope,

        $$m = \frac{1100 - 1200}{60-50} = -10.$$

        Using point slope form we get, 

        $$q - 1200 = -10(p-50)$$

        and simplifying gives, 

        $$q = 1700 - 10p.$$

        Now we can write revenue as, $R = p(1700-10p) = 1700p - 10p^2$. Computing the derivative gives, 

        $$R' = 1700 - 20p$$

        and we solve for when $R' = 0$ to get $p = 85$. We should check this is indeed a maximum and not a minimum. To do this, let's check the second derivative:

        $$R'' = -20 < 0$$

        so it is, in fact, a maximum. 

        Therefore, the revenue is maximized when the price per ticket is $85. A this price she will sell 850 tickets and total revenue will be $72,250.


Recall that profit $P = R - C$. If we want to maximize profit we take the derivative, 

$$P' = R' - C'$$

and then find when it is equal to 0, 

$$0 = R' - C' \implies R' = C'.$$

This is where the expression "profit is maximized when marginal cost and marginal revenue are equal" comes from! Of course, we now know this is not entirely true. When marginal cost equals marginal revenue profit has a *critical point*, but we should be careful to investigate whether or not that is a maximum!

!!! example "Example 9"
    A company sells q ribbon winders per year at $p per ribbon winder. The demand function for ribbon winders is given by: $p = 300 − 0.02q$. The ribbon winders cost $30 apiece to manufacture, plus there are fixed costs of $9000 per year. Find the quantity where profit is maximized.

    ??? success "Solution"
        Revenue is $R = q(300-0.02q)$ and cost is $C = 30q + 9000$. Thus profit is,

        $$P = 300q - 0.02q^2 - 30q - 9000 = 270q - 0.02q^2 - 9000.$$

        Taking the derivative gives

        $$P' = 270 - 0.04q$$

        and setting $P'=0$ gives $q = 6750$. This is indeed a maximum, because the second derivative $P'' = -0.04$ is always negative. 

!!! example "Example 10"
    A rectangular garden is to be constructed using a rock wall as one side of the garden and wire fencing for the other three sides. Given 100 ft of wire fencing, determine the dimensions that would create a garden of maximum area. What is the maximum area?

    ??? success "Solution"
        Let $x$ be the length of each side perpendicular to the rock wall and $y$ the length of the side parallel to it. The wall serves as the fourth side, so the 100 ft of fencing only has to cover the other three:

        $$2x + y = 100 \quad\Longrightarrow\quad y = 100 - 2x$$

        The area of the garden is length times width. Substituting for $y$ gives the area as a function of $x$ alone:

        $$A(x) = x(100 - 2x) = 100x - 2x^2$$

        Both sides must have positive length, so $x$ is restricted to $0 < x < 50$.

        To find the maximum, take the derivative and set it equal to zero:

        $$A'(x) = 100 - 4x = 0 \quad\Longrightarrow\quad x = 25$$

        The second derivative, $A''(x) = -4$, is negative everywhere. That means the area curve opens downward, so $x = 25$ gives a maximum and not a minimum. The area also drops to zero at both ends of the interval, which confirms that this is the largest possible value.

        Plugging $x = 25$ back into the fencing equation gives the side along the wall:

        $$y = 100 - 2(25) = 50$$

        So the garden should measure 25 ft by 50 ft, with the 50 ft side running parallel to the rock wall. 


## Exercises

### 7.1 Exercises

Compute the second derivatives of the following functions.

<div class="grid cards" markdown>

- **Problem 1.**

    $y = e^x$

- **Problem 2.**

    $y = 3x+4$ 

- **Problem 3.**

    $g(x) = x^2 - 10x + 1$

- **Problem 4.**

    $f(x) = x^3 + \frac{1}{2}x^2 - 3x + 1$

- **Problem 5.**

    $y = \frac{x}{x+1}$

- **Problem 6.**

    $y = x\ln(x)$

- **Problem 7.**

    $y = e^{1-2x}$

- **Problem 8.**

    $y = \sqrt{x^2+1}$

</div>

Use the second derivative to determine when the function is concave up versus concave down. 

<div class="grid cards" markdown>

- **Problem 9.**

    $y = x^3 - 6x^2 + 4$

- **Problem 10.**

    $y = x^4 - 6x^2$

- **Problem 11.**

    $y = xe^x$

- **Problem 12.**

    $y = \ln(x^2+1)$

</div>

### 7.2 Exercises 

Compute all critical points of the following functions. 

<div class="grid cards" markdown>

- **Problem 13.**

    $y = x^3 - 3x$

- **Problem 14.**

    $y = x^4 - 8x^2$

- **Problem 15.**

    $y = 2x^3 - 3x^2 - 12x$

- **Problem 16.**

    $y = x^2 e^x$

- **Problem 17.**

    $y = \dfrac{x}{x^2+1}$

- **Problem 18.**

    $y = x + \dfrac{4}{x}$

</div>

Determine the critical points of the following functions, then classify each critical point as a maximum, minimum, or neither by using the first and second derivative tests. 

<div class="grid cards" markdown>

- **Problem 19.**

    $y = x^3 - 12x$

- **Problem 20.**

    $y = x^4 - 4x^3$

- **Problem 21.**

    $y = 3x^4 - 4x^3 - 12x^2$

- **Problem 22.**

    $y = \dfrac{x^2}{x-1}$

</div>

### 7.3 Exercises 

**Problem 23.** Owners of a car rental company have determined that if they charge customers $p$ dollars per day to rent a car, where $50\leq p \leq 200$, the number of cars $n$ they rent per day can be modeled by the linear function $n(p) = 1000 - 5p$. If they charge $⁢50 per day or less, they will rent all their cars. If they charge $⁢200 per day or more, they will not rent any cars. Assuming the owners plan to charge customers between $50 per day and $⁢200 per day to rent a car, how much should they charge to maximize their revenue?

**Problem 24.** A manufacturer of wireless headphones finds that to sell $x$ pairs per month, the price per pair must be $p(x) = 120 - 0.02x$ dollars. The monthly cost of producing $x$ pairs is $C(x) = 2000 + 40x$ dollars. How many pairs should the manufacturer produce each month to maximize profit, and what price should it charge per pair?

**Problem 25.** The concentration of a drug in a patient's bloodstream $t$ hours after it is injected is modeled by $C(t) = \dfrac{5t}{t^2 + 4}$ milligrams per liter, where $t \geq 0$. At what time is the concentration highest? What is the maximum concentration?

**Problem 26.** A property manager runs an apartment complex with 80 units. When the rent is $\$1200$ per month, every unit is occupied. Each $\$25$ increase in monthly rent leaves one more unit vacant. Each occupied unit costs $\$100$ per month in maintenance. What monthly rent should the manager charge to maximize profit, and how many units will be occupied at that rent?

**Problem 27.** A cargo boat makes a 200-mile trip at a constant speed of $v$ miles per hour. Fuel costs $\dfrac{v^2}{50}$ dollars per hour, and the crew is paid a combined $\$32$ per hour. At what speed should the boat travel to minimize the total cost of the trip? What is the minimum cost?

**Problem 28.** A farmer can harvest 120 bushels of apples today and sell them for $\$4$ per bushel. For each week the farmer waits, the crop grows by 10 bushels, but the price drops by $\$0.20$ per bushel. How many weeks should the farmer wait to maximize revenue? What is the maximum revenue?
