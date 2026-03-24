When using only the simplex method isn't enough, a new approach must be used
## Example

$$2x+y-s_1=10$$ 
Let us add an Artificial Variable $y_1$.
$$2x+y-s_{1}+y_{1}$$
The only way we can relate the two Feasible Solutions of these systems would be if the Artificial Variable has the value $0$.

So, our goal is to make the value of the AV $0$. This can be done using a Linear Problem.

$$\text{Min}z'=\sum y_i = \text{sumAV}$$
Can be written as
$$\text{Max}z''=-\sum y_{i}$$

*****

$$\text{Max }z=2x+3y$$
$$x+2y\geq2$$
$$x+y\geq{3}$$
$$x,y\geq{0}$$

Change forms

$$x+2y-s_{1}=2$$
$$3x+y-s_{2}=3$$
$$x,y,s_{1},s_{2}\geq{0}$$

Place in a tableau


|       | $x$ | $y$ | $s_1$ | $s_2$ | $z$ |     |
| ----- | --- | --- | ----- | ----- | --- | --- |
| $s_1$ | 1   | 2   | -1    | 0     | 0   | 2   |
| $s_2$ | 3   | 1   | 0     | -1    | 0   | 3   |
|       | 0   | 0   | 1     | 1     | 1   | 0   |
Here, $s_1$ and $s_2$ can't act as basic variables, as they're negative while the RBHS are positive. So instead, we add two new artificial variables $y_1,y_2$.

|       | $x$ | $y$ | $s_1$ | $s_2$ | $y_1$ | $y_2$ | $z''$ |     |
| ----- | --- | --- | ----- | ----- | ----- | ----- | ----- | --- |
| $y_1$ | 1   | 2   | -1    | 0     | 1     | 0     | 0     | 2   |
| $y_2$ | 3   | 1   | 0     | -1    | 0     | 1     | 0     | 3   |
|       | 0   | 0   | 0     | 0     | 1     | 1     | 1     | 0   |
However, even now, the objective row is incorrect as the columns of the basic variables are non-zero.

we can use row operations $OR - R_1 - R_2 = OR$

|       | $x$ | $y$ | $s_1$ | $s_2$ | $y_1$ | $y_2$ | $z''$ |     |
| ----- | --- | --- | ----- | ----- | ----- | ----- | ----- | --- |
| $y_1$ | 1   | 2   | -1    | 0     | 1     | 0     | 0     | 2   |
| $y_2$ | 3   | 1   | 0     | -1    | 0     | 1     | 0     | 3   |
|       | -4  | -3  | 1     | 1     | 0     | 0     | 1     | -5  |
|       |     |     |       |       |       |       |       |     |

Here is our current solution:

$$\begin{vmatrix}
x\\
y\\
s_{1}\\
s_{2}\\
y_{1}\\
y_{2}\\
\end{vmatrix}=\begin{vmatrix}
0\\0\\0\\0\\2\\3\end{vmatrix}$$

With negatives in our objective row, we simply use simplex until solved.

|     | $x$ | $y$ | $s_1$      | $s_2$          | $y_1$      | $y_2$         | $z''$ |           |
| --- | --- | --- | ---------- | -------------- | ---------- | ------------- | ----- | --------- |
| $y$ | 0   | 1   | $-\frac35$ | $\frac15$      | $\frac35$  | $-\frac15$    | 0     | $\frac35$ |
| $x$ | 1   | 0   | $\frac15$  | $-\frac{2}{5}$ | $-\frac15$ | $\frac{2}{5}$ | 0     | $\frac45$ |
|     | 0   | 0   | 0          | 0              | 1          | 1             | 1     | 0         |
If all Artificial Variables are Non-Basic Variables, in FT of P1 drop their columns. Then, you replace the objective row with the original.

|     | $x$ | $y$ | $s_1$      | $s_2$          | $z$ |           |
| --- | --- | --- | ---------- | -------------- | --- | --------- |
| $y$ | 0   | 1   | $-\frac35$ | $\frac15$      | 0   | $\frac35$ |
| $x$ | 1   | 0   | $\frac15$  | $-\frac{2}{5}$ | 0   | $\frac45$ |
|     | -2  | -3  | 0          | 0              | 1   | 0         |
And now you continue simplex method (remember basic variables must have 0's in their objective row.)

|     | $x$ | $y$ | $s_1$ | $s_2$ | $z$ |     |
| --- | --- | --- | ----- | ----- | --- | --- |
| $y$ | 3   | 1   | 0     | -1    | 0   | 3   |
| $x$ | 5   | 0   | 1     | -2    | 0   | 4   |
|     | 7   | 0   | 0     | -3    | 1   | 9   |
This shows that the original LP is unbounded.

*****
## Example Problem

### T1P1 
*which means Tableau 1, Phase 1*
Since we added the Artificial Variable $y_1$, we need to use the objective function 

$$\text{Min }z'=y_{1}$$
because once an AV is introduced it must be minimized. (taken out of the equation).
This will be put in the Objective Row.

|       | $x$ | $y$ | $s_1$ | $y_1$ | $z''$ |     |
| ----- | --- | --- | ----- | ----- | ----- | --- |
| $y$   | 2   | 1   | 1     | 0     | 0     | 2   |
| $y_1$ | -3  | 1   | 0     | 1     | 0     | 3   |
|       | 3   | -1  | 0     | 0     | 1     | -3  |
### T2P1


|       | $x$ | $y$ | $s_1$ | $y_1$ | $z''$ |     |
| ----- | --- | --- | ----- | ----- | ----- | --- |
| $y$   | 2   | 1   | 1     | 0     | 0     | 2   |
| $y_1$ | -5  | 0   | -1    | 1     | 0     | 1   |
|       | 5   | 0   | 1     | 0     | 1     | -1  |
All entries in our Objective row are non-negative, and those in the pivot columns are 0 so, this is the final tableau of Phase 1. At the same time, the AV $y_1$ is still being used as a basic variable.

> Since $z''_{OV}=-1\ne0$, every Feasible Solution of this system with Artificial Variables has some Artificial Variable that has a non zero value. This means that the Original Linear Problem system is infeasible.

## Effect of Degeneracy
|         | $x$ | $y$ | $s_1$ | $s_2$ | $z$ |     |
| ------- | --- | --- | ----- | ----- | --- | --- |
| $s_{1}$ | 1   | 2   | 1     | 0     | 0   | 0   |
| $y_2$   | 3   | 1   | 0     | 1     | 0   | 2   |
|         | -2  | -3  | 0     | 0     | 1   | 4   |
If the Entering variable column is positive in any of the rows in which the basic variable value is 0, then one of those must be the departing variable, as $\theta=0$.

So, using simplex method will get you to the same BFS vector, but the Basic Variable labeling changed.