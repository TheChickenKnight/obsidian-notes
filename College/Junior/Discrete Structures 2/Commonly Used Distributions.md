# Discrete Random Variable
A variable, $X$, which is the number of "successes", which depends on the problem.
# Bernoulli Distribution
If I have a discrete random variable $X$, with the different values $i$, if I go through the trial exactly $n=1$ time, $X=1$ when you get the success. $X=0$ when we get a failure. Then, this discrete random variable follows a Bernoulli Distribution with parameter $p$, probability of success. $X\sim\text{Bernoulli}(p)$

## Expected Value
$$\mu_x=E(x)=p$$
## Variance
$$\sigma_x^2=\text{Var}(x)=p(1-p)=pq$$
## Example
After scoring a touchdown, a football team may elect to attempt a two-point conversion, by running or passing the ball into the end zone. If successful, the team scores two points. For a certain football team, the probability that this play is successful is $0.40$.

- Let $X=1$ if successful, $X=0$ if not. Find the mean and variance of $X$.

$X$ can only be 0 and 1, and a certain football team's probability of this play means $n=1$


This means $X$ follows the Bernoulli Distribution.
$$X\sim\text{Bernoulli}(0.40)$$
*****

- If the conversion is successful, the team scores 2 points; if not the team scores 0 points. Let $Y$ be the number of points scored. Does $Y$ have a Bernoulli distribution? If so, find the success probability. If not, explain why not.

Even though there are only two cases, the cases are 0 and 2 here, representing a score, not 0 and 1, representing two cases. Therefore, this isn't a Bernoulli Distribution.

# Binomial Distribution
Consider a Bernoulli trial repeated for $n\gt1$, with each trial independent from others.

Consider the Discrete Random Variable $X$ as the number of successes 

$$X\sim\text{Bin}(n,p)$$

Where $p$ is the probability of success

## Expected Value
$$\mu_x=E(x)=np$$
## Variance
$$\sigma_x^2=\text{Var}(x)=np(1-p)=npq$$

## Probability Function
$$P(X=i)= _nC_i p^iq^{n-i}$$Where $q$ is the probability of failure, or $1-p$


****
# Geometric Distribution
Let $X$ be the number of trials **up to and including** the **first** success.

Then,
$$X\sim\text{Geom}(p)$$

## Probability Function
$$P(X=i)=(1-p)^{i-1}p=pq^{i-1}$$

## Mean/Expected value
$$\mu_x=\frac1p$$

## Variance
$$\sigma_x^2=\frac{1-p}{p^2}=\frac q{p^2}$$

# Negative Binomial
an extension of **geometric distribution**
$$NB(1,p)=Geom(p)$$

Let $X$ be the number of trials up to and including $r$ successes, where $p$ is the probability of a success, then

$$X\sim NB(r,p)$$

## Probability
$$P(X=i)=_{i-1}C_{r-1}p^{r-1}q^{i-r}p$$
## Mean/Expected Value
$$\mu_x=\frac rp$$
## Variance
$$\sigma _x^2= \frac{r(1-p)}{p^2}=\frac{rq}{p^2}$$
# Hypergeometric Distribution
Assume a finite population contains $N$ items, of which $R$ are successes and $N-R$ are failures. Assume that $n$ items are sampled from the population, and let $X$ represent the number of successes in the sample. Then,
$$X\sim H(N,R,n)$$
## Probability
$$P(x=i)=\frac{(_RC_x)(_{N-R}C_{n-x})}{_NC_n}$$