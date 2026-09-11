# 2. Matrices

## 2.1 Basic Operations 

A **matrix** is a two-dimensional array of numbers. Whenever we discuss a matrix, we must denote it **dimensions** (or size). The dimensions of a matrix is the number of **rows** followed by the number of **columns**. For example, 

$$A = \begin{bmatrix} 
1 & -3 & 2 \\ 
12 & 6 & -1 
\end{bmatrix}$$

is a $2 \times 3$ matrix, meaning there are $2$ rows and $3$ columns. Typically, uppercase letters are used to denote matrices. 

!!! example "Example 1"
    State the dimensions of the following matrices, 

    $$A = \begin{bmatrix}
    1 & 3 \\
    2 & -4 \\
    0 & 0 \\
    1 & 6
    \end{bmatrix}, \quad 
    B = \begin{bmatrix}
    1 & 3 & 0 & 3\\
    2 & -4 & -1 & 6\\
    0 & 3 & 3 & 0
    \end{bmatrix}$$

    ??? success "Solution"
        Matrix $A$ has dimensions $4\times 2$ and matrix $B$ has dimensions $3\times 4$.

A matrix is called **square** if it has the same number of rows as columns. The **identity** matrix is a square matrix where the entries along the main diagonal are all 1 and all other entries are 0. For example, 

$$I = \begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1 
\end{bmatrix}$$

is the $3\times 3$ identity matrix. It is common to use the notation $I_n$ to denote the $n \times n$ identity matrix. If the dimensions are clear given the context, this notation is typically shortened to $I$. A matrix where either one of the dimensions is $1$, e.g. $1\times n$ or $n \times 1$, is referred to as a **vector**. For example, 

$$v = \begin{bmatrix}
1 \\
3 \\
0 \\
-1
\end{bmatrix}$$

is a $4 \times 1$ vector. We often use lowercase letters $v$, $u$ and $w$ to denote vectors. The above is referred to as a **column vector** since it is a matrix with a single column. Alternatively, 

$$u = \begin{bmatrix}
0 & -1 & 1 
\end{bmatrix}$$

is referred to as a **row vector** since it is a matrix with a single row. 

We can add and subtract matrices if they have the same dimensions. We add and subtract matrices *entrywise*. 

!!! example "Example 2"
    Compute $A+B$, where 

    $$A = \begin{bmatrix}
    1 & 3 \\
    2 & -4 \\
    0 & 0 \\
    1 & 6
    \end{bmatrix}, \quad
    B = \begin{bmatrix}
    2 & 2 \\
    0 & 10 \\
    5 & 1 \\
    1 & 1
    \end{bmatrix}.$$

    ??? success "Solution"
        $$A+B=\begin{bmatrix}
        1 & 3 \\
        2 & -4 \\
        0 & 0 \\
        1 & 6
        \end{bmatrix} +
        \begin{bmatrix}
        2 & 2 \\
        0 & 10 \\
        5 & 1 \\
        1 & 1
        \end{bmatrix} =
        \begin{bmatrix}
        1+2 & 3+2 \\
        2+0 & -4+10 \\
        0+5 & 0+1 \\
        1+1 & 6+1 
        \end{bmatrix} =
        \begin{bmatrix}
        3 & 5 \\
        2 & 6 \\
        5 & 1 \\
        2 & 7 
        \end{bmatrix}$$

!!! example "Example 3"
    Find, if possible: a) $A + B$, b) $A - B$, c) $A + C$, d) $B - C$, e) $C + D$.

    $$A = \begin{bmatrix}
    1 & 3 \\
    -2 & 4
    \end{bmatrix} \quad
    B = \begin{bmatrix}
    0 & -1 \\
    5 & 2
    \end{bmatrix} \quad
    C = \begin{bmatrix}
    1 & 0 & 2 \\
    3 & -1 & 4
    \end{bmatrix} \quad
    D = \begin{bmatrix}
    2 & 1 \\
    0 & -3 \\
    4 & 5
    \end{bmatrix}$$

    ??? success "Solution"
        a) 
        
        $$\begin{bmatrix} 1+0 & 3+(-1) \\ -2+5 & 4+2 \end{bmatrix} = \begin{bmatrix} 1 & 2 \\ 3 & 6 \end{bmatrix}$$

        b) 
        
        $$\begin{bmatrix} 1-0 & 3-(-1) \\ -2-5 & 4-2 \end{bmatrix} = \begin{bmatrix} 1 & 4 \\ -7 & 2 \end{bmatrix}$$

        c) Not possible. $A$ is $2 \times 2$ and $C$ is $2 \times 3$. Matrices must have the same dimensions to add.

        d) Not possible. $B$ is $2 \times 2$ and $C$ is $2 \times 3$. Matrices must have the same dimensions to subtract.

        e) Not possible. $C$ is $2 \times 3$ and $D$ is $3 \times 2$. Matrices must have the same dimensions to add.


Multiplying matrices is more complicated. There are two types of matrix multiplication we will define. The first is known as **scalar multiplication**. We can multiple a matrix by a single number (a scalar), by multiplying each entry by that value. 

!!! example "Example 4"
    Compute $2A$ and $-3B$, where

    $$A = \begin{bmatrix}
    3 & -1 \\
    0 & 4
    \end{bmatrix} \quad
    B = \begin{bmatrix}
    2 & -1 & 5 \\
    0 & 3 & -2
    \end{bmatrix}$$

    ??? success "Solution"
        The notation $2A$ denotes scalar multiplication of $A$ by $2$. This means we multiply each entry of $A$ by $2$,


        $$2A = \begin{bmatrix} 2(3) & 2(-1) \\ 2(0) & 2(4) \end{bmatrix} = \begin{bmatrix} 6 & -2 \\ 0 & 8 \end{bmatrix}$$

        To compute $-3B$ us the same method, 

        $$-3B = \begin{bmatrix} -3(2) & -3(-1) & -3(5) \\ -3(0) & -3(3) & -3(-2) \end{bmatrix} = \begin{bmatrix} -6 & 3 & -15 \\ 0 & -9 & 6 \end{bmatrix}$$

Next, we need to know **matrix multiplication**, i.e. how to multiply two matrices together. It's easiest to start by explaining how to multiply a row vector by a column vector, which is allowed if they have the same number of entries. To multiply a row vector by a column vector, you pair up the entries in order, multiply each pair, and then add all those products together to get a single number.

!!! example "Example 5"
    Compute $AB$, where 

    $$A = \begin{bmatrix} 
    2 & 10 
    \end{bmatrix}, \quad
    B = \begin{bmatrix}
    4 \\
    -1
    \end{bmatrix}.$$

    ??? success "Solution"
        We multiple the first entry of $A$ by the first entry in $B$ and the second entry in $A$ by the second entry in $B$. We then add these together to get, 

        $$AB = \begin{bmatrix} 
        2 & 10 
        \end{bmatrix}
        \begin{bmatrix}
        4 \\
        -1
        \end{bmatrix} = 
        \begin{bmatrix}
        2(4) + 10(-1)
        \end{bmatrix} = 
        \begin{bmatrix}
        8 - 10
        \end{bmatrix} = 
        \begin{bmatrix}
        -2
        \end{bmatrix} = -2.$$

        A $1 \times 1$ matrix is just a scalar. In order to perform this procedure, the row and column vector must have the same number of entries. 

!!! example "Example 6"
    Compute 

    $$\begin{bmatrix} 
    1 & 1 & 3 & -2 
    \end{bmatrix}
    \begin{bmatrix}
    2 \\
    -1 \\
    3 \\
    1
    \end{bmatrix}.$$

    ??? success "Solution"

        $$\begin{bmatrix} 
        1 & 1 & 3 & -2 
        \end{bmatrix}
        \begin{bmatrix}
        2 \\
        -1 \\
        3 \\
        1
        \end{bmatrix}=
        1(2) + 1(-1) + 3(3) + (-2)(1) = 2 -1 + 9 -2 = 8.$$






When multiplying scalars, the order of multiplication doesn't matter. For example, $5 \times 3 = 3 \times 5$. This is not the case when multiplying matrices! The order of multiplication matters in matrix multiplication. In other words, we say matrix multiplication is **noncommutative**. 

!!! note "When is matrix multiplication allowed?"
    We can multiply two matrices together only if the number of columns in the first matrix is equal to the number of rows in the second matrix. 

!!! example "Example 7"

    Determine whether the following multiplication is allowed (do not solve): a) $AB$, b) $BC$, c) $AC$. 

    $$A = \begin{bmatrix} 1 & -2 & 4 \\ 0 & 3 & 5 \end{bmatrix} \quad 
    B = \begin{bmatrix} 2 & 1 \\ -1 & 0 \\ 3 & 6 \end{bmatrix} \quad 
    C = \begin{bmatrix} 7 & -3 \\ 2 & 8 \end{bmatrix}$$

    ??? success "Solution"

        a) $AB$ is allowed, since $A$ has 3 columns and $B$ has 3 rows. 

        b) $BC$ is allowed, since $B$ has 2 columns and $C$ has 2 rows.

        c) $AC$ is not allowed, since $A$ has 3 columns and $C$ has 2 rows.

Let $A$ and $B$ be matrices such that $AB$ is computable. The first row of $AB$ is computed by taking the first row in $A$ and multiplying it by each column in $B$. The second row of $AB$ is computed by taking the second row of $A$ and multiplying it by each column in $B$. This process continues until we use all rows of $A$. For example

$$\begin{bmatrix}
a & b \\
c & d 
\end{bmatrix}
\begin{bmatrix}
e & f \\
g & h
\end{bmatrix} = 
\begin{bmatrix}
\begin{bmatrix} a & b \end{bmatrix}\begin{bmatrix} e \\ g \end{bmatrix} & 
\begin{bmatrix} a & b \end{bmatrix}\begin{bmatrix} f \\ h \end{bmatrix} \\
\begin{bmatrix} c & d \end{bmatrix}\begin{bmatrix} e \\ g \end{bmatrix} &
\begin{bmatrix} c & d \end{bmatrix}\begin{bmatrix} f \\ h \end{bmatrix}
\end{bmatrix} =
\begin{bmatrix}
ae+bg & af+bh \\
ce+dg & cf+dh
\end{bmatrix}.$$

!!! example "Example 8"
    Multiply, 

    $$\begin{bmatrix}
    1 & 1 \\
    3 & 0
    \end{bmatrix}
    \begin{bmatrix}
    2 & -1 \\
    1 & 2
    \end{bmatrix}.$$

    ??? success "Solution" 
        
        $$\begin{bmatrix}
        1 & 1 \\
        3 & 0
        \end{bmatrix}
        \begin{bmatrix}
        2 & -1 \\
        1 & 2
        \end{bmatrix} = 
        \begin{bmatrix}
        1(2)+1(1) & 1(-1)+1(2) \\
        3(1)+0(1) & 3(-1)+0(2)
        \end{bmatrix} = 
        \begin{bmatrix}
        3 & 1 \\
        3 & -3 
        \end{bmatrix}.$$

!!! example "Example 9"
    Let 

    $$A = 
    \begin{bmatrix}
    1 & 4 & 3 \\
    2 & -1 & -2
    \end{bmatrix}, \quad
    B = \begin{bmatrix}
    2 & 2 & -1\\
    0 & 1 & -4\\
    1 & 0 & 2
    \end{bmatrix}$$

    Compute $AB$.

    ??? success "Solution" 

        Each entry is a row of $A$ times a column of $B$:

        $$AB = 
        \begin{bmatrix}
        (1)(2) + (4)(0) + (3)(1) & (1)(2) + (4)(1) + (3)(0) & (1)(-1) + (4)(-4) + (3)(2) \\
        (2)(2) + (-1)(0) + (-2)(1) & (2)(2) + (-1)(1) + (-2)(0) & (2)(-1) + (-1)(-4) + (-2)(2)
        \end{bmatrix}$$

        $$AB = 
        \begin{bmatrix}
        5 & 6 & -11 \\
        2 & 3 & -2
        \end{bmatrix}$$

Notice in the above example that $A$ was $2\times 3$, $B$ was $3 \times 3$, and $AB$ was $2\times 3$. The product $AB$ does not necessarily have the same dimensions as $A$ or $B$. 

!!! note "Matrix Multiplication Dimensions"
    If $A$ is $n \times m$ and $B$ is $m \times k$, then $AB$ will be $n \times k$.  

!!! example "Example 10"
    Find, if possible: a) EF, b) FE, c) FH, d) GH, e) HG. 

    $$E = \begin{bmatrix}
    1 & 2 \\
    4 & 2 \\
    3 & 1 
    \end{bmatrix} \quad
    F = \begin{bmatrix}
    2 & -1 \\
    3 & 2 
    \end{bmatrix} \quad
    G = \begin{bmatrix}
    4 & 1 
    \end{bmatrix} \quad
    H = \begin{bmatrix}
    -3 \\
    -1 
    \end{bmatrix}$$

    ??? success "Solution"
        The sizes are: $E$ is $3 \times 2$, $F$ is $2 \times 2$, $G$ is $1 \times 2$, and $H$ is $2 \times 1$.

        a) 

        $$EF = 
        \begin{bmatrix}
        (1)(2) + (2)(3) & (1)(-1) + (2)(2) \\
        (4)(2) + (2)(3) & (4)(-1) + (2)(2) \\
        (3)(2) + (1)(3) & (3)(-1) + (1)(2)
        \end{bmatrix}
        =
        \begin{bmatrix}
        8 & 3 \\
        14 & 0 \\
        9 & -1
        \end{bmatrix}$$

        b) $F$ has 2 columns and $E$ has 3 rows, so $FE$ is **not defined**.

        c)

        $$FH = 
        \begin{bmatrix}
        (2)(-3) + (-1)(-1) \\
        (3)(-3) + (2)(-1)
        \end{bmatrix}
        =
        \begin{bmatrix}
        -5 \\
        -11
        \end{bmatrix}$$

        d)

        $$GH = 
        (4)(-3) + (1)(-1)
        =
        -13$$

        e)

        $$HG = 
        \begin{bmatrix}
        (-3)(4) & (-3)(1) \\
        (-1)(4) & (-1)(1)
        \end{bmatrix}
        =
        \begin{bmatrix}
        -12 & -3 \\
        -4 & -1
        \end{bmatrix}$$

When combining matrix operations, we should respect the usual order of operations (PEMDAS).

!!! example "Example 11"
    Given matrices $R$, $T$ and $S$, find $R - 2ST$. 

    $$R = \begin{bmatrix}
    1 & 0 & 1\\
    2 & 2 & 4 \\
    1 & 2 & 3
    \end{bmatrix} \quad
    S = \begin{bmatrix}
    2 & -1 & -1\\
    0 & 2 & -2 \\
    1 & 4 & 2
    \end{bmatrix} \quad
    T = \begin{bmatrix}
    1 & -1 & 0 \\
    3 & 1 & 2 \\
    2 & 2 & -2
    \end{bmatrix}$$

    ??? success "Solution"
        First compute the product $ST$:

        $$ST = 
        \begin{bmatrix}
        (2)(1) + (-1)(3) + (-1)(2) & (2)(-1) + (-1)(1) + (-1)(2) & (2)(0) + (-1)(2) + (-1)(-2) \\
        (0)(1) + (2)(3) + (-2)(2) & (0)(-1) + (2)(1) + (-2)(2) & (0)(0) + (2)(2) + (-2)(-2) \\
        (1)(1) + (4)(3) + (2)(2) & (1)(-1) + (4)(1) + (2)(2) & (1)(0) + (4)(2) + (2)(-2)
        \end{bmatrix}
        =
        \begin{bmatrix}
        -3 & -5 & 0 \\
        2 & -2 & 8 \\
        17 & 7 & 4
        \end{bmatrix}$$

        Next, multiply by the scalar $2$:

        $$2ST = 
        \begin{bmatrix}
        -6 & -10 & 0 \\
        4 & -4 & 16 \\
        34 & 14 & 8
        \end{bmatrix}$$

        Finally, subtract from $R$:

        $$R - 2ST = 
        \begin{bmatrix}
        1 - (-6) & 0 - (-10) & 1 - 0 \\
        2 - 4 & 2 - (-4) & 4 - 16 \\
        1 - 34 & 2 - 14 & 3 - 8
        \end{bmatrix}
        =
        \begin{bmatrix}
        7 & 10 & 1 \\
        -2 & 6 & -12 \\
        -33 & -12 & -5
        \end{bmatrix}$$


## 2.2 Systems as Matrix Equations

In the last chapter, we learned how to solve systems with two unknowns and two equations such as 

$$x + 2y = 5$$

$$3x - 2y = -1$$

We can represent systems like these as **matrix equations**. Using matrices will present an organized way to solve the system. This method will extend to systems with $n$ equations and $n$ variables. 

Let $A$ be the matrix, 

$$A = \begin{bmatrix}
1 & 2 \\
3 & -2
\end{bmatrix},$$

and let $X$ be the vector

$$X = \begin{bmatrix}
x \\
y 
\end{bmatrix}.$$

Then notice that 

$$AX = \begin{bmatrix}
2x+y \\
3x - 2y
\end{bmatrix}$$

which is eactly the left hand side of both out initial equations. If we then let

$$B = \begin{bmatrix}
5 \\
-1
\end{bmatrix}$$

the matrix equation $AX = B$ exactly encodes our original system of equations. 

!!! example "Example 12"
    Write the system 

    $$2x + 3y = 4$$

    $$-x+4y = -3$$

    as a matrix equation. 

    ??? success "Solution"
        We write, 

        $$\begin{bmatrix}
        2 & 3 \\
        -1 & 4 
        \end{bmatrix}
        \begin{bmatrix}
        x \\
        y
        \end{bmatrix} = 
        \begin{bmatrix}
        4 \\
        -3
        \end{bmatrix}.$$

!!! example "Example 13"
    Write the system 

    $$y = 3x - 10$$

    $$2y - 2x = 0$$

    as a matrix equation. 

    ??? success "Solution"
        First rewrite the first equation as $y - 3x = -10$. Now we can write, 

        $$\begin{bmatrix}
        1 & -3 \\
        2 & -2 
        \end{bmatrix}
        \begin{bmatrix}
        x \\
        y
        \end{bmatrix} = 
        \begin{bmatrix}
        -10 \\
        0
        \end{bmatrix}.$$

This idea extends to any number of equations and variables. We just need to choose the appropriate size matrix. 

!!! example "Example 12"
    Write the system 

    $$x-y+4z= 1$$

    $$2x + 3y - z=-2$$

    $$3x - 4z = 3$$

    as a matrix equation. 

    ??? success "Solution"
        Notice the third equation has no $y$ variable. That is okay, we make the coefficient $0$ in this case. 

        $$\begin{bmatrix}
        1 & -1 & 4\\
        2 & 3 & -1 \\
        3 & 0 & -4
        \end{bmatrix}
        \begin{bmatrix}
        x \\
        y \\
        z
        \end{bmatrix} = 
        \begin{bmatrix}
        1 \\
        -2 \\
        3
        \end{bmatrix}.$$

If we has a *scalar* equation $ax = b$, solving for $x$ would be simple--just divide both sides by $a$. We never defined division for matrices though and, in fact, the idea of division isn't exactly transferable. In the following section we will tackle methods for solving the matrix equation $AX = B$.

## 2.3 Gaussian Elimination

The next step is to actually solve the matrix equation. Here we introduce a procedure known as **Gaussian elimination**. Let's consider the initial example introduced in Section 2.2. This had the matrix form 

$$\begin{bmatrix}
1 & 2 \\
3 & -2
\end{bmatrix}
\begin{bmatrix}
x \\
y 
\end{bmatrix} = 
\begin{bmatrix}
5 \\
-1
\end{bmatrix}$$

From this we can write the **augmented matrix**

$$\begin{bmatrix}
1 & 2 & | & 5\\
3 & -2 & | & -1
\end{bmatrix}$$

where we append $B$ to $A$. We will be performing a series of operations which mirror the *elimination* method describe in Section 1.5. Our goal is to obtain all 0s below the $A$ diagonal. The allowed operations are the following:

- swap rows, 
- multiple or divide a row by a constant,
- add or subtract a multiple of a row from another. 

In the example being worked, let's first multiple the top row by $-3$ then add it to the second row. This new expression will replace the second row,

$$\begin{bmatrix}
1 & 2 & | & 5\\
3 + 1(-3) & -2+2(-3) & | & -1+5(-3)
\end{bmatrix} =
\begin{bmatrix}
1 & 2 & | & 5\\
0 & -8 & | & -16
\end{bmatrix}$$

Notice that this created a 0 in the lower left entry! Next, let's divide the second row by -8,

$$\begin{bmatrix}
1 & 2 & | & 5\\
0 & 1 & | & 2
\end{bmatrix}$$

If we translate this back into a system of equations it is already much easier to solve, 

$$ x + 2y = 5$$

$$y = 2$$

The $A$ side of the augemented matrix is in **row echelon form** (REF). When a matrix is in REF, all entries below the diagonal are 0. This is enough for finding a solution, although some like to go even further, to **reduced row echelon form** (RREF). In RREF, we change all diagonal entries to 1 and all non-diagonal entries to 0 *if possible*. Note that there are some systems where we cannot completely eliminate the other terms. 

Let's put the augemented matrix into RREF. To do so, we need to multiply the second row by $-2$ and add it to the first row. This new expression will replace the first row,

$$\begin{bmatrix}
1 & 0 & | & 1\\
0 & 1 & | & 2
\end{bmatrix}$$

Now we can really just read off the system solution, $x = 1$ and $y = 2$. Go ahead and check that this solves the system in its original form!

!!! example "Example 13"
    Solve the following system using Gaussian elimination,

    $$3x + 2y = 12$$

    $$x - y = 1$$

    ??? success "Solution"
        Let's first write the augmented matrix,

        $$\begin{bmatrix}
        3 & 2 & | & 12 \\
        1 & -1 & | & 1
        \end{bmatrix}$$

        It is best to have a 1 in the upper left corner. Let's swap the first and second row,

        $$\begin{bmatrix}
        1 & -1 & | & 1 \\
        3 & 2 & | & 12
        \end{bmatrix}$$

        Now let's use the first row to make every other entry in the first column 0. Add $-3$ times the first row to the second,

        $$\begin{bmatrix}
        1 & -1 & | & 1 \\
        0 & 5 & | & 9
        \end{bmatrix}$$

        Divide the second row by $5$,

        $$\begin{bmatrix}
        1 & -1 & | & 1 \\
        0 & 1 & | & \frac{9}{5}
        \end{bmatrix}$$

        Now use the 1 in the $(2,2)$ position to eliminate the $-1$ above it. Add the second row to the first,

        $$\begin{bmatrix}
        1 & 0 & | & \frac{14}{5} \\
        0 & 1 & | & \frac{9}{5}
        \end{bmatrix}$$

        Now we can read off the solution $x = \dfrac{14}{5}$ and $y = \dfrac{9}{5}$.

!!! example "Example 14" 
    Solve the following system using Gaussian elimination,

    $$2x+y+2z=10$$

    $$x+2y+z=8$$

    $$3x+y-z=2$$

    ??? success "Solution"
        Let's first write the augmented matrix, 

        $$\begin{bmatrix}
        2 & 1 & 2 & | & 10 \\
        1 & 2 & 1 & | & 8 \\
        3 & 1 & -1 & | & 2
        \end{bmatrix}$$

        It is best to have a 1 in the upper left corner. We could divide the top row by 2, but that would introduce fractions. Instead, let's swap the first and second row. 

        $$\begin{bmatrix}
        1 & 2 & 1 & | & 8 \\
        2 & 1 & 2 & | & 10 \\
        3 & 1 & -1 & | & 2
        \end{bmatrix}$$

        Now let's use the first row to make every other entry in the first column 0. Start by adding $-2$ times the first row to the second,

        $$\begin{bmatrix}
        1 & 2 & 1 & | & 8 \\
        0 & -3 & 0 & | & -6 \\
        3 & 1 & -1 & | & 2
        \end{bmatrix}$$

        Then add $-3$ times the first row to the third row, 

        $$\begin{bmatrix}
        1 & 2 & 1 & | & 8 \\
        0 & -3 & 0 & | & -6 \\
        0 & -5 & -4 & | & -22
        \end{bmatrix}$$

        Next let's divide the second row by $-3$,

        $$\begin{bmatrix}
        1 & 2 & 1 & | & 8 \\
        0 & 1 & 0 & | & 2 \\
        0 & -5 & -4 & | & -22
        \end{bmatrix}$$

        Now we can use the 1 in the $(2,2)$ position to make all the other entries in the second column 0. 

        $$\begin{bmatrix}
        1 & 0 & 1 & | & 4 \\
        0 & 1 & 0 & | & 2 \\
        0 & -5 & -4 & | & -22
        \end{bmatrix}$$

        $$\begin{bmatrix}
        1 & 0 & 1 & | & 4 \\
        0 & 1 & 0 & | & 2 \\
        0 & 0 & -4 & | & -12
        \end{bmatrix}$$

        Divide the third row by $-4$, 

        $$\begin{bmatrix}
        1 & 0 & 1 & | & 4 \\
        0 & 1 & 0 & | & 2 \\
        0 & 0 & 1 & | & 3
        \end{bmatrix}$$

        Lastly, eliminate the 1 in the $(1,3)$ position by subtracting the third row from the first, 

        $$\begin{bmatrix}
        1 & 0 & 0 & | & 1 \\
        0 & 1 & 0 & | & 2 \\
        0 & 0 & 1 & | & 3
        \end{bmatrix}$$

        Now we can read off the solution $x=1$, $y=2$, and $z=3$. 

Notice that we follow a predictable procedure, although the exact algebra needed will vary. We start by making the $(1,1)$ position a 1. Next, use that 1 to make all other entries in column 1 equal to 0. Then, make the $(2,2)$ entry a 1 and use that entry to make all the other entries in column 2 equal to 0. This procedure continues until we've addressed all rows. 

## 2.4 Inverse Matrices 

Let $A$ be a square matrix. The **inverse** of $A$, denoted $A^{-1}$, is the matrix satisfying

$$AA^{-1} = A^{-1}A = I,$$

where $I$ is the identity matrix with the appropriate dimensions. 

!!! example "Example 15"
    Verify that $B$ is the inverse of $A$, where

    $$A = \begin{bmatrix}
    2 & 1 \\
    5 & 3
    \end{bmatrix} \quad
    B = \begin{bmatrix}
    3 & -1 \\
    -5 & 2
    \end{bmatrix}$$

    ??? success "Solution"
        We need to verify that $AB = BA = I$. First compute $AB$,

        $$AB = \begin{bmatrix} 2 & 1 \\ 5 & 3 \end{bmatrix}\begin{bmatrix} 3 & -1 \\ -5 & 2 \end{bmatrix} = \begin{bmatrix} 2(3)+1(-5) & 2(-1)+1(2) \\ 5(3)+3(-5) & 5(-1)+3(2) \end{bmatrix} = \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix}$$

        Then compute $BA$,

        $$BA = \begin{bmatrix} 3 & -1 \\ -5 & 2 \end{bmatrix}\begin{bmatrix} 2 & 1 \\ 5 & 3 \end{bmatrix} = \begin{bmatrix} 3(2)+(-1)(5) & 3(1)+(-1)(3) \\ -5(2)+2(5) & -5(1)+2(3) \end{bmatrix} = \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix}$$

        Since $AB = BA = I$, $B$ is the inverse of $A$.

!!! example "Example 16"
    Verify that $B$ is the inverse of $A$, where

    $$A = \begin{bmatrix}
    1 & 2 & 0 \\
    0 & 1 & 3 \\
    0 & 0 & 1
    \end{bmatrix} \quad
    B = \begin{bmatrix}
    1 & -2 & 6 \\
    0 & 1 & -3 \\
    0 & 0 & 1
    \end{bmatrix}$$

    ??? success "Solution"
        We need to verify that $AB = BA = I$. First compute $AB$,

        $$AB = \begin{bmatrix} 1 & 2 & 0 \\ 0 & 1 & 3 \\ 0 & 0 & 1 \end{bmatrix}\begin{bmatrix} 1 & -2 & 6 \\ 0 & 1 & -3 \\ 0 & 0 & 1 \end{bmatrix}$$

        $$= \begin{bmatrix} 1(1)+2(0)+0(0) & 1(-2)+2(1)+0(0) & 1(6)+2(-3)+0(1) \\ 0(1)+1(0)+3(0) & 0(-2)+1(1)+3(0) & 0(6)+1(-3)+3(1) \\ 0(1)+0(0)+1(0) & 0(-2)+0(1)+1(0) & 0(6)+0(-3)+1(1) \end{bmatrix} = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix}$$

        Then compute $BA$,

        $$BA = \begin{bmatrix} 1 & -2 & 6 \\ 0 & 1 & -3 \\ 0 & 0 & 1 \end{bmatrix}\begin{bmatrix} 1 & 2 & 0 \\ 0 & 1 & 3 \\ 0 & 0 & 1 \end{bmatrix}$$

        $$= \begin{bmatrix} 1(1)+(-2)(0)+6(0) & 1(2)+(-2)(1)+6(0) & 1(0)+(-2)(3)+6(1) \\ 0(1)+1(0)+(-3)(0) & 0(2)+1(1)+(-3)(0) & 0(0)+1(3)+(-3)(1) \\ 0(1)+0(0)+1(0) & 0(2)+0(1)+1(0) & 0(0)+0(3)+1(1) \end{bmatrix} = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix}$$

        Since $AB = BA = I$, $B$ is the inverse of $A$.

A matrix must be square in order to have an inverse, however not all square matrices are **invertible** (e.g. have an inverse). For example, 

$$\begin{bmatrix}
1 & 0 \\
0 & 0
\end{bmatrix}$$

does not have an inverse. Let's see this by multiplying by a generic matrix, 

$$\begin{bmatrix}
1 & 0 \\
0 & 0
\end{bmatrix}
\begin{bmatrix}
a & b \\
c & d
\end{bmatrix} = 
\begin{bmatrix}
a & b \\
0 & 0
\end{bmatrix}.$$

There is no matrix that we can multiply by to get a $1$ appearing in the $(2,2)$ entry, therefore the matrix is not invertible.

If we have the (matrix) system, 

$$AX = B$$

and $A$ is invertible, then we can solve by multiplying both sides *on the left* by $A^{-1}$,

$$A^{-1}AX = A^{-1}B$$

$$X = A^{-1}B$$

!!! warning "Matrix Multiplication is Noncommutative!"

    Remember the order matters in matrix multiplication. Since I want $A^{-1}$ to be directly next to $A$, I should multiply on the left. That means on the other side of the equation I should also multiply on the left!

!!! example "Example 17"
    Solve the system, 

    $$\begin{bmatrix}
    2 & 1 \\
    5 & 3
    \end{bmatrix}
    \begin{bmatrix}
    x \\
    y
    \end{bmatrix} = 
    \begin{bmatrix}
    1 \\
    4
    \end{bmatrix}$$

    ??? success "Solution"
        Recall from Example 15 that the inverse of 

        $$\begin{bmatrix}
        2 & 1 \\
        5 & 3
        \end{bmatrix}$$

        is 

        $$\begin{bmatrix}
        3 & -1 \\
        -5 & 2
        \end{bmatrix}.$$

        So we can multiply, 

        $$\begin{bmatrix}
        3 & -1 \\
        -5 & 2
        \end{bmatrix}
        \begin{bmatrix}
        2 & 1 \\
        5 & 3
        \end{bmatrix}
        \begin{bmatrix}
        x \\
        y
        \end{bmatrix} = 
        \begin{bmatrix}
        3 & -1 \\
        -5 & 2
        \end{bmatrix}
        \begin{bmatrix}
        1 \\
        4
        \end{bmatrix}$$

        $$
        \begin{bmatrix}
        x \\
        y
        \end{bmatrix} = 
        \begin{bmatrix}
        -1 \\
        3
        \end{bmatrix}$$

Given a matrix, how do we compute it's inverse? We can use Gaussian elimination. If $A$ is an $n \times n$ matrix, we write the augmented matrix, 

$$\begin{bmatrix}
A & | & I_n
\end{bmatrix}.$$

Next, we use our valid row operations and simplify until the left hand side of the augmented matrix is simplified to $I_n$ (in other words, put it in RREF). If this is not possible, the matrix is not invertible. Once this is accomplished, the right hand we be $A^{-1}$. Let's see this on the matrix used in Example 15 and Example 17,

$$\begin{bmatrix}
2 & 1 & | & 1 & 0 \\
5 & 3 & | & 0 & 1 
\end{bmatrix}$$

Start by dividing the first row by $2$, 

$$\begin{bmatrix}
1 & 1/2 & | & 1/2 & 0 \\
5 & 3 & | & 0 & 1 
\end{bmatrix}$$

Next multiply the first row by $-5$ and add it to the second row, 

$$\begin{bmatrix}
1 & 1/2 & | & 1/2 & 0 \\
0 & 1/2 & | & -5/2 & 1 
\end{bmatrix}$$

Next, subtract the second row from the first, 

$$\begin{bmatrix}
1 & 0 & | & 3 & -1 \\
0 & 1/2 & | & -5/2 & 1 
\end{bmatrix}$$

Lastly, multiply the second row by $2$,

$$\begin{bmatrix}
1 & 0 & | & 3 & -1 \\
0 & 1 & | & -5 & 2 
\end{bmatrix}$$

See that the right hand side above is the inverse of our original matrix. 

!!! example "Example 18"
    Find the inverse of $A$, where

    $$A = \begin{bmatrix}
    1 & 2 & 1 \\
    0 & 1 & 3 \\
    2 & 3 & 0
    \end{bmatrix}$$

    ??? success "Solution"
        We form the augmented matrix $[A | I]$,

        $$\begin{bmatrix}
        1 & 2 & 1 & | & 1 & 0 & 0 \\
        0 & 1 & 3 & | & 0 & 1 & 0 \\
        2 & 3 & 0 & | & 0 & 0 & 1
        \end{bmatrix}$$

        We already have a 1 in the upper left corner. Use the first row to eliminate the 2 in the $(3,1)$ position by adding $-2$ times the first row to the third,

        $$\begin{bmatrix}
        1 & 2 & 1 & | & 1 & 0 & 0 \\
        0 & 1 & 3 & | & 0 & 1 & 0 \\
        0 & -1 & -2 & | & -2 & 0 & 1
        \end{bmatrix}$$

        Now use the 1 in the $(2,2)$ position to eliminate the entries above and below it. Add $-2$ times the second row to the first,

        $$\begin{bmatrix}
        1 & 0 & -5 & | & 1 & -2 & 0 \\
        0 & 1 & 3 & | & 0 & 1 & 0 \\
        0 & -1 & -2 & | & -2 & 0 & 1
        \end{bmatrix}$$

        Then add the second row to the third,

        $$\begin{bmatrix}
        1 & 0 & -5 & | & 1 & -2 & 0 \\
        0 & 1 & 3 & | & 0 & 1 & 0 \\
        0 & 0 & 1 & | & -2 & 1 & 1
        \end{bmatrix}$$

        Now use the 1 in the $(3,3)$ position to eliminate the entries above it. Add $5$ times the third row to the first,

        $$\begin{bmatrix}
        1 & 0 & 0 & | & -9 & 3 & 5 \\
        0 & 1 & 3 & | & 0 & 1 & 0 \\
        0 & 0 & 1 & | & -2 & 1 & 1
        \end{bmatrix}$$

        Then add $-3$ times the third row to the second,

        $$\begin{bmatrix}
        1 & 0 & 0 & | & -9 & 3 & 5 \\
        0 & 1 & 0 & | & 6 & -2 & -3 \\
        0 & 0 & 1 & | & -2 & 1 & 1
        \end{bmatrix}$$

        We have reached reduced row echelon form, so we can read off the inverse,

        $$A^{-1} = \begin{bmatrix}
        -9 & 3 & 5 \\
        6 & -2 & -3 \\
        -2 & 1 & 1
        \end{bmatrix}$$

Depending on the size of the matrix, there are formulas one can use to deduce the inverse. Here we will only present the formula for the inverse of a $2 \times 2$ matrix. Given a matrix, 

$$A = \begin{bmatrix}
a & b \\
c & d
\end{bmatrix}$$

the inverse is, 

$$ A^{-1} = \frac{1}{ad-bc} \begin{bmatrix}
d & -b \\
-c & a
\end{bmatrix}$$

provided $ad - bc \neq 0$. If $ad-bc = 0$, then the matrix has no inverse. 

## 2.5 Markov Processes

A **transition matrix**, or stochastic matrix, is a square matrix satisfying the following properties:

- Every entry is between 0 and 1 (inclusive).
- The sum of the entries from any column is 1. 

Note that while the columns must sum to 1, the rows do not need to. For example, 

$$\begin{bmatrix}
0.2 & 0.5 \\
0.8 & 0.5
\end{bmatrix}$$

is a transition matrix. The entries of a transition matrix typically represent **transition probabilities**. The rows and columns represent **states** of the system. The matrix entry $(i,j)$ (where $i$ and $j$ are states) represents the probability of transitioning from state $j$ to state $i$. 

!!! warning "Transition Matrix Convention"
    Some texts will use an alternate convention than the one presented here for transition matrices. Sometimes the convention used is that the *rows* sum to 1, not the columns. The difference in convention changes how algebra is performed, since order of multiplication matters for matrices. If you are using alternate sources, make sure the convention is the same as the one presented here!

!!! example "Example 19"
    Consider a small community with two bike share stations. Residents who take a bike from a station may return the bike to either station. Of bikes located at station 1 at the beginning of the day, $20\%$ are at station 1 at the end of the day and $80\%$ are at station 2 at the end of the day. Of the bikes located at station 2, $50\%$ are at station 1 at the end of the day and $50\%$ are at station 2 at the end of the day. Write a transition matrix which represents this information. 

    ??? success "Solution"
        We let the matrix entry $(i,j)$ represent the probability that a bike at station $j$ ends up at station $i$. For example, the entry $(1,2)$ should be the probability that a bike taken from station 2 ends up at station 1. We get the transition matrix, 

        $$\begin{bmatrix}
        0.2 & 0.5 \\
        0.8 & 0.5
        \end{bmatrix}.$$  

A **Markov process** is a system that moves between states over time, where the probability of moving to the next state depends only on the current state. This is useful for modeling things like customer brand loyalty, market share, or population movement. The probabilities of moving from one state to the next are given by the transition matrix. The **state vector** $v_n$ gives the probability of being in each state at time step $n$.

To find the state at the next time step, we multiply,

$$v_{n+1} = Tv_n.$$

!!! example "Example 20"
    The movement of the bikes in Example 19 can be viewed as a Markov process. On a given day $40\%$ of the bikes are located at station 1. What proportion of bikes will be at station 1 at the end of the day?

    ??? success "Solution"  
        The state vector is, 

        $$v_0 = \begin{bmatrix}
        0.4 \\
        0.6 \end{bmatrix}$$

        which represents station 1 having $40\%$ of the bikes and station 2 having the other $60\%$ of the bikes. To compute the next state, we multiply

        $$v_1 = \begin{bmatrix}
        0.2 & 0.5 \\
        0.8 & 0.5
        \end{bmatrix}  
        \begin{bmatrix}
        0.4 \\
        0.6 \end{bmatrix} = 
        \begin{bmatrix}
        0.38 \\
        0.62
        \end{bmatrix}.$$

        So at the end of the day, station 1 will have $38\%$ of the bikes. 

A **stationary** or steady state vector $v$ satisfies $Tv = v$, meaning the distribution no longer changes over time. To find it we solve,

$$(I-T)v = \mathbf{0}$$

subject to the condition that the entries of $v$ sum to 1. The notation $\mathbf{0}$ is used to represent the column vector containing only 0s. 

!!! example "Example 21"
    Find the stationary vector for the Markov process described in Example 19. 

    ??? success "Solution"
        We wish to solve, 

        $$\begin{bmatrix}
        0.8 & -0.5 \\
        -0.8 & 0.5
        \end{bmatrix}
        \begin{bmatrix}
        s_1 \\
        s_2 
        \end{bmatrix} = 
        \begin{bmatrix}
        0 \\
        0 
        \end{bmatrix}.$$

        Let's write this matrix expression as scalar equations, 

        $$ 0.8s_1 - 0.5s_2 = 0$$

        $$-0.8s_1 + 0.5s_2 = 0$$

        Notice that these equations are essentially the same. This can be seen by multiplying the first by $-1$, which turns it into the second equation. Solving the first equation we get, 

        $$s_1 = \frac{5}{8}s_2.$$

        This is where the second condition on the stationary vector comes in. We require that $s_1+s_2 = 1$. Plugging the above in, 

        $$\frac{5}{8}s_2 + s_2 = 1$$

        $$\frac{13}{8}s_2 = 1$$

        $$s_2 = \frac{8}{13}$$

        and then 

        $$s_1 = \frac{5}{13}.$$ 
        
If a Markov process has a *unique* stationary vector, then it has an important physical meaning. Regardless of the initial state of our Markov process, if we run the process for enough time it will tend towards the stationary state. So for our bike station problem. Regardless of how many bikes start at station 1 and 2 we expect that for large enough $n$

$$v_n \approx \begin{bmatrix}
5/13 \\
8/13
\end{bmatrix} \approx 
\begin{bmatrix}
0.3846 \\
0.6154
\end{bmatrix}.$$

Let's see this in action by considering two different settings: 

- Case 1: all the bikes are initially at station 1. 
- Case 2: all the bike are initially at station 2. 

For case 1, the initial state vector is 

$$v_0 = \begin{bmatrix} 1 \\ 0\end{bmatrix}$$

Let's compute the proportion of bikes at each station after 100 days, in other words we want to compute $v_{100}$. We can do this by noticing a pattern and using technology. We start with, 

$$v_1 = Tv_0$$

where $T$ is the transition matrix. Repeating this pattern we get, 

$$v_2 = Tv_1 = T T v_0 = T^2v_0,$$

$$v_3 = Tv_2 = T T^2 v_0 = T^3 v_0.$$

Above we use exponent notation as short hand. 

!!! warning "Powers of Matrices"
    We use powers of matrices to denote repetative multiplication. When we write $T^2$ we *do not* mean the the entries of $T$ are squared, we mean to multiply $TT$. 

    E.g. let 

    $$A = \begin{bmatrix} 1 & 2 \\ -1 & 3 \end{bmatrix}$$

    then 

    $$A^2 = \begin{bmatrix} -1 & 8 \\ -4 & 7 \end{bmatrix}.$$

If we continue this pattern, we see that 

$$v_{100} = T^{100}v_0$$

Plugging this into a calculator gives, 

$$v_{100} \approx 
\begin{bmatrix}
0.3846 \\
0.6154
\end{bmatrix}.$$

We can take the same approach for case 2. This time let 

$$u_0 = \begin{bmatrix} 0 \\ 1 \end{bmatrix}$$

then 

$$u_{100} = T^{100} u_0 \approx \begin{bmatrix}
0.3846 \\
0.6154
\end{bmatrix}$$

also! These examples illustrate that after a long period of time it didn't matter where the bikes started, eventually the proportion of bikes at each station will be the same. 


!!! warning "Stationary Vector Existence and Uniqueness"
    One should note that the existence and uniqueness of the stationary vector is not automatic and requires conditions we will not discuss in this course. If you are asked to compute the stationary vector, assume it exists. 

!!! example "Example 20"
    Two coffee shops, Brew Co. and Daily Grind, compete for customers. Each month, Brew Co. retains 80% of its customers and loses 20% to Daily Grind. Daily Grind retains 70% of its customers and loses 30% to Brew Co. Currently, Brew Co. has 90% of the market and Daily Grind has 10%.

    a) Write the transition matrix.

    b) Find the market share after 1 and 2 months.

    c) Find the long-run steady state market share.

    ??? success "Solution"
        a) The transition matrix is

        $$T = \begin{bmatrix} 0.8 & 0.3 \\ 0.2 & 0.7 \end{bmatrix}$$

        where the first row/column corresponds to Brew Co. and the second to Daily Grind. Notice each column sums to 1.

        b) The initial state vector is $\mathbf{s}_0 = \begin{bmatrix} 0.9 \\ 0.1 \end{bmatrix}$. After one month,

        $$\mathbf{s}_1 = T\mathbf{s}_0 = \begin{bmatrix} 0.8 & 0.3 \\ 0.2 & 0.7 \end{bmatrix}\begin{bmatrix} 0.9 \\ 0.1 \end{bmatrix} = \begin{bmatrix} 0.8(0.9)+0.3(0.1) \\ 0.2(0.9)+0.7(0.1) \end{bmatrix} = \begin{bmatrix} 0.75 \\ 0.25 \end{bmatrix}$$

        After two months,

        $$\mathbf{s}_2 = T\mathbf{s}_1 = \begin{bmatrix} 0.8 & 0.3 \\ 0.2 & 0.7 \end{bmatrix}\begin{bmatrix} 0.75 \\ 0.25 \end{bmatrix} = \begin{bmatrix} 0.8(0.75)+0.3(0.25) \\ 0.2(0.75)+0.7(0.25) \end{bmatrix} = \begin{bmatrix} 0.675 \\ 0.325 \end{bmatrix}$$

        Notice Brew Co.'s market share is declining from 90% toward an equilibrium.

        c) To find the steady state we solve $T\mathbf{s} = \mathbf{s}$, or equivalently $(T-I)\mathbf{s} = \mathbf{0}$,

        $$\begin{bmatrix} -0.2 & 0.3 \\ 0.2 & -0.3 \end{bmatrix}\begin{bmatrix} p \\ q \end{bmatrix} = \begin{bmatrix} 0 \\ 0 \end{bmatrix}$$

        The first equation gives $-0.2p + 0.3q = 0$, so $p = 1.5q$. Using the condition $p + q = 1$,

        $$1.5q + q = 1 \implies 2.5q = 1 \implies q = 0.4, \quad p = 0.6$$

        In the long run, Brew Co. will hold 60% of the market and Daily Grind will hold 40%, regardless of the starting distribution.

## Practice Problems

### 2.1 Exercises

State the dimensions of the following matrices.

<div class="grid cards" markdown>

- **Problem 1.**

    $$A = \begin{bmatrix} 1 & 0 \\ -2 & 3 \\ 4 & 1 \end{bmatrix}$$

- **Problem 2.**

    $$B = \begin{bmatrix} 3 & -1 & 2 & 0 \\ 1 & 4 & -3 & 5 \end{bmatrix}$$

- **Problem 3.**

    $$C = \begin{bmatrix} 2 \\ -1 \\ 0 \\ 5 \end{bmatrix}$$

- **Problem 4.**

    $$D = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix}$$

</div>

Compute the following, if possible.

<div class="grid cards" markdown>

- **Problem 5.**

    $$\begin{bmatrix} 2 & -1 \\ 0 & 3 \end{bmatrix} + \begin{bmatrix} 1 & 4 \\ -2 & 1 \end{bmatrix}$$

- **Problem 6.**

    $$\begin{bmatrix} 5 & 0 \\ -1 & 2 \end{bmatrix} - \begin{bmatrix} 3 & -1 \\ 4 & 2 \end{bmatrix}$$

- **Problem 7.**

    $$\begin{bmatrix} 1 & 2 & 3 \end{bmatrix} + \begin{bmatrix} 1 & 0 \\ -1 & 2 \end{bmatrix}$$

- **Problem 8.**

    $$\begin{bmatrix} 1 & 2 \\ -3 & 0 \\ 4 & 1 \end{bmatrix} - \begin{bmatrix} 0 & -1 \\ 2 & 3 \\ -1 & 4 \end{bmatrix}$$

</div>

Compute the following scalar products.

<div class="grid cards" markdown>

- **Problem 9.**

    $$3\begin{bmatrix} 2 & -1 \\ 0 & 4 \end{bmatrix}$$

- **Problem 10.**

    $$-2\begin{bmatrix} 1 & 0 & -3 \\ 2 & 5 & 1 \end{bmatrix}$$

- **Problem 11.**

    $$4\begin{bmatrix} 1 \\ -2 \\ 3 \end{bmatrix}$$

- **Problem 12.**

    $$-1\begin{bmatrix} 2 & -4 \\ -1 & 3 \end{bmatrix}$$

</div>

Determine whether the following matrix multiplications are allowed. If allowed, state the dimensions of the resulting matrix.

<div class="grid cards" markdown>

- **Problem 13.**

    $AB$, where $A$ is $3 \times 2$ and $B$ is $2 \times 4$.

- **Problem 14.**

    $BA$, where $A$ is $3 \times 2$ and $B$ is $2 \times 4$.

- **Problem 15.**

    $CD$, where $C$ is $2 \times 3$ and $D$ is $2 \times 3$.

- **Problem 16.**

    $DC$, where $C$ is $2 \times 3$ and $D$ is $3 \times 2$.

</div>

Compute the following matrix products.

<div class="grid cards" markdown>

- **Problem 17.**

    $$\begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix}\begin{bmatrix} 0 & 1 \\ 1 & 0 \end{bmatrix}$$

- **Problem 18.**

    $$\begin{bmatrix} 2 & -1 \\ 0 & 3 \end{bmatrix}\begin{bmatrix} 1 & 2 \\ -1 & 4 \end{bmatrix}$$

- **Problem 19.**

    $$\begin{bmatrix} 1 & 0 & 2 \\ 3 & 1 & -1 \end{bmatrix}\begin{bmatrix} 2 & 1 \\ -1 & 0 \\ 3 & 2 \end{bmatrix}$$

- **Problem 20.**

    $$\begin{bmatrix} 2 & 1 & -1 \\ 0 & 3 & 2 \\ 1 & -1 & 4 \end{bmatrix}\begin{bmatrix} 1 & 0 & 2 \\ -1 & 2 & 1 \\ 3 & 1 & 0 \end{bmatrix}$$

</div>

**Problem 21.** Given 

$$A = \begin{bmatrix} 1 & 2 \\ 0 & 1 \end{bmatrix}, \quad B = \begin{bmatrix} 3 & 1 \\ -1 & 2 \end{bmatrix}, \quad C = \begin{bmatrix} 0 & -1 \\ 2 & 1 \end{bmatrix}$$

compute $A + 2BC$.

**Problem 22.** Using the same matrices as Problem 21, compute $3AB - C$.

Determine whether the following statements are true or false. Justify your decision. 

<div class="grid cards" markdown>

- **Problem 23.**

    Let $A$ and $B$ be matrices with the same dimensions. Then $A + B = B + A$.

- **Problem 24.**

    If $S$ and $T$ have the same dimensions, then $ST$ is computable. 

- **Problem 25.**

    For square matrices $M$ and $N$, $MN = NM$. 

- **Problem 26.**

    Let $c$ be a scalar and let $A$ and $B$ be matrices such that $AB$ is computable. Then $(cA)B = A(cB)$. 

</div>

### 2.2 Exercises

Write each system as a matrix equation $AX = B$. You do not need to solve. 

<div class="grid cards" markdown>

- **Problem 27.**

    $$x + 3y = 7$$

    $$2x - y = 1$$

- **Problem 28.**

    $$4x - 2y = 0$$

    $$x + 5y = 3$$

- **Problem 29.**

    $$y = 2x + 1$$

    $$3x + y = 10$$

- **Problem 30.**

    $$2x - y = 4$$

    $$y = x - 1$$

</div>

<div class="grid cards" markdown>

- **Problem 31.**

    $$x + y + z = 6$$

    $$2x - y + z = 3$$

    $$x + 2y - z = 2$$

- **Problem 32.**

    $$3x - y + 2z = 5$$

    $$x + 4z = -1$$

    $$2x + y - z = 0$$

</div>

### 2.3 Exercises

Solve each system using Gaussian elimination.

<div class="grid cards" markdown>

- **Problem 33.**

    $$x + 2y = 8$$

    $$3x - y = 3$$

- **Problem 34.**

    $$2x + y = 5$$

    $$x - 3y = -1$$

- **Problem 35.**

    $$4x + 2y = 10$$

    $$-2x + y = 1$$

- **Problem 36.**

    $$3x - 2y = 4$$

    $$x + y = 3$$

</div>

<div class="grid cards" markdown>

- **Problem 37.**

    $$x + y + z = 6$$

    $$2x - y + z = 3$$

    $$x + 2y - z = 2$$

- **Problem 38.**

    $$x - y + 2z = 5$$

    $$2x + y - z = 1$$

    $$3x - 2y + z = 8$$

</div>

### 2.4 Exercises

Verify that $B$ is the inverse of $A$.

<div class="grid cards" markdown>

- **Problem 39.**

    $$A = \begin{bmatrix} 4 & 1 \\ 3 & 1 \end{bmatrix}, \quad B = \begin{bmatrix} 1 & -1 \\ -3 & 4 \end{bmatrix}$$

- **Problem 40.**

    $$A = \begin{bmatrix} 1 & 2 \\ 3 & 5 \end{bmatrix}, \quad B = \begin{bmatrix} -5 & 2 \\ 3 & -1 \end{bmatrix}$$

</div>

Use the augmented matrix method to find the inverse of each matrix.

<div class="grid cards" markdown>

- **Problem 41.**

    $$\begin{bmatrix} 1 & 3 \\ 2 & 5 \end{bmatrix}$$

- **Problem 42.**

    $$\begin{bmatrix} 3 & 1 \\ 4 & 2 \end{bmatrix}$$

- **Problem 43.**

    $$\begin{bmatrix} 1 & 0 & 2 \\ 0 & 1 & 1 \\ 1 & 1 & 0 \end{bmatrix}$$

- **Problem 44.**

    $$\begin{bmatrix} 1 & 1 & 0 \\ 0 & 1 & 1 \\ 1 & 0 & 1 \end{bmatrix}$$

</div>

Use the $2 \times 2$ inverse formula to find the inverse of each matrix, or state that it does not exist.

<div class="grid cards" markdown>

- **Problem 45.**

    $$\begin{bmatrix} 5 & 2 \\ 3 & 1 \end{bmatrix}$$

- **Problem 46.**

    $$\begin{bmatrix} 2 & -4 \\ -1 & 2 \end{bmatrix}$$

- **Problem 47.**

    $$\begin{bmatrix} 6 & 1 \\ 2 & 0 \end{bmatrix}$$

- **Problem 48.**

    $$\begin{bmatrix} 3 & 6 \\ 1 & 2 \end{bmatrix}$$

</div>

**Problem 49.** Use the inverse found in Problem 39 to solve the system,

$$4x + y = 3$$

$$3x + y = 1$$

**Problem 50.** Use the inverse found in Problem 40 to solve the system,

$$x + 2y = 0$$

$$3x + 5y = -1$$

### 2.5 Exercises 

Determine which of the following matrices are valid transition matrices.

<div class="grid cards" markdown>

- **Problem 51.**

    $$\begin{bmatrix} 0.6 & 0.3 \\ 0.4 & 0.7 \end{bmatrix}$$

- **Problem 52.**

    $$\begin{bmatrix} 0.5 & 0.6 \\ 0.5 & 0.3 \end{bmatrix}$$

- **Problem 53.**

    $$\begin{bmatrix} 0.5 & 0.2 & 0.3 \\ 0.6 & 0.5 & 0.3 \\ -0.1 & 0.3 & 0.4 \end{bmatrix}$$

- **Problem 54.**

    $$\begin{bmatrix} 0.4 & 0.1 & 0.3 \\ 0.4 & 0.6 & 0.3 \\ 0.2 & 0.3 & 0.4 \end{bmatrix}$$

</div>

**Problem 55.** A transition matrix is given by

$$T = \begin{bmatrix} 0.7 & 0.4 \\ 0.3 & 0.6 \end{bmatrix}$$

and the current state vector is $v_0 = \begin{bmatrix} 0.5 \\ 0.5 \end{bmatrix}$.

a) Find $v_1$.

b) Find $v_2$.


**Problem 56.** A transition matrix is given by

$$T = \begin{bmatrix} 0.9 & 0.2 \\ 0.1 & 0.8 \end{bmatrix}$$

Find the stationary state.


**Problem 57.** Each year, $5\%$ of the rural population moves to the city, and $3\%$ of the city population moves to the rural area. Currently $40\%$ of the population is rural and $60\%$ lives in the city.

a) Write a transition matrix for the process.

b) Find the population distribution after 1 and 2 years.

c) Find the long-run steady state distribution.


**Problem 58.** Two streaming services, StreamMax and ViewPlus, compete for subscribers. Each month, StreamMax retains $75\%$ of its subscribers and loses $25\%$ to ViewPlus. ViewPlus retains $85\%$ of its subscribers and loses $15\%$ to StreamMax. Currently StreamMax holds $30\%$ of the market and ViewPlus holds $70\%$.

a) Write the transition matrix.

b) Find the market share after 1 and 2 months.

c) Find the long-run steady state market share.


**Problem 59.** Customers have three grocery store options: FreshMart, ValueGrocer, and QuickShop. Each week, FreshMart keeps $70\%$ of its customers, loses $20\%$ to ValueGrocer, and $10\%$ to QuickShop. ValueGrocer keeps $60\%$ of its customers, loses $25\%$ to FreshMart, and $15\%$ to QuickShop. QuickShop keeps $80\%$ of its customers, loses $10\%$ to FreshMart, and $10\%$ to ValueGrocer. Currently the market shares of FreshMart, ValueGrocer, and QuickShop are $50\%$, $30\%$, and $20\%$ respectively.

a) Write the transition matrix.

b) Find the market share after 1 week.

c) Find the long-run steady state market share.
