Listing Method
*Traditional Counting*
List all possible outcomes of the experiment 
## Example
Sample space[^1] of rolling 1 die:
$$\{1,2,3,4,5,6\}$$

## Tree Diagram

### Example
Sample space[^1] of tossing a coin twice.

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2025.9.16 - 18.26pm.drawing",
	"width": 733.2890625,
	"aspectRatio": 1.901278902056555
}
```
$$S=\{(H,H), (H,T), (T,H), (T,T)\}$$
****
# Fundamental Principle of Counting
If an experiment has $k$ repeated tasks. If the $k$th task can be done in $n_k$ ways, then the total number of outcomes of the task is given by:
$$n_1\times n_2 \times ... \times n_k$$

## Examples
### 4 digit odd numbers > 3000
$$7\times10\times10\times5$$

### even numbers > 3000


### odd numbers > 3000 without repetition
# Permutations and Combinations

## Example
I have 3 phone numbers of men and 4 phone numbers of women. How many different ways can I list them if the 3 men have to be next to each other?

### Solution
In any problem where multiple elements must remain together, consider them as one.

Now, we have the 1 element of male phone numbers and 4 elements of female phone numbers. There are $5!$ ways to list these.

Also, there are $3!$ ways to order the men, so together that's $3!\times 5!$.

\_ \_ \_ \_ \_ \_ \_

m f f m f m  f f   3! x 3! x 2!     $$\frac{7!}{6!\times}$$

## Example
For the letters of **ATTRACT**, the number of distinguishable arrangements is
$$\frac{7!}{3!\times2!}$$
For the letters of **BANANA**, the number of distinguishable arrangements is
$$\frac{6!}{3!\times2!}$$

## Permutation Formula
- Order is important
Arrangements of $n$ items taken $r$ at a time
$$_nP_r=\frac{n!}{(n-r)!}$$
## Combination Formula
- Order is not important
Subsets of $n$ items taken $r$ at a time
$$_nC_r=\frac{n!}{r!(n-r)!}=\frac{_nP_r}{r!}$$

# Counting of Problems Involving "Not" or "Or"
## "OR" Problems
1.  $S$ and $n(S)$
2.  Define Sets from world problem
3. Find Cardinality of Sets
4. Write the formula & substitute values.
## "NOT" Problems
$$|S|=|A|+|A'|$$


[^1]: The Set of all possible outcomes, $S$


```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2025.9.18 - 16.06pm.drawing",
	"width": 500,
	"aspectRatio": 1
}
```
