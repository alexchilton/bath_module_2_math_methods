# Matrix Operations Solutions

## Given Matrices

$$A = \begin{pmatrix} 2 & 4 \\ -2 & -5 \end{pmatrix}$$

$$B = \begin{pmatrix} 2 & -1 \\ 4 & 1 \\ 5 & 6 \end{pmatrix}$$

$$C = \begin{pmatrix} 1 & 5 & 2 \\ -1 & 4 & 0 \end{pmatrix}$$

$$D = \begin{pmatrix} 4 & 3 & 2 \\ -1 & -1 & 5 \\ 0 & 2 & 4 \\ 0 & 0 & 0 \end{pmatrix}$$

## Question 1: Matrix Additions

### a) $A + A$

$$A + A = \begin{pmatrix} 2 & 4 \\ -2 & -5 \end{pmatrix} + \begin{pmatrix} 2 & 4 \\ -2 & -5 \end{pmatrix} = \begin{pmatrix} 4 & 8 \\ -4 & -10 \end{pmatrix}$$

### b) $3D$ (equivalent to $D + D + D$)

$$3D = 3 \begin{pmatrix} 4 & 3 & 2 \\ -1 & -1 & 5 \\ 0 & 2 & 4 \\ 0 & 0 & 0 \end{pmatrix} = \begin{pmatrix} 12 & 9 & 6 \\ -3 & -3 & 15 \\ 0 & 6 & 12 \\ 0 & 0 & 0 \end{pmatrix}$$

## Question 2: Matrix Multiplications

### a) $AA$

$$AA = \begin{pmatrix} 2 & 4 \\ -2 & -5 \end{pmatrix} \begin{pmatrix} 2 & 4 \\ -2 & -5 \end{pmatrix}$$

$$= \begin{pmatrix} 2(2) + 4(-2) & 2(4) + 4(-5) \\ -2(2) + (-5)(-2) & -2(4) + (-5)(-5) \end{pmatrix}$$

$$= \begin{pmatrix} 4 - 8 & 8 - 20 \\ -4 + 10 & -8 + 25 \end{pmatrix} = \begin{pmatrix} -4 & -12 \\ 6 & 17 \end{pmatrix}$$

### b) $AC$

$$AC = \begin{pmatrix} 2 & 4 \\ -2 & -5 \end{pmatrix} \begin{pmatrix} 1 & 5 & 2 \\ -1 & 4 & 0 \end{pmatrix}$$

$$= \begin{pmatrix} 2(1) + 4(-1) & 2(5) + 4(4) & 2(2) + 4(0) \\ -2(1) + (-5)(-1) & -2(5) + (-5)(4) & -2(2) + (-5)(0) \end{pmatrix}$$

$$= \begin{pmatrix} 2 - 4 & 10 + 16 & 4 + 0 \\ -2 + 5 & -10 - 20 & -4 + 0 \end{pmatrix} = \begin{pmatrix} -2 & 26 & 4 \\ 3 & -30 & -4 \end{pmatrix}$$

### c) $BA$

$$BA = \begin{pmatrix} 2 & -1 \\ 4 & 1 \\ 5 & 6 \end{pmatrix} \begin{pmatrix} 2 & 4 \\ -2 & -5 \end{pmatrix}$$

$$= \begin{pmatrix} 2(2) + (-1)(-2) & 2(4) + (-1)(-5) \\ 4(2) + 1(-2) & 4(4) + 1(-5) \\ 5(2) + 6(-2) & 5(4) + 6(-5) \end{pmatrix}$$

$$= \begin{pmatrix} 4 + 2 & 8 + 5 \\ 8 - 2 & 16 - 5 \\ 10 - 12 & 20 - 30 \end{pmatrix} = \begin{pmatrix} 6 & 13 \\ 6 & 11 \\ -2 & -10 \end{pmatrix}$$

### d) $BC$

$$BC = \begin{pmatrix} 2 & -1 \\ 4 & 1 \\ 5 & 6 \end{pmatrix} \begin{pmatrix} 1 & 5 & 2 \\ -1 & 4 & 0 \end{pmatrix}$$

$$= \begin{pmatrix} 2(1) + (-1)(-1) & 2(5) + (-1)(4) & 2(2) + (-1)(0) \\ 4(1) + 1(-1) & 4(5) + 1(4) & 4(2) + 1(0) \\ 5(1) + 6(-1) & 5(5) + 6(4) & 5(2) + 6(0) \end{pmatrix}$$

$$= \begin{pmatrix} 2 + 1 & 10 - 4 & 4 + 0 \\ 4 - 1 & 20 + 4 & 8 + 0 \\ 5 - 6 & 25 + 24 & 10 + 0 \end{pmatrix} = \begin{pmatrix} 3 & 6 & 4 \\ 3 & 24 & 8 \\ -1 & 49 & 10 \end{pmatrix}$$

### e) $CD$

$$CD = \begin{pmatrix} 1 & 5 & 2 \\ -1 & 4 & 0 \end{pmatrix} \begin{pmatrix} 4 & 3 & 2 \\ -1 & -1 & 5 \\ 0 & 2 & 4 \\ 0 & 0 & 0 \end{pmatrix}$$

Since $C$ is $2 \times 3$ and $D$ is $4 \times 3$, this multiplication is **not possible** because the number of columns in $C$ (3) does not equal the number of rows in $D$ (4).

### f) $DB$

$$DB = \begin{pmatrix} 4 & 3 & 2 \\ -1 & -1 & 5 \\ 0 & 2 & 4 \\ 0 & 0 & 0 \end{pmatrix} \begin{pmatrix} 2 & -1 \\ 4 & 1 \\ 5 & 6 \end{pmatrix}$$

$$= \begin{pmatrix} 4(2) + 3(4) + 2(5) & 4(-1) + 3(1) + 2(6) \\ -1(2) + (-1)(4) + 5(5) & -1(-1) + (-1)(1) + 5(6) \\ 0(2) + 2(4) + 4(5) & 0(-1) + 2(1) + 4(6) \\ 0(2) + 0(4) + 0(5) & 0(-1) + 0(1) + 0(6) \end{pmatrix}$$

$$= \begin{pmatrix} 8 + 12 + 10 & -4 + 3 + 12 \\ -2 - 4 + 25 & 1 - 1 + 30 \\ 0 + 8 + 20 & 0 + 2 + 24 \\ 0 + 0 + 0 & 0 + 0 + 0 \end{pmatrix} = \begin{pmatrix} 30 & 11 \\ 19 & 30 \\ 28 & 26 \\ 0 & 0 \end{pmatrix}$$

### g) $D^2$ (equivalent to $DD$)

$$D^2 = \begin{pmatrix} 4 & 3 & 2 \\ -1 & -1 & 5 \\ 0 & 2 & 4 \\ 0 & 0 & 0 \end{pmatrix} \begin{pmatrix} 4 & 3 & 2 \\ -1 & -1 & 5 \\ 0 & 2 & 4 \\ 0 & 0 & 0 \end{pmatrix}$$

$$= \begin{pmatrix} 4(4) + 3(-1) + 2(0) & 4(3) + 3(-1) + 2(2) & 4(2) + 3(5) + 2(4) \\ -1(4) + (-1)(-1) + 5(0) & -1(3) + (-1)(-1) + 5(2) & -1(2) + (-1)(5) + 5(4) \\ 0(4) + 2(-1) + 4(0) & 0(3) + 2(-1) + 4(2) & 0(2) + 2(5) + 4(4) \\ 0(4) + 0(-1) + 0(0) & 0(3) + 0(-1) + 0(2) & 0(2) + 0(5) + 0(4) \end{pmatrix}$$

$$= \begin{pmatrix} 16 - 3 + 0 & 12 - 3 + 4 & 8 + 15 + 8 \\ -4 + 1 + 0 & -3 + 1 + 10 & -2 - 5 + 20 \\ 0 - 2 + 0 & 0 - 2 + 8 & 0 + 10 + 16 \\ 0 + 0 + 0 & 0 + 0 + 0 & 0 + 0 + 0 \end{pmatrix} = \begin{pmatrix} 13 & 13 & 31 \\ -3 & 8 & 13 \\ -2 & 6 & 26 \\ 0 & 0 & 0 \end{pmatrix}$$

## Question 3: The Missing Matrix Multiplication

Looking at the dimensions of our matrices:
- $A$: $2 \times 2$
- $B$: $3 \times 2$
- $C$: $2 \times 3$
- $D$: $4 \times 3$

We've calculated: $AA$, $AC$, $BA$, $BC$, $DB$, $D^2$, and found that $CD$ is not possible.

The one remaining possible multiplication is $CB$:

$$CB = \begin{pmatrix} 1 & 5 & 2 \\ -1 & 4 & 0 \end{pmatrix} \begin{pmatrix} 2 & -1 \\ 4 & 1 \\ 5 & 6 \end{pmatrix}$$

$$= \begin{pmatrix} 1(2) + 5(4) + 2(5) & 1(-1) + 5(1) + 2(6) \\ -1(2) + 4(4) + 0(5) & -1(-1) + 4(1) + 0(6) \end{pmatrix}$$

$$= \begin{pmatrix} 2 + 20 + 10 & -1 + 5 + 12 \\ -2 + 16 + 0 & 1 + 4 + 0 \end{pmatrix} = \begin{pmatrix} 32 & 16 \\ 14 & 5 \end{pmatrix}$$

## Question 4: Calculate $\det(A)$ and $A^{-1}$

### Finding $\det(A)$

$$\det(A) = \det\begin{pmatrix} 2 & 4 \\ -2 & -5 \end{pmatrix} = 2(-5) - 4(-2) = -10 + 8 = -2$$

### Finding $A^{-1}$

For a $2 \times 2$ matrix $\begin{pmatrix} a & b \\ c & d \end{pmatrix}$, the inverse is $\frac{1}{ad-bc}\begin{pmatrix} d & -b \\ -c & a \end{pmatrix}$

$$A^{-1} = \frac{1}{-2}\begin{pmatrix} -5 & -4 \\ 2 & 2 \end{pmatrix} = \begin{pmatrix} \frac{5}{2} & 2 \\ -1 & -1 \end{pmatrix}$$

## Question 5: Solving the System of Linear Equations

The system is:
$$\begin{aligned}
2x_1 + 4x_2 &= 22 \\
-2x_1 - 5x_2 &= -26
\end{aligned}$$

This can be written in matrix form as $A\mathbf{x} = \mathbf{b}$ where:

$$\begin{pmatrix} 2 & 4 \\ -2 & -5 \end{pmatrix} \begin{pmatrix} x_1 \\ x_2 \end{pmatrix} = \begin{pmatrix} 22 \\ -26 \end{pmatrix}$$

The solution is $\mathbf{x} = A^{-1}\mathbf{b}$:

$$\begin{pmatrix} x_1 \\ x_2 \end{pmatrix} = \begin{pmatrix} \frac{5}{2} & 2 \\ -1 & -1 \end{pmatrix} \begin{pmatrix} 22 \\ -26 \end{pmatrix}$$

$$= \begin{pmatrix} \frac{5}{2}(22) + 2(-26) \\ -1(22) + (-1)(-26) \end{pmatrix} = \begin{pmatrix} 55 - 52 \\ -22 + 26 \end{pmatrix} = \begin{pmatrix} 3 \\ 4 \end{pmatrix}$$

**Therefore: $x_1 = 3$ and $x_2 = 4$**