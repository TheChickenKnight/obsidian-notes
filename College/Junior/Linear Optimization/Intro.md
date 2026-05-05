	
A Matrix $A$ is invertible if it's **determinant** is nonzero.

# Determinant
## 2x2 Matrices
In this case, its much easier to calculate the determinant.
$$detA=ad-bc$$
where
$$
A=\begin{vmatrix}a&b\\c&d\end{vmatrix}
$$


# Inverse of a 2x2 Matrix
$$\begin{vmatrix}a&b\\c&d\end{vmatrix}^{-1}=\frac1{ad-bc}\begin{vmatrix}d&-b\\-c&a\end{vmatrix}$$

# Linear Function
any function with the form $f(x)=mx$

# Linear Program
A generalization of this to $n$ finite vars with:
- a linear function $f(x)$
- the region is defined with linear constraints

## Example
A sandwich is made with peanut butter and jelly. It must have at least 30 grams of sugar and no more than 10 grams of fat.

100 grams of peanut butter contains 10 grams of sugar and 50 grams of fat, costing $0.6
100 grams of Jelly contains 50 grams of sugar and 1 gram of fat, costing $8.

How much peanut butter and jelly must be used so that cost is minimized.
*****
Let $x$ be the number of 100 grams of peanut butter in the sandwich.
Let $y$ be the number of 100 grams of jam in the sandwich.


### Implied Constraints
It must have at least 30 grams of sugar.
$$10x+50y\geq30$$

It must have no more than 10 grams of fat.
$$50x+y\leq10$$

And because $x$ and $y$ represent real objects,
$$x,y\geq0$$

