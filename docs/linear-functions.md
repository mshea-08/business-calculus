# 1. Linear Functions

## 1.1 Graph of a Line 

Equations whose graphs are straight lines are known as **linear equations**. Examples of lines include: $y = 2x + 5$, $x - 2y = 1$, $y = 4$, etc. Given the equation of a line, we can graph it by finding two points on the line and connecting them. To find two points, simply pick *any* two $x$ values and compute the corresponding $y$ values. 

!!! example "Example 1"
    Sketch a graph of the line $y = 2x - 1$.

    ??? success "Solution"
        Let's pick the two $x$ values, $x = 1$ and $x = -1$. When $x = 1$, 

        $$y = 2(1) - 1 = 2 - 1 = 1$$

        and when $x = -1$,

        $$y = 2(-1) - 1 = -2 -1 = -3.$$

        So we can plot the points $(1,1)$ and $(-1,-3)$ and connect them with a line. 

        <!-- https://www.desmos.com/calculator/1e5qrzyqz0 -->

        <center><iframe src="https://www.desmos.com/calculator/1e5qrzyqz0?embed" width="400" height="400" style="border: 1px solid #ccc" frameborder=0></iframe></center>

!!! example "Example 2"
    Sketch a graph of the line $2x + y = 3$.

    ??? success "Solution"
        Let's pick the two $x$ values, $x = 2$ and $x = 0$. When $x = 2$, 

        $$2(2) + y = 3,$$

        $$4 + y = 3,$$

        $$y = 3-4 = -1.$$

        And when $x = 0$,

        $$2(0) + y = 3,$$

        $$y = 3.$$

        So we can plot the points $(2,-1)$ and $(0,3)$ and connect them with a line. 

        <!-- https://www.desmos.com/calculator/ijaood2xum -->

        <center><iframe src="https://www.desmos.com/calculator/ijaood2xum?embed" width="400" height="400" style="border: 1px solid #ccc" frameborder=0></iframe></center>

A **horizontal line** is a line with constant $y$ value, e.g. $y = 1$ or $y = -1/4$. A **vertical line** has constant $x$ value, e.g. $x = 0$ and $x=-2$.

## 1.2 Slope of a Line 

One way to determine a line is to know two points on the line. Another way we can realize a line is by knowing a *single* point on the line and the **slope** of the line. The slope of a line is a measure of its incline. We typically use the letter $m$ to denote slope. 

<span style="color: green;">Positive</span> slope mean the line trends up as you go to the right. <span style="color: red;">Negative</span> slope means the line trends down as you go to the right. The magnitude of the slope tells you the *steepness* of the line. 

!!! example "Example 3"
    Each graph below shows a linear function. Match each graph to one of the slopes provided: $m=1$, $m=3$, $m = -1/2$.

    1. <iframe src="https://www.desmos.com/calculator/6hjcpmtpzs?embed" width="200" height="200" style="border: 1px solid #ccc" frameborder=0></iframe>

    2. <iframe src="https://www.desmos.com/calculator/vwhtsqv6os?embed" width="200" height="200" style="border: 1px solid #ccc" frameborder=0></iframe>

    3. <iframe src="https://www.desmos.com/calculator/grcilwpms6?embed" width="200" height="200" style="border: 1px solid #ccc" frameborder=0></iframe>

    ??? success "Solution"
        Graph 2 goes down as you go to the right, therefore it has negative slope. That means graph 2 must have $m = -1/2$. Graph 1 and 3 both have positive slope, however graph 3 is clearly steeper. That means graph 1 has slope $m=1$ and graph 3 has slope $m=3$.

The slope of a line has the form, 

$$m = \frac{\text{change in }y}{\text{change in }x}.$$

Given any two points $(x_1,y_1)$ and $(x_2,y_2)$ on a line the slope is computed by, 

$$m = \frac{y_2 - y_1}{x_2 - x_1}.$$

Note that the points you use do not matter, however it is important to have consistent ordering in the numerator and denominator of the above expression.

!!! example "Example 4"
    A line passes through the points $(1,3)$ and $(5,7)$, what is the slope of the line?

    ??? success "Solution"
        Using the formula for slope, we can write

        $$m = \frac{7 - 3}{5 - 1} = \frac{4}{2} = 2.$$

!!! example "Example 5"
    What is the slope of the line given by the equation $2x + 3y = 1$. 

    ??? success "Solution"
        One way we can compute the slope is by finding any two points on the line and using the formula for slope. When $x=0$ we have, 

        $$2(0) + 3y = 1,$$

        $$y = 1/3.$$

        And when $x = 1$ we have, 

        $$2(1) + 3y = 1,$$

        $$2 + 3y = 1,$$

        $$3y = -1,$$

        $$y = -1/3$$

        Plugging this into the slope formula gives, 

        $$m = \frac{-\frac{1}{3} - \frac{1}{3}}{1-0} = \frac{-\frac{2}{3}}{1} = -\frac{2}{3}.$$

!!! info "Slope of Horizontal and Vertical Lines"
    A horizontal line has slope $m=0$. A vertical line has *undefined* slope. 

## 1.3 Determining the Equation of a Line 

The **y-intercept** of a line is the point where the line crosses the vertical $y$ axis. In other words, it is the value $b$ such that $(0,b)$ is on the line. 

!!! example "Example 6"
    What is the $y$-intercept of the line $2x + 4y = 10$?

    ??? success "Solution"
        Plug in $x=0$ and solve for the $y$ value,

        $$2(0) + 4y = 10,$$

        $$4y = 10,$$

        $$y = 10/4 = 5/2.$$

One of the most common ways to express a line is to use **slope-intercept form**. If a line has slope $m$ and $y$-intercept $b$, then the equation of the line is 

$$y = mx + b$$

!!! note "Reminder"
    Knowing a point on the line and the slope completely determine the line. The $y$-intercept is the point $(0,b)$. 

!!! example "Example 7"
    A line has slope $-3/4$ and $y$-intercept $(0,-2)$. What is the equation of the line?

    ??? success "Solution"
        Using slope-intercept form we have $m = -3/4$ and $b = -2$, thus

        $$y = -\frac{3}{4}x - 2.$$

!!! example "Example 8"
    Compute an equation for the line depicted below

    <center>
    <iframe src="https://www.desmos.com/calculator/8vszldzzms?embed" width="400" height="400" style="border: 1px solid #ccc" frameborder=0></iframe>
    </center>

    ??? success "Solution"
        Based on the graph, the line goes through the points $(0,-2)$ and $(4,0)$. We compute the slope,

        $$m = \frac{0 - (-2)}{4-0} = \frac{2}{4} = \frac{1}{2}.$$

        Thus the equation of the line is,

        $$y = \frac{1}{2}x-2.$$
        

This gives us a way to compute the slope of a line when given the equation of the line (in any form). To compute the slope we can put the equation in slope-intercept form and read off the slope. 

!!! example "Example 9"
    Compute the slope of the line $2y - 6x = 4$ by putting the line in slope-intercept form. 

    ??? success "Solution"
        To put the linear equation in slope intercept form, we should isolate $y$. First, move over the $x$ term 

        $$2y = 6x + 4,$$

        then divide, 

        $$y = 3x + 2.$$

        The slope of the line is $m=3$. 

Another common line form is **point-slope form**. Given *any* point on the line $(x_1,y_1)$ and slope $m$, the line can be expressed by the equation

$$y - y_1 = m(x-x_1)$$

or equivalently 

$$y = m(x-x_1) - y_1.$$

!!! example "Example 10"
    Compute the slope-intercept form of a line that passes through the point $(3,2)$ and has slope $4$. 

    ??? success "Solution"
        Using the equation for slope-intercept form we have, 

        $$y-2=4(x-3).$$

!!! example "Example 11"
    Edith and Eric are both computing the equation for the line that goes through the points $(-3,4)$ and $(3,0)$. Edith gets 

    $$y - 4 = -\frac{2}{3}(x+3)$$

    and Eric gets

    $$y = -\frac{2}{3}(x-3).$$

    Who is correct?

    ??? success "Solution"
        Both are correct! The slope of the line is 

        $$m = \frac{4 - 0}{-3 -3} = - \frac{4}{6} = - \frac{2}{3}.$$

        Using the point $(-3,4)$, point-slope form gives 

        $$y - 4 = -\frac{2}{3}(x+3),$$

        which is Edith's answer. Using the point $(3,0)$, point-slope form gives 

        $$y = -\frac{2}{3}(x-3)$$

        which is Eric's answer. 

The last linear equation form we will introduce is **standard form**. The standard form of a line is, 

$$Ax+By = C$$

where $A$, $B$, and $C$ are **integers**. If a line is in standard form, then the slope of the line is 

$$m = -\frac{A}{B}.$$

!!! example "Example 12"
    Put the following linear equation in standard form,

    $$y = -\frac{1}{2}x + 1.$$

    ??? success "Solution"
        We start by moving the $x$ term,

        $$y + \frac{1}{2}x = 1.$$

        Next, multiply by 2 so that all coefficients are integers, 

        $$2y + x = 2.$$


## 1.4 Applications

 Lines can be used to model real world relationships. In this section, we will introduce a couple examples of applications of lines.

!!! example "Example 13"
    It cost $750 to manufacture 25 items and $1000 to manufacture 50 items. If we assume a linear relation holds, find the cost equation and use this equation to compute the cost of manufacturing 100 items. 
    
    ??? success "Solution"
        Let $x =$ the number of items and $y =$ the cost of manufacturing. Thus the problem defines two points on the line, $(25,750)$ and $50,1000)$. We can compute the slope, 

        $$m = \frac{1000-750}{50-25} = \frac{250}{25} = 10.$$

        Now let's use point-slope form to write an equation,

        $$y - 1000 = 10(x - 50)$$

        rearranging gives, 

        $$y = 10x-500 + 1000 = 10x+500.$$

        So the cost of manufacturing 100 items is

        $$y = 10(100) + 500 = 1000+500 = 1500 \text{ dollars}.$$

When dealing with applications of lines, it is good to remember that $x$ represents the **inpout**, e.g. the information given, and $y$ represents the **output**, e.g. what we want to infer. In the above problem we *want to know* the cost when we are *given* the number of items manufactured. 

!!! example "Example 14"
    The freezing temperature of water is 0 degrees Celcius and 32 degrees Fahrenheit. The boiling temperature of water is 100 degrees Celcius and 212 degrees Fahrenheit. If Celcius and Fahrenheit are linearly related, write an equation that converts Celcius temperatures to Fahrenheit. 

    ??? success "Solution"
        From the information we have, we know two points on the line: $(0,32)$ and $(100,212)$. Note that the Celcius temperature is the $x$ coordinate becase we are converting Celcius *to* Fahrenheit. Compute the slope

        $$m = \frac{212-32}{100-0} = \frac{180}{100} = \frac{9}{5}.$$

        Note that the point $(0,32)$ is the $y$-intercept of the line. So we can use slope-intercept form, 

        $$y = \frac{9}{5}x + 32.$$

!!! example "Example 15"
    It costs $90 to rent a car and drive 100 miles and $140 to rent and drive it 200 miles. Write a cost function where $y=$ the total rental cost and $x=$ the number of miles driven. 


## 1.5 Linear Systems in Two Variables

Let's start by learning how to find the intersection point of two lines algebraically. Note that we can always try to carefully draw the two lines and use the graph to infer the answer, however this isn't always practical. Knowing how to solve for the answer algebraically will give use a precise answer, regardless of the lines involved.

!!! example "Example 16"
    Find the intersection point of the lines $y=3x-1$ and $y=7-x$.

    <center>
    <iframe src="https://www.desmos.com/calculator/o8aew52l6u?embed" width="300" height="300" style="border: 1px solid #ccc" frameborder=0></iframe>
    </center>

    ??? success "Solution"
        When the lines intersect they share the same $x$ and $y$ coordinate. This means we can set the $y$ values equal,

        $$3x-1=7-x.$$

        It's important to recognize that the $x$ values on each side of the equation represent the *same* number $x$. Now we can isolate $x$ and solve,

        $$4x-1=7$$

        $$4x = 8$$

        $$x = 2.$$

        So the lines intersect when $x=2$. To find the $y$ value of the intersection point, we can plug this $x$ value into *either* line (if we did the algebra right, of course). So we get, 

        $$y = 3(2) - 1 = 6-1=5.$$

        Checking both lines is a good way to be sure about our work,

        $$y = 7 - 2 = 5.$$

        Thus, the lines intersect at $(2,5)$. 

If both lines are presented as $y = \cdots$ then the above method is a great way of finding the intersection of two lines. Even if they are not written in this manner, we can rearrange them and then use the method above. 

If the lines are not written in the form $y=\dots$ it is sometimes easier to use a method called **elimination** instead of rewriting the equation. The idea behind the elimination method is adding the equations together to eliminate one of the variables. 

!!! warning "Elimination Method"
    The elimination method is typically viewed as more challenging when first learned, however the technique becomes very valuable when we increase to systems of 3 or more variables/equations. It is thus good to learn it now. 

!!! example "Example 17"
    Find the intersection of the lines $2y + 3x = 6$ and $y - 3x=3$.
    ??? success "Solution"
        We add the equations together like so, 

        $$\begin{array}
        2y & + 3x & =6 \\
        y & -3x & =3 \\
        \hline 
        3y & & =9
        \end{array}$$

        So we get $y=3$. We can plug this into either of the equations to get the $x$ value. 

        $$2(3) + 3x = 6,$$

        $$6 + 3x = 6,$$

        $$3x = 0 \implies x=0.$$

        The point of intersection is $(0,3)$.

In elimination, we can also multiply the equations by a constant to create the cancellation we desire. This is because multiplying a line by a constant does not change the line! For example, $x - y = 2$ is the same line as $2x - 2y = 4$. 

!!! example "Example 18"
    Use elimination to find the intersection of the lines $x - 2y = 1$ and $2x -3y = 4$. 
    ??? success "Solution"
        Let's multiply the first equation by $-2$, 

        $$-2x +4y = -2.$$

        Now we can add the two equations together, 

        $$\begin{array}
        -2x & + 4y & = -2\\
        2x & -3y & =4 \\
        \hline 
        y & & =2
        \end{array}$$

        Now plug $y=2$ into the original first equation, 

        $$x - 2(2) = 1,$$

        $$x = 5.$$


Some lines *never* intersect. These are known as **parallel lines**. Parallel lines have the same slope, but go through different points. For example, the lines $y=2x+1$ and $y=2x+5$ are parallel. 

<center>
<iframe src="https://www.desmos.com/calculator/nevqzdp8yq?embed" width="400" height="400" style="border: 1px solid #ccc" frameborder=0></iframe>
</center>

Notice that parallel lines look like train tracks, they always stay the same distance away from each other. 

### 1.5.1 Supply and Demand Curves

A **supply curve** describes how many items can be made available at a given price. A **demand curve** describes the number of items consumers will buy at different unit prices. The *input* ($x$ value) of a supply and demand curve is the price, the *output* is the number of items. 

As the price of a product increases, generally supply will increase but demand will decrease. The **equilibrium price** is reached when supply and demand are equal. 

!!! example "Example 19" 
    The supply curve for a product is $y = 35x-140$ and the demand curve is $y=-25x+340$. 

    1. How many items can be supplied at a cost of $10 per item?
    2. How many items will be demanded at a cost of $10 per item?
    3. What is the equilibrium price?

    ??? success "Solution"
        We plug $x = 10$ into the supply curve,

        $$y = 35(10) - 140 = 350 - 140 = 210.$$

        So $210$ items can be supplied at the cost of $\$10$ per item. Now plug $x = 10$ into the demand curve, 

        $$y = -25(10) + 340 = -250 + 340 = 90.$$

        So $90$ items will be bought. Notice that at $\$10$ there is more supply then demand. Set the $y$ values equal to solve for the equilibrium price, 

        $$35x-140 = -25x+340$$

        $$60x = 480$$

        $$x = 8.$$

        The equilibrium price is $\$8$. 

### 1.5.2 Break-Even Point

If a company sells an item for $P$ dollars, then the **revenue** is the price multiplied by the number of items sold, $R=Px$. The **production costs** are the sum of the variable and fixed costs. Typically written $C = mx+b$, where $x=$ the number of items manufactured. 

- The fixed cost is represented by $b$; it does not change no matter how much is produced. Think of the fixed cost as things such as manufacturing space and equipment. 
- The variable cost is $mx$, which depends on the amount being produced. We call $m$ the marginal cost, e.g. the cost of producing an additional item. 

**Profit** is $P = R-C$. We call the point when profit is 0 the **break-even** point. If costs are more than revenue, the company is operating at a loss. Geometrically, the break-even point is the point where the revenue and production costs lines intersect. 

!!! example "Example 20"
    If $R = 5x$ and $C = 3x+12$,

    1. What is the marginal cost? What is the fixed cost? 
    2. What is the revenue from producing 4 items?
    3. What is the cost of producing 4 items?
    4. What is the break-even point? 
    5. What will the revenue and cost be at the break-even point?

    ??? success "Solution"
        The cost function is $C = 3x+12$, so the marginal cost is $\$3$ and the fixed cost is $\$12$. The revenue from producing $4$ items is, $5(4) = 20$ dollars. The cost of producing $4$ items is, 

        $$C = 3(4) + 12 = 12 + 12 = 24 \text{ dollars}.$$

        The break-even point is when $C = R$, so we compute

        $$5x = 3x+12$$

        $$2x = 12$$

        $$x = 6 \text{ items.}$$

        The revenue and cost will be the *same* at the break-even, so we can compute either

        $$R = 5 (6) = 30 \text{ dollars}.$$

## Practice Problems

### 1.1 Exercises

Determine whether the following points are on the given line.

<div class="grid cards" markdown>

- **Problem 1.**

    $(1, 2)$ and $y = x + 1$.


- **Problem 2.**

    $(2,-2)$ and $y = -x + 4$.

- **Problem 3.**

    $(4, 1)$ and $y + 3x = 2$.


- **Problem 4.**

    $(2, -1)$ and $3x - y = 2$. 


</div>

Sketch a graph of the following lines by finding two points on the line. 

<div class="grid cards" markdown>

- **Problem 5.**

    $y = x + 1$.


- **Problem 6.**

    $y = 3x - 4$.


- **Problem 7.**

    $2y = x + 2$.


- **Problem 8.**

    $3x + y = 6$.


</div>

### 1.2 Exercises

Compute the slope of the line passing through the given points. 

<div class="grid cards" markdown>

- **Problem 9.**

    $(1,1)$ and $(3,0)$.


- **Problem 10.**

    $(4,-3)$ and $(5,5)$.


- **Problem 11.**

    $(-2,0)$ and $(0,-3)$.


- **Problem 12.**

    $(1,3)$ and $(1,0)$.


</div>

### 1.3 Exercises

Determine the slope of the following lines.

<div class="grid cards" markdown>

- **Problem 13.**

    $y = 3x-4$.


- **Problem 14.**

    $2y = x + 10$.


- **Problem 15.**

    $3x + 4y = 12$.


- **Problem 16.**

    $3x-y=1$.

</div>

Determine the equation of the line passing through the given points. Express the equation in slope-intercept form. 

<div class="grid cards" markdown>

- **Problem 13.**

    $(0,1)$ and $(1,2)$.


- **Problem 14.**

    $(0,0)$ and $(2,3)$.


- **Problem 15.**

    $(-3,1)$ and $(1,5)$.


- **Problem 16.**

    $(2,-1)$ and $(5,10)$.

</div>

**Problem 17.** Put the linear equation $y = 3x + 1$ in *standard form*.

**Problem 18.** Put the linear equation $y = x/2 - 3/4$ in *standard form*.

### 1.4 Exercises 

**Problem 19.** A taxi company charges a flat fee of $\$3.50$ plus $\$2.25$ per mile. Write an equation for the total cost $C$ of a ride of $m$ miles long. How much does a $12$ mile ride cost? 

**Problem 20.** A gardener measures a bamboo plant's height on two occasions. On day $4$ after planting, it was $22$ cm tall. On day $10$, it was $43$ cm tall. Assuming the plant's groth is linear, write an equation that gives the height of the plant $H$ in cm after $d$ days. How tall will the plant be after two weeks?

**Problem 21.** A tank contains $500$ gallons of water and is being drained at a rate of $20$ gallons per minute. Write an equation for the amount of water $W$ remaining after $t$ minutes. How much water is left after $8$ minutes? How long until the tank is empty?

### 1.5 Exercises

For the following problems compute the intersection point of the two lines. For problems 24 and 25 use the **elimination** method. 

<div class="grid cards" markdown>

- **Problem 22.**

    $y = 2x+1$ and $y=-x+7$.


- **Problem 23.**

    $y = 3x-4$ and $y=x+6$. 


- **Problem 24.**

    $2x+y=10$ and $x-y=2$.


- **Problem 25.**

    $3x+2y=12$ and $-2x+4y=8$.
    

</div>

**Problem 26.** In a race, Maria runs at $6$ meters per second. Jamal gets a $30$ meter head start but runs at only $4$ meters per second. How many seconds until Maria catches Jamal, and how far will she have run?

**Problem 27.** Gym A charges a $\$50$ signup fee plus $\$20$ per month. Gym B charges a $\$10$ signup fee plus $\$30$ per month. After how many months will the total cost be the same, and what is that cost?

**Problem 28.** At a farmers market, the weekly demand for honey is given by $D = 100 − 4p$, and the supply is given by $S = 20 + 6p$, where $p$ is the price per jar in dollars and quantities are in jars. (a) How many jars could be sold if they are priced at $\$10$ per jar? (b) Find the equilibrium price.

**Problem 29.** The demand for tickets to a local concert is $D = 900 − 15p$, and the venue's supply is $S = 10p + 150$, where $p$ is the ticket price in dollars. Find the equilibrium price and the number of tickets sold.

**Problem 30.** A student starts a T-shirt printing business. Equipment costs $\$600$, and each shirt costs $\$5$ to produce. She sells the shirts for $\$17$ each. Write the cost function and revenue function. How many shirts must she sell to break even, and what is the revenue at the break-even point?