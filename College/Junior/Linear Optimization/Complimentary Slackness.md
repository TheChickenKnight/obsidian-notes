
Primal:
$$\text{Max }z=\vec{C}^T\vec{x}$$
$$A\vec{x}\le\vec{b}$$
$$\vec{x}\ge \vec{0}$$

With slack variables, becomes
$$A\vec{x}+\vec{S}=\vec{b}$$
$$\vec{S}\ge \vec{0}$$

Dual:
$$\text{Min }z'=\vec{b}^T\vec{w}$$
$$A^T\vec{w}-\vec{v}=\vec{C}$$
$$\vec{w},\vec{v} \ge \vec{0}$$

Suppose $\vec x ^{(0)}$ is an OS to P and $\vec w^{(0)}$ to D
Then, Complimentary Slackness relates them to slack. We can derive and then write


$$A\vec{x}^{0}+\vec{S}=\vec{b}$$
$$A^T\vec{w}^{(0)}-\vec{v}^0=\vec{C}$$
$$\vec{x}^0, \vec{s}^0,\vec{w}^0,\vec{v}^0\ge\vec{0}$$

$$\vec{C}^T\vec{x}^{0}=\vec{b}^T\vec{w}^{0}$$
We can use these to create
$$\vec{w}^{0^T}\vec{s}^0+\vec{x}^T\vec{v}^0=\vec{0}$$

But, because we know that these vectors are non-negative and equal 0, they have to all be equal to the 0 vector.
$$\vec{w}^{0^T}\vec{s}^0=\vec{0}$$
$$\vec{x}^T\vec{v}^0=\vec{0}$$

What this all means is that at the OS Pair, the $i$th primal variable multiplied by the $i$th dual slack equals 0 and vice versa.


******

$$\text{Max }z=-x_{1}-3x_{2}$$
$$-x_{1}-x_{2}\le{-2}$$
$$x_{2}-x_{2}\le -1$$
$$x_{1},x_{2}\ge 0$$

Given the OS is $(\frac12,\frac32)$

The Dual would be

$$\text{Min }z'=-2w_{1}-w_{2}$$
$$-w_{1}+w_{2}-v_{1}=-1$$
$$-w_{1}-w_{2}-v_{2}=-3$$