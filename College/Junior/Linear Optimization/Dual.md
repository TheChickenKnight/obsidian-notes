## Example
Taking the dual of this primal[^1] LP
$$\text{Max } z=3x_{1}-4x_{2}$$
$$x_{1}-5x_{2}\le3$$
$$-4x_{1}+5x_{2}\le 5$$
$$6x_{1}-7x_{2}\le 8$$
$$x_{1},x_{2}\ge 0$$

And then the Dual:
$$\text{Min }z'=3w_{1}+5w_{2}+8w_{3}$$
$$1w_{1}-4w_{2}+6w_{3}\ge 3$$
$$-5w_{1}+5w_{2}-7w_{3}\ge -4$$
$$w_{1},w_{2},w_{3}\ge 0$$
*literally just the transpose*

[^1]: a primal LP is the LP that will have the dual taken of it.

****
$$\text{Min }z'=\vec{b}^T\vec{w}$$
$$A^T\vec{w}\ge \vec{c}$$
$$\vec{w}\ge \vec{o}$$

$$\text{Max }z''=(-\vec{b})^T\vec{w}$$
$$(-A^T)\vec{w}\le -\vec{c}$$


$$\text{min }z=x_{1}-2x_{2}+x_{3}$$
$$-3x_{1}-11x_{2}+x_{3}\ge -5$$
$$9x_{1}+8x_{2}+7x_{3}\ge 19$$




$$\text{max }z'=-5w_{1}+19w_{2}$$
$$-3w_{1}+9w_{2}\le 1$$
$$-11w_{1}+8w_{2}\le -2$$
$$w_{1}+7w_{2}\le 1$$
****
