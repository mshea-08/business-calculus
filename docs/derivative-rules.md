# Derivative Rules 

It is quite laborsome to use the limit definition of the derivative every time you want to compute a derivative. In this chapter, we state some rules that will allow us to quickly compute derivatives we are interested in. 

## 6.1 Basic Rules 

Let's use some examples to motivate some fundamental rules. 

!!! example "Example 1"
    Compute the derivative of the function $f(x) = 5$. 

    ??? success "Solution"
        The function is a horizontal line, so the slope is always 0. Therefore, $f'(x) = 0$. 

!!! note "Rule"
    The derivative of a constant function is zero. 

!!! example "Example 2"
    Compute the derivative of the function $f(x) = 2x + 4$. 

    ??? success "Solution"
        Any tangent line of a linear function is the same line! Therefore the slope of the tangent line, e.g. the derivative, $f'(x) = 2$. 

!!! note "Rule"
    Let $f(x)$ be a line with slope $m$, then $f'(x) = m$. 

The derivative is known as a **linear operator**. This means it satisfies the following two useful properties:

!!! note "Constant Multiplication Rule"
    Let $f$ be a function with derivative $f'$ and let $k$ be any constant. Then,

    $$\frac{d}{dx}(kf) = kf'$$

In other words, if a function is multiplied by a constant, then the derivative of this new function is just the derivative of the old function multiplied by the same constant. 

!!! example "Example 3"
    The derivative of the function $f(x) = x^3 - 2x$ is $f'(x) = 3x^2-2$. What is the derivative of $g(x) = 3x^3-6x$?

    ??? success "Solution"
        Notice that 

        $$g(x) = 3x^3-6x = 3(x^3-2x) = 3f(x)$$ 

        So 

        $$g'(x) = 3f'(x) = 3(3x^2-2) = 9x^2 - 6.$$

!!! note "Sum and Difference Rule"
    Let $f$ and $g$ be functions with derivatives $f'$ and $g'$, respectively. Then, 

    $$\frac{d}{dx}(f \pm g) = f' \pm g'.$$

!!! example "Example 4"
    Find the derivative of each function in terms of the functions given using the sum/difference and constant multiplication rules.

    a) $f(x) = 3g(x) - 5h(x)$

    b) $y = 4f(x) + 2g(x) - h(x)$

    c) $y = -6f(x)$

    ??? success "Solution"
        a) $f'(x) = 3g'(x) - 5h'(x)$

        b) $y' = 4f'(x) + 2g'(x) - h'(x)$

        c) $y' = -6f'(x)$

!!! example "Example 5"
    Suppose $f'(1) = 3$, $g'(1) = -2$, and $h'(1) = 5$. Find the derivative of each function at $x = 1$.

    a) $p(x) = 4f(x) + g(x)$

    b) $q(x) = 3g(x) - 2h(x)$

    c) $r(x) = f(x) + g(x) - 4h(x)$

    ??? success "Solution"
        a) First use the sum/difference and constant multiplication rules, then plug in the point $x=1$.

        $$p'(1) = 4f'(1) + g'(1) = 4(3) + (-2) = 10$$

        b) $q'(1) = 3g'(1) - 2h'(1) = 3(-2) - 2(5) = -6 - 10 = -16$

        c) $r'(1) = f'(1) + g'(1) - 4h'(1) = 3 + (-2) - 4(5) = 3 - 2 - 20 = -19$

## 6.2 Power Rule

!!! note "Power Rule"
    The derivative of $f(x) = x^n$ is $f'(x) = nx^{n-1}$. 

We can use the power rule to produce results identical to what we saw in Chapter 5. 

!!! example "Example 6"
    Compute the derivative of $y = x^2$ using the power rule. 

    ??? success "Solution"
        According to the power rule, 

        $$y' = 2x^{2-1} = 2x.$$

We can also use the power rule alongside the basic rules learned in Section 6.1 to compute the derivative of any polynomial.

!!! example "Example 7"
    Compute the derivative of $f(x) = x^3 - 2x^2 + 5x - 1$. 

    ??? success "Solution"
        First split up the derivative by sums and differences, 

        $$\frac{df}{dx} = \frac{d}{dx}(x^3 - 2x^2 + 5x - 1) = \frac{d}{dx}(x^3) - \frac{d}{dx}(2x^2) + \frac{d}{dx}(5x) - \frac{d}{dx}(1)$$

        Now take the derivative of each term, 

        $$\frac{d}{dx}(x^3) = 3x^{3-1} = 3x^2$$

        $$\frac{d}{dx}(2x^2) = 2\frac{d}{dx}(x^2) = 2 \cdot 2x^{2-1} = 4x$$

        $$\frac{d}{dx}(5x) = 5$$

        $$\frac{d}{dx}(1) = 0$$

        and recombine, 

        $$\frac{df}{dx} = 3x^2 - 4x + 5.$$

When first starting out, it is helpful to write out each step and clearly indicate which rule is being used. Once you are practiced, you only need to write down what you need. 

!!! example "Example 8"
    Let $g(x) = 30x^4 - 12x^3 - 10x + 16$. Compute $g'(1)$. 

    ??? success "Solution"
        To compute the derivative at $x=1$, first compute the derivative as a function, then plug in the value. 

        $$g'(x) = 30 \cdot 4 x^3 - 12 \cdot 3 x^2 - 10 = 120x^3 - 36x^2 - 10$$

        $$g'(1) = 120 - 36 - 10 = 74.$$

Note that the power rule holds for *any* number $n$ (not just positive integers). So we can use the power rule to take derivatives of roots and negative exponents. 

!!! example "Example 9"
    Compute the derivative of $f(x) = \sqrt{x}$ using the power rule.

    ??? success "Solution"
        First rewrite $\sqrt{x}$ as a power of $x$,

        $$f(x) = x^{1/2}$$

        Now apply the power rule,

        $$f'(x) = \frac{1}{2}x^{1/2 - 1} = \frac{1}{2}x^{-1/2} = \frac{1}{2\sqrt{x}}$$

!!! example "Example 10"
    Compute the derivative of $y = \dfrac{1}{x^2}$ using the power rule.

    ??? success "Solution"
        First rewrite $\dfrac{1}{x^2}$ as a power of $x$,

        $$y = x^{-2}$$

        Now apply the power rule,

        $$y' = -2x^{-2-1} = -2x^{-3} = -\frac{2}{x^3}$$

When simplifying, it is okay leave negative exponents in complicated expressions however if the function is simple it is good practice to always rewrite in terms of positive exponents like is done in the above examples. 

## 6.3 Derivatives of Exponentials and Logarithms

For many important applications, we will need to know how to take derivatives of exponential and logarithmic functions. 

!!! note "Exponential Derivative"
    Let $f(x) = e^x$, then $f'(x) = e^x$. 

    Let $g(x) = b^x$ for any $b > 0$, then $g'(x) = \ln(b) \cdot b^x$.

We see another reason why $e$ is a special constant. The function $f(x) = c e^x$ (where $c$ is a constant) is the *only* function where $f(x) = f'(x)$. 

!!! note "Natural Logarithm Derivative"
    Let $f(x) = \ln x$, then $f'(x) = \frac{1}{x}$.

From here on out, we will only be dealing with the natural logarithm function. We saw in Chapter 4, that all logarithms can be translated to whatever base we want and the derivative of the natural logarithm is the simplest to remember. 

!!! example "Example 11"
    A population of bacteria grows according to the model $P(t) = 1000e^t$, where $t$ is measured in hours. Find the rate of growth at $t = 2$ hours.

    ??? success "Solution"
        Taking the derivative using the rule $\dfrac{d}{dx}e^x = e^x$,

        $$P'(t) = 1000e^t$$

        At $t = 2$ hours,

        $$P'(2) = 1000e^2 \approx 7{,}389 \text{ bacteria per hour}$$

        Notice that for the function $e^t$, the rate of growth equals the population itself — this is the defining property of the exponential function.

!!! example "Example 12"
    A company finds that its revenue in thousands of dollars after running $x$ ads is modeled by $R(x) = 5\ln(x) + 2x$. Find the marginal revenue function and compute the marginal revenue at $x = 10$ ads.

    ??? success "Solution"
        Taking the derivative using the rule $\dfrac{d}{dx}\ln(x) = \dfrac{1}{x}$,

        $$R'(x) = \dfrac{5}{x} + 2$$

        At $x = 10$ ads,

        $$R'(10) = \dfrac{5}{10} + 2 = 0.5 + 2 = 2.5$$

        The marginal revenue at $x = 10$ ads is $\$2{,}500$. This means that running one additional ad beyond 10 generates approximately $\$2{,}500$ in additional revenue.

## 6.4 Product and Quotient Rule 

!!! example "Example 13"
    Compute $h'(x)$, where $h(x) = (x^2-3x+2)(x+1)$.

    ??? success "Solution"
        This function is not simply the sum or difference of polynomials, it is a product. To take the derivative we can first multiply out

        $$h(x) = x^3+x^2-3x^2-3x+2x+2 = x^3-2x^2-x+2$$

        then take the derivative

        $$h'(x) = 3x^2-4x-1$$

The above method works, but might become taxing if the product involves more complicated polynomials. The following rule is therefore useful, 

!!! note "Product Rule"
    Let $y = f(x)g(x)$, then $y' = f'(x)g(x) + f(x)g'(x)$. 

Note that the product rule does *not* just tell us to take the derivative of each term! This would give us the wrong answer. 

!!! example "Example 14" 
    Use the product rule to compute the derivative of the function $y = (x^2+3)(2x+4)$.

    ??? success "Solution"
        Let $f(x) = x^2+3$ and $g(x) = 2x+4$. Then using the formula we get,

        $$y' = 2x(2x+4)+(x^2+3)(2) = 4x^2 + 8x + 2x^2+6 = 6x^2+8x+6$$

The product rule works for the product of any two functions, not just polynomials.

!!! example "Example 15"
    Find the derivative of $h(x) = e^x\ln(x)$. 

    ??? success "Solution"
        The two functions are $e^x$ and $\ln(x)$. Using the product rule we get,

        $$\frac{dh}{dx} = e^x\ln(x) + e^x\frac{1}{x}$$

The product rule also works for the product of more than two functions, following a similar pattern.

!!! note "Product Rule for Three Functions"
    Let $y = f(x)g(x)h(x)$, then $y'(x) = f'(x)g(x)h(x)+f(x)g'(x)h(x)+f(x)g(x)h'(x)$.

We also have a rule for when a function looks like a quotient. 

!!! note "Quotient Rule"
    Suppose $y = f(x)/g(x)$, then 

    $$y' = \frac{g(x)f'(x) - f(x)g'(x)}{(g(x))^2}$$

The order of terms in the numerator is important. I use the little rhyme, "Lo d-Hi minus Hi d-Lo over Lo-Lo," to help me remember the expression. When using the quotient rule, it is helpful to simplify a quotient expression as much as possible *before* using the quotient rule. Expressions get long and complicated quick when using the rule. 

!!! example "Example 16"
    Find the derivative of the function, 

    $$y = \frac{x-1}{x^2-1}$$

    ??? success "Solution"
        First let's simplify the functions, 

        $$y = \frac{x-1}{(x-1)(x+1)} = \frac{1}{x+1}$$

        Now differentiate, 

        $$y' = \frac{(x+1)(0) - 1 (1)}{(x+1)^2} = -\frac{1}{(x+1)^2}$$

When presenting solutions you are expected to do simple simplifications, such as constant multiplication, but you do not need to do anything beyond that. Notice above I left the denominator factored--and you should too! 

### 6.4.1 Marginal Average Cost and Revenue

The **average cost** of producing $x$ units is, 

$$AC(x) = \frac{C(x)}{x}$$

The **marginal average cost**, $AC'(x)$, is the approximate change in average cost by producing an additional unit. Note that this is different from marginal cost. In marginal average cost, fixed costs are averaged over the number of units, this is not true of marginal cost. For example, consider an item with cost function, 

$$C(x) = 5x + 100$$

Recall that the variable cost is $5 and the fixed cost is $100. In this case the marginal cost is the same for all items, also $5. Since the average cost disperses the fixed cost accross each item, the marginal average cost will be negative (we will see this below!). 

!!! example "Example 17"
    A company's average cost of producing $x$ units is given by 

    $$AC(x) = \frac{C(x)}{x} = \frac{5x+100}{x}$$

    Find the marginal average cost $AC'(x)$.

    ??? success "Solution"
        You might want to straight away apply the quotient rule but let's simplify first, 

        $$AC(x) = 5 + \frac{100}{x} = 5 + 100x^{-1}$$

        Now we can take the derivative without the quotient rule, 

        $$AC'(x) = -100x^{-2} = -\frac{100}{x^2}$$

        We see that for any value of $x$ the marginal average cost is negative. Meaning producing more items makes the average cost decrease. 

In a similar vein we can compute the **average revenue**,

$$AR(x) = \frac{R(x)}{x}$$

and **marginal average revenue**, $AR'(x)$.

!!! example "Example 18"
    A company's total revenue from selling $x$ units is given by $R(x) = 80x - 2x^2$. The average revenue is defined as

    $$AR(x) = \frac{R(x)}{x} = \frac{80x - 2x^2}{x}$$

    Find the marginal average revenue $AR'(x)$ and interpret its meaning.

    ??? success "Solution"
        Since we can simplify the average revenue first, no quotient rule is needed. 
        
        $$AR(x) = 80 - 2x$$

        Taking the derivative,

        $$AR'(x) = -2$$

        The marginal average revenue is constant at $-2$. This means that for every additional unit produced, the average revenue decreases by $\$2$. 

        Why might average revenue decrease with more items sold? In order to sell more items a company may need to decrease the price or spend more money on advertising. 

## 6.5 Chain Rule

The last derivative rule we need is the chain rule. The chain rule helps when we have a composition of functions, $y = f(g(x))$. We need to be able to confindently identify and decompose compositions in order to properly use the chain rule, so let's see some examples. 

!!! example "Example 19"
    All of the function listed have the form $y = f(g(x))$. Decompose the following composition of functions into their parts, $f$ and $g$. 

    a) $y = (x+3)^4$

    b) $y = \ln(x^2+1)$

    c) $y = e^{3x+2}$

    d) $y = \frac{1}{x^2-3x+2}$

    ??? success "Solution"
        a) To solve these problems, it helps to think of the order of algebra you would perform if you plugged a value in for $x$. In this example, I would first add 3, so the inner function is $g(x) = x+3$, then I would raise that to the power of 4, so the outer function is $f(u) = u^4$/ Here we use the *dummy variable* $u$ to remind ourselves that we are plugging a different function in for $u$. 

        b) Here the inner functionis $g(x) = x^2+1$ and the outer function is $f(u) = \ln u$. 

        c) It can be tricky to identify the composition when dealing with exponentials. First thing we must do here is compute $3x+2$, so $g(x) = 3x+2$. The outer function is the $f(u) = e^u$.

        d) Another way to write the function is as $y = (x^2-3x+2)^{-1}$, now the composition should be clear. We have $g(x) = x^2 - 3x + 2$ and $f(u) = u^{-1}$. 

!!! note "Chain Rule"
    Let $y = f(g(x))$, then $y' = f'(g(x))\cdot g'(x)$. 

    Alternatively, let $y = f(u)$ and $u = g(x)$. Then

    $$\frac{dy}{dx} = \frac{dy}{du}\cdot\frac{du}{dx}$$

!!! example "Example 20"
    Find the derivative of the function $y = (x^2-3x)^6$. 

    ??? success "Solution"
        The inner function is, $u = x^2-3x$ so, 

        $$\frac{du}{dx} = 2x-3$$

        and the outer function is, $y = u^6$ so 

        $$\frac{dy}{du} = 6u^5$$

        Thus 

        $$\frac{dy}{dx} = \frac{dy}{du} \cdot \frac{du}{dx} = 6 (x^2-3x)^5 \cdot (2x-3)$$

        It is important to use parentheses correctly when expressing derivatives using the chain rule. 

!!! example "Example 21"
    Determine the derivative of the function $y = e^{x^2-1}$. 

    ??? success "Solution"
        We have $u = x^2-1$, therefore

        $$\frac{du}{dx} = 2x$$ 

        and $y = e^u$, so 

        $$\frac{dy}{du} = e^u$$

        Combining gives, 

        $$y' = 2xe^{x^2-1}$$

## 6.6 More Complicated Derivatives 

You may face situations where computing the derivative involves applying multiple rules. In order to solve the problems, you should first identify the order the rules should be applied in--work from outside to inside. Carefully write down the steps to make sure you do not miss anything. 

!!! example "Example 22"
    Compute the derivative of the function 

    $$y = \left(\frac{3x}{x+1}\right)^4$$

    ??? success "Solution"
        We first apply the **chain rule**, where the outer function is 

        $$y = u^4$$

        and the inner function is 

        $$u = \frac{3x}{x+1}$$

        To compute the derivative of the inner function, we need the **quotient rule**

        $$\frac{du}{dx} = \frac{3(x+1)-3x}{(x+1)^2} = \frac{3}{(x+1)^2}$$

        Now finishing the chain rule gives, 

        $$y' = 4\left(\frac{3x}{x+1})^3 \cdot \frac{3}{(x+1)^2}$$

!!! example "Example 23"
    Find 

    $$\frac{d}{dx}\left(x^3 \cdot \ln (2x+1)\right)$$

    ??? success "Solution"
        We first use the **product rule**, where the pieces are $x^3$ and $\ln(2x+1)$. For the second term we need to apply the **chain rule**. We get, 

        $$3x^2\ln(2x+1) + x^3 \cdot \frac{1}{2x+1} \cdot 2$$



## Exercises 

### 6.1 Exercises

Compute the derivative of each function in terms of $f'(x)$, $g'(x)$, and $h'(x)$. 

<div class="grid cards" markdown>

- **Problem 1.**

    $y = f(x) + g(x)$

- **Problem 2.**

    $p(x) = 3f(x) + h(x)$

- **Problem 3.**

    $q(x) = 2g(x) - h(x) + 3f(x)$

- **Problem 4.**

    $y = g(x) + 4h(x) + 10$

</div>

Suppose $f'(3) = 3$, $g'(3) = 1$, and $h'(3) = 0$. Compute the derivatives of the following functions, evaluated at $x = 3$. 

<div class="grid cards" markdown>

- **Problem 5.**

    $r(x) = 3f(x) + 2g(x)$

- **Problem 6.**

    $p(x) = 3f(x)$ 

- **Problem 7.**

    $t(x) = f(x) - 2g(x) + h(x)$

- **Problem 8.**

    $q(x) = 4f(x) + 10h(x)$

</div>

**Problem 9.** Suppose $f'(1) = 2$ and $g'(1) = 3$. Find a constant $c$ such that $y = cf(x) + g(x)$ satisfies $y'(1) = 11$.

**Problem 10.** Suppose $f'(2) = 4$ and $g'(2) = -1$. Find constants $a$ and $b$ such that $y = af(x) + bg(x)$ satisfies $y'(2) = 10$.

### 6.2 Exercises 

For each of the following functions, compute its derivative

<div class="grid cards" markdown>

- **Problem 11.**

    $y = x^4$

- **Problem 12.**

    $y = x^{14}$ 

- **Problem 13.**

    $g(x) = x^{3/2}$

- **Problem 14.**

    $f(x) = \frac{1}{x^3}$

</div>

For each of the following functions, determine its derivative. 

<div class="grid cards" markdown>

- **Problem 15.**

    $f(x) = 3x^4 - 2x^3 + x - 7$

- **Problem 16.**

    $y = 5\sqrt{x} + \dfrac{3}{x}$

- **Problem 17.**

    $g(x) = \dfrac{x^4}{4} - \dfrac{x^3}{3} + 2x$

- **Problem 18.**

    $y = 4x^3 - \dfrac{2}{x^2} + \sqrt{x}$

- **Problem 19.**

    $h(x) = 3x^{-4} + 2x^{1/3} - 5x$

- **Problem 20.**

    $f(x) = \dfrac{2}{x^3} - \dfrac{1}{\sqrt{x}} + 6x^2$

</div>

**Problem 21.** A ball is dropped from a bridge and its height above the water in meters after $t$ seconds is given by $h(t) = 80 - 4.9t^2$. Find $h'(t)$ and determine how fast the ball is falling at $t = 3$ seconds.

**Problem 22.** A company's total cost of producing $x$ units is given by $C(x) = 0.01x^3 - 0.6x^2 + 15x + 100$ dollars. Find the marginal cost function and compute the marginal cost at $x = 20$ units.

**Problem 23.** The population of a bacteria culture after $t$ hours is modeled by $P(t) = 500t^2 - \dfrac{t^3}{3}$. Find $P'(t)$ and determine the rate of growth at $t = 6$ hours.

**Problem 24.** The demand for a product is given by $D(p) = \dfrac{800}{\sqrt{p}}$, where $p$ is the price in dollars. Find $D'(p)$ and compute the rate of change of demand when the price is $\$4$.

### 6.3 Exercises 

For each of the following functions, compute its derivative

<div class="grid cards" markdown>

- **Problem 25.**

    $y = e^x$

- **Problem 26.**

    $y = 3^x$ 

- **Problem 27.**

    $g(x) = 12^x$

- **Problem 28.**

    $f(x) = 2^x$

</div>

For each of the following functions, compute its derivative

<div class="grid cards" markdown>

- **Problem 29.**

    $f(x) = \ln(x) + x$

- **Problem 30.**

    $h(x) = 2^x - x^3$ 

- **Problem 31.**

    $y = \frac{4}{x^3} - x^2 + 3e^x$

- **Problem 32.**

    $q(x) = 4\cdot 3^x - \sqrt{2x}$

</div>

**Problem 33.** The value in dollars of a piece of artwork after $t$ years is modeled by $V(t) = 5000e^t$. Find $V'(t)$ and determine the rate of appreciation at $t = 2$ years.

**Problem 34.** The monthly profit in thousands of dollars from selling $x$ units of a product is modeled by $P(x) = 8\ln(x) - 3x + 50$. Find the marginal profit function and compute the marginal profit at $x = 4$ units.

### 6.4 Exercises 

Find the derivatives of the following functions, 

<div class="grid cards" markdown>

- **Problem 35.**

    $y = xe^x$

- **Problem 36.**

    $f(x) = \dfrac{e^x}{1+e^x}$

- **Problem 37.**

    $g(t) = t^3(1+2t^2)$

- **Problem 38.**

    $h(x) = x^2 \ln(x)$

- **Problem 39.**

    $y = \dfrac{x^2 + 1}{x^3 - 2}$

- **Problem 40.**

    $y = (x^2 + 3)(x^3 - 5x)$

- **Problem 41.**

    $g(x) = \dfrac{\ln(x)}{x^2}$

- **Problem 42.**

    $h(x) = \dfrac{x^3 + 1}{e^x}$

</div>

**Problem 43.** A company's total cost of producing $x$ units is $C(x) = x^3 - 4x^2 + 20x + 100$. Compute the marginal average cost.

**Problem 44.** A company's total revenue from selling $x$ units is $R(x) = 120x - 3x^2$. Compute the marginal average revenue.

**Problem 45.** A company's total cost of producing $x$ units is $C(x) = 2x^2 + \sqrt{x} + 80$. Compute the marginal average cost.

**Problem 46.** A company's total revenue from selling $x$ units is $R(x) = 200x - x^3$. Compute the marginal average revenue. At what production level is the marginal average revenue equal to zero?

### 6.5 Exercises 

Find the following derivatives using the chain rule,

<div class="grid cards" markdown>

- **Problem 47.**

    $y=(x^2+3x-1)^4$

- **Problem 48.**

    $f(x) = \ln(3x+7)$

- **Problem 49.**

    $y = (4x^2 - 10x)^6$

- **Problem 50.**

    $h(t) = e^{3t^2+2}$

- **Problem 51.**

    $y = e^{1/x^2}$

- **Problem 52.**

    $y = \ln(e^x+x)$

</div>

### 6.6 Exercises

Compute the derivative of each function.

<div class="grid cards" markdown>

- **Problem 53.**

    $y = x^2 e^x$

- **Problem 54.**

    $y = e^x + \ln(x)$

- **Problem 55.**

    $f(x) = \dfrac{x^3 + 1}{x^2 - 1}$

- **Problem 56.**

    $y = (2x^3 - 1)(x^2 + 5)$

- **Problem 57.**

    $h(x) = \dfrac{\ln(x)}{x^3}$

- **Problem 58.**

    $f(t) = \dfrac{t^2 + 3t}{e^t}$

- **Problem 59.**

    $p(x) = \ln(x) \cdot e^x$

- **Problem 60.**

    $y = \dfrac{x^4 - 2x^2 + 1}{x^2}$

- **Problem 61.**

    $c(t) = t^3e^{t^2}$

- **Problem 62.**

    $g(x) = \dfrac{e^{3x}}{x^2 + 1}$

- **Problem 63.**

    $y = x^2 \ln(x^2 + 1)$

- **Problem 64.**

    $f(x) = \dfrac{\ln(x^3)}{e^{2x}}$

</div>

