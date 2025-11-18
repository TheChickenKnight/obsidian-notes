---
share_link: https://share.note.sx/70mtg060#J1QfLqyIgnyr4JJJrnw+rXdJv8jmeqEy88zBUhuckmU
share_updated: 2025-10-20T13:48:49-04:00
---
# Formula
Consider Sample space $S$ and the Subset $A \subseteq S$, and the probability of $A$ out of $S$ be $P(A)$:
$$S_i\rightarrow P(A)=\frac{|A|}{|S|}$$
# Example
Out of 3 children, what's the probability for getting at least 1 girl?

Let $A$ be the set of at least one girl.
Then, $A'$ is the set of the possibility of 3 boys.
$|S|=2^3$, and $|A|=|S|-|A'|$,
so 
$$|A| = 2^3-1=7$$****
> **Odds**
> If all outcomes in a sample space are equally likely, $a$ of them are favorable to the event $E$, and the remaining $b$ events against $a$, then $P(E)=\frac{a}{a+b}$

*****
# Conditional Probability
The probability of event $B$, computed on the assumption that event $A$ has happened, is called the **conditional probability of $B$ given $A$** and is denoted $$P(B|A)=\frac{P(A\cap B)}{P(A)}=\frac{\frac{|A\cap B|}{|S|}}{\frac{|A|}{|S|}}=\frac{|A\cap B|}{|A|}$$
## Example

Toss a coin 3 times. Given we roll a head on the first roll, what's the probability of having two heads?

### List elements of $A$
$$A=\{(H,H,T),(H,H,H),(H,T,H),(H,T,T)\}$$
### List elements of $B$
$$B=\{(H,H,T),(H,T,H),(T,H,H)\}$$
### Use formula
$$P(B|A)=\frac{|A\cap B|}{|A|}=\frac{2}{4}$$

To prove two events are independent, show it
****
# Baye's Theorem
lets say $P(A),P(B), P(B|A)$ are given for $S$, $A$&$B\in S$ 
what is $P(A|B)?$

We know $$P(A|B)=\frac{P(A\cap B)}{P(B)}$$
and that 
$$P(A\cap B)=P(A)P(B|A)$$
so,
$$P(A|B)=\frac{P(A)P(B|A)}{P(B)}$$
## Example
Suppose a new disease test has a 95% chance to correctly identify a sick patient and a 10% chance to incorrectly identify a healthy patient as sick. Assume 5% of the population has the disease. **What is the probability that a person who's tested positive is really sick?**
### Given
We know
$$P(A)=0.05,P(A')=0.95$$
Where $A$ is the given probability of getting a truly sick patient.

We also know that $$P(B|A)=0.95,P(B'|A)=0.05$$
Where $B$ is the population who is tested positive and that
$$P(B|A')=0.1,P(B'|A')=0.9$$

We are asked to get
$$P(A|B)$$
### Formula
$$P(A|B)=\frac{P(A)P(B|A)}{P(B)}$$
However, there are two cases where $P(B)$ occurs. These are true and false positives.
So,
$$P(A|B)=\frac{P(A)P(B|A)}{P(A\cap B)+P(A'\cap B)}=\frac{P(A)P(B|A)}{P(A)P(B|A)+P(A')P(B|A')}$$
And now to fill in numbers:
$$P(A|B)=\frac{(0.05)(0.95)}{(0.05)(0.95)+(0.95)(0.1)}$$
******
# Probability Mass Function
A function where there is some constant $c$ and a function that all values of $x$ will output 1 together.

Let $X$ be a discrete random variable with probability mass function $p(x)=P(X=x$.)

The mean of $X$ is given by
$$\mu_x=\sum_xxP(X=x)$$
where the sum is over all possible values of $X$.
	The mean of $X$ is sometimes called the expectation, or expected value, of $X$ and may also be denoted by $E(X)$ or by $\mu$.
## Example
Toss a coin 3 times. Find the expected value of number of heads. 

Let $X$ be the number of heads.
$i$ can be $0,1,2,3$

| x=i |     | P(x=i)    |
| --- | --- | --------- |
| 0   |     | $\frac18$ |
| 1   |     | $\frac38$ |
| 2   |     | $\frac38$ |
| 3   |     | $\frac18$ |

$E(x)=\sum i P(x=i)$

$$=0(\frac18)+1(\frac38)+2(\frac38)+3(\frac18)$$
$$=\frac32=1.5\text { heads}$$

## Example
A player pays $3 to play the following game: He tosses three fair coins and receives back payoffs of $1 if he tosses no heads, \$2 got one head, \$3 got two heads, and \$4 for three heads. Find the player's expected net winnings for this game.

For net winning , each $i$ must be the net gain from each outcome.

| # of heads | P(x)      | Gross($) | Net($) |
| ---------- | --------- | -------- | ------ |
| 0          | $\frac18$ | 1        | -2     |
| 1          | $\frac38$ | 2        | -1     |
| 2          | $\frac38$ | 3        | 0      |
| 3          | $\frac18$ | 4        | 1      |

$$E(x)=\sum i P(x=i)=-2(\frac18)+-1(\frac38)+0(\frac38)+1(\frac18)=-0.5$$
*****
if $E(x)=0$, then a game can be considered a **fair game**, $E(x)<0$, then it is unfair against the player. If $E(x)>0$, then the game is unfair in favor of the player.



$$Var(x)=\sum i^2P(X=i)-\mu^2=E(x^2)-(E(x))^2$$

