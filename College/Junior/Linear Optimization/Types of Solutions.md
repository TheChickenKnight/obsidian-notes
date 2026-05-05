
# Example
$$\begin{vmatrix}1&2&1\\1&4&2\end{vmatrix}\begin{vmatrix}x_1\\x_2\\x_3\end{vmatrix}=\begin{vmatrix}-1\\1\end{vmatrix}$$
## Can $\{x_1\}$ be a list of basic variables?
No, Not as many as number of rows
## Can $\{x_1,x_2\}$ act as basic variables?
Yes, as it equals the number of rows.

## Check if $\vec{A_1},\vec{A_2}$ are linearly dependent
Checking the linearly dependence of two vectors is trivial, but for the record:
$$det(\begin{vmatrix}1&2\\1&4\end{vmatrix})=4(1)-2(1)=2\neq0$$

Their determinant is nonzero, so yes.

## Can $\{x_2,x_3\}$ be basic variables?
No, because $\vec{A_2},\vec{A_3}$ are not linearly independent (their determinant is 0).


Setting values of S-m non-basic variables to be 0, then solving is called a basic solution.

$$\begin{vmatrix}1&2&1\\1&4&2\end{vmatrix}\begin{vmatrix}x_1\\0\\x_3\end{vmatrix}=\begin{vmatrix}-1\\1\end{vmatrix}$$

## Degenerate Basic Solution
a basic solution with at least 1 val 0
### Ex.
$\begin{vmatrix}2\\0\\0\end{vmatrix}$ as a solution to the previous example.

## Basic Feasible Solution
A basic solution which also satisfies non-negativity in it's variables



$\vec{v}$ is an Extreme Point if $A\vec x=\vec b$, $\vec x\geq\vec 0$ if and only if 
$\vec v$ is a Basic Feasible Solution.
