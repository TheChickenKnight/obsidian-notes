- Last row is the objective row, the objective function into a row

## Example
### Objective Function
$z=x_1+3x_2$
### Constraints
$-x_1+x_2+x_3=2$
$2x_1+x_2+x_4=1$
$x_1+x_2+x_5=1$

### Table (KB formatting[^1])

| $x_1$ | $x_2$ | $x_3$ | $x_4$ | $x_5$ | $z$ |     |
| ----- | ----- | ----- | ----- | ----- | --- | --- |
| -1    | 1     | 1     | 0     | 0     | 0   | 2   |
| 2     | 1     | 0     | 1     | 0     | 0   | 1   |
| 1     | 1     | 0     | 0     | 1     | 0   | 1   |
| -1    | -3    | 0     | 0     | 0     | 1   | 0   |
**Coefficients of $z$ in Objective Row must be 1, or 0 otherwise**

[^1]: You should follow the same formatting or else you have to be more specific.

### Tableau 
Use "row operations" to get pivot columns

| $x_1$ | $x_2$      | $x_3$ | $x_4$      | $x_5$ | $z$ |           |
| ----- | ---------- | ----- | ---------- | ----- | --- | --------- |
| 0     | $\frac32$  | 1     | $\frac12$  | 0     | 0   | $\frac52$ |
| 1     | $\frac12$  | 0     | $\frac12$  | 0     | 0   | $\frac12$ |
| 0     | $\frac12$  | 0     | $-\frac12$ | 1     | 0   | $\frac12$ |
| 0     | $-\frac52$ | 0     | $\frac12$  | 0     | 1   | $\frac12$ |
Now, we see that there are 3 linearly independent rows $x_1$, $x_3$, and $x_5$, meaning that there is a possible **basic solution** with these three **basic variables**.

> Note: This also "solves" $x_1$, $x_3$, $x_5$, and $z$ in terms of non-basic variables:
$x_3=\frac52-\frac32 x_2-\frac12x_4$
$x_1=\frac12-\frac12x_2+\frac12x_4$
$x_5=\frac12-\frac12x_2+\frac12x_4$
$z=\frac12+\frac52x_2-\frac12x_4$

To find the basic solution, set the values of the non basic variables to 0. 

### Basic Solution
$$\begin{vmatrix}
x_{1} \\
x_{2} \\
x_{3} \\
x_{4} \\
x_{5}
\end{vmatrix}=\begin{vmatrix}
\frac{1}{2} \\
0 \\
\frac{5}{2} \\
0 \\
\frac{1}{2}
\end{vmatrix}$$

With the z-value at this basic solution being $z=\frac12$.


> If all objective row entries other than the z value are $\geq$ 0, then it is optimal.



*****



| BV  | $x_1$ | $x_2$ | $x_3$ | $x_4$ | $x_5$ |     |
| --- | ----- | ----- | ----- | ----- | ----- | --- |
|     |       |       |       |       |       |     |
|     |       |       |       |       |       |     |

