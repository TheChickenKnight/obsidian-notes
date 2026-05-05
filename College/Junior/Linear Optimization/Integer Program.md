A linear program but with the extra constraint that all variables must be integers.

## Relaxation
The ordinary LP derived from removing the integer constraint from an Integer program.

## Branch & Bound strategy
Example
$$\text{Max }z=x_{1}+2x_{2}$$
$$3x_{1}+2x_{2}\le{4}$$
$$2x_{1}+4x_{2}\le 7$$
$$x_{1},x_{2}\ge 0, \text{INT}$$

### Solve the Relaxation $R$
- Extreme point analysis
- in practice, simplex or two phase method.

We have the points $(0,0)$, $(\frac43,0)$, $(0,\frac72)$, and $(\frac14,\frac{13}8)$
With the last two points both having the highest $z$ value. We will pick the last one arbitrarily. In both cases, $z=3.5$.

Unfortunately, both variables are fractions here. The next step is to pick the fraction which has the largest fractional part. $x_{1}$ has $\frac14$, while $x_2$ has $\frac58$.
### Branching
So we have picked $x_2$, and now we have to branch it into two new constraints:
1. $x_2\le[x_2\text{ value}]$
2. $x_2\ge[x_2\text{ value}]+1$
where $[x]$ finds the closest lower integer.
we find that $2\le x_2\le1$

Now, we incorporate the new constraints into the previous solved tableau to perform dual simplex for each constraint.

for $x\le1$, we find new feasible points, and that the OS is $(\frac23,1)$, $z=2.6666$
for $x\ge 2$, we can find that this is infeasible with the rest of the constraints.

Even this new OS still has a fraction, so we have to branch again.

we get $x\le0$ and $x\ge1$. Two more branches. continue. once your branches are all ended, then you can see which has the largest z. that is your IP's OS.