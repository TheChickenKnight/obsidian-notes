- Suppose you have **3 factories** and **4 warehouses**. 
	- Each factory can produce a certain amount of cars. 
		- These cares are indivisible (e.g. you can't produce a fraction of a car).
		- Factory 1 can produce 100 cars per unit of time 
			- $S_1=100$
		- Factory 2 can produce 80 cars
			- $S_2=80$
		- Factory 3 can produce 140 cars
			- $S_3=140$
	- Each Warehouse requires a demand of cars
		- $d_1=60$
		- $d_2=60$
		- $d_3=80$
		- $d_4=120$
- To transport 1 unit from factory $i$ to warehouse $j$ costs $c_{ij}$ dollars
	- so, $3*4=12$ 
- The Objective is the minimum total cost of transporting.
*****
How many to send from each factory to each warehouse?

### Constraints
Each factory $i$ can ship at most $s_i$ units

Each warehouse must receive at least $d_j$ units

### Decision Variables
Each will be called $x_{ij}$ where $i=[1,m]$ and $j=[1,n]$


$$\text{Min }z=\sum^n_{j=1}\sum^m_{i=1}x_{ij}$$
Subject to 
number coming out of factory $i$

$$\sum^n_{j=1}x_{ij}\le s_{i}$$
There are $m$ such constraints

$$\sum^m_{i=1}x_{ij}\ge d_{j}$$
There are $n$ such constraints


## Example

Costs Matrix
$$(C_{ij})=\begin{vmatrix}
5&2&3&6\\2&7&7&4\\1&3&6&9
\end{vmatrix}$$

Supply from factories
$$\vec{s}=\begin{vmatrix}
100\\80\\140
\end{vmatrix}$$
Demand of Warehouses.
$$\vec{d}=\begin{vmatrix}
60\\60\\80\\20
\end{vmatrix}$$


Let's write out the LP without summation:
$$\text{Min }z=5x_{11}+2x_{12}+3x_{13}+6x_{14}+2x_{21}+7x_{22}+7x_{23}+4x_{24}+1x_{31}+3x_{32}+6x_{33}9x_{34}$$

Let's also write out the constraints without summation:

Constraints for Supply
$$x_{11}+x_{12}+x_{13}+x_{14}\le 100$$
$$x_{21}+x_{22}+x_{23}+x_{24}\le 80$$
$$x_{31}+x_{32}+x_{33}+x_{34}\le 140$$

Constraints for Demand
$$x_{11}+x_{21}+x_{31}\ge 60$$
$$x_{12}+x_{22}+x_{32}\ge 60$$
$$x_{13}+x_{23}+x_{33}\ge 80$$
$$x_{14}+x_{24}+x_{34}\ge 120$$


In general we focus on the supply equaling the demand. If they don't create an artificial warehouse with a 0 cost to travel to where the excess can go. Given now that supply and demand is equal, we can change all constraints to strict equivalents.

There are $m+n-1$ basic variables.
## Representation

| $d_1=60$ | $d_2=60$ | $d_3=80$ | $d_4=120$ |           |
| -------- | -------- | -------- | --------- | --------- |
| 25       | 25       | 25       | 25        | $s_1=100$ |
| 20       | 20       | 20       | 20        | $s_2=80$  |
| 15       | 15       | 35       | 75        | $s_3=140$ |
|          |          |          |           |           |
It's easy to get a feasible solution by just filling in numbers based on the constraint. Next, Let's make it a basic feasible solution.

$$\begin{vmatrix}
1&1&1&1|&0&0&0&0|&0&0&0&0 \\
0&0&0&0|&1&1&1&1|&0&0&0&0 \\
0&0&0&0|&0&0&0&0|&1&1&1&1 \\ 
\_&\_&\_&\_&\_&\_&\_&\_&\_&\_&\_&\_\\
1&0&0&0|&1&0&0&0|&1&0&0&0 \\
0&1&0&0|&0&1&0&0|&0&1&0&0 \\
0&0&1&0|&0&0&1&0|&0&0&1&0 \\
0&0&0&1|&0&0&0&1|&0&0&0&1
\end{vmatrix}\begin{vmatrix}
x_{11} \\
x_{12} \\
x_{13} \\
x_{14} \\
x_{21} \\
x_{22} \\
x_{23} \\
x_{24} \\
x_{31} \\
x_{32} \\
x_{33} \\
x_{34} \\
\end{vmatrix}=\begin{vmatrix}
100 \\
80 \\
140 \\
60 \\
60 \\
80 \\
120
\end{vmatrix}$$

Every column is linearly dependent.

Cells on a loop are Linearly dependent, if the edges alternate.

*****
## Row Min Cost Rule
1. Apply the largest possible value to each lowest cost, starting with the first row.
2. These filled in cells are the basic variables.
**This is important because this method never creates a loop, therefore being linearly independent and more so a basic feasible solution**
### Example

| $d_1=60$ | $d_2=60$ | $d_3=80$ | $d_4=120$ |           |
| -------- | -------- | -------- | --------- | --------- |
| 5()      | 2(60)    | 3(40)    | 6()       | $s_1=100$ |
| 2(60)    | 7()      | 7()      | 4(20)     | $s_2=80$  |
| 1()      | 3()      | 6(40)    | 9(100)    | $s_3=140$ |
This creates a basic feasible solution, but probably not optimal.

$$OR_{ij}=v_{i}+w_{j}-c_{ij}$$

where $v_{i}$ is the $i$th row constraint and $w_j$ the $j$th column constraint.

Because we are in a tight constraint (=) problem, we know we have one free variable. So, fix $v_i$ to 0 and solve for the rest of the dual variables using basic variable cells.

Then, find the objective row values for each cell with the same formula.

Now we perform simplex.
all OR must be $\le 0$, so we decide on the

EV: cell w/ highest OR value
DV: Check how increasing the EV by 1 will change the existing BV, this will create a loop. The smaller of the BV that decrease is swapped.

If there are multiple possible DV with the same value, choose one randomly. the rest become 0 value basic variables.