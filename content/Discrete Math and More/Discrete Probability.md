---
tags:
  - Discrete-Math
---


A probability is a number between 1 and 0 associated with an event.

It captures the likelihood of the event occurring as a consequence of a random experience.

Probability = 0, Event never happens
		 = 1 , Event always happens


***Inclusion Exclusion***

$| A \cup B | = |A| + |B| - | A \cap B |$


Example:

What is the probability that a positive integer from the set {1,2,3...,99,100} is divisible by 2 or 5?

$E_1$ divisible by 2
$E_2$ divisible by 5

So do divisible by 2 + divisible by 5 - divisible by both because they would be counted twice.

Divide 100 by 2, 5, 10 for these values

$= 50/100 + 20/100 -10/100=3/5$



***Uniform Distribution***

This assigns the probability 1/n to each element of set S

In a biased die, 3 appears twice as often as each other number, and the other five outcomes are equally likely. 


Now we have 7 sides essentially, therefore considering 1,3,3,5 the answer is 4/7.


***Conditional Probability***

Let E and F be events with p(F) > 0. The conditional probability of E given F, denoted by p(E|F) is defined as

$$p(E|F)= \frac{p(E\cap F)}{p(F)}$$
Example: 

A bit string of length 4 is generated at random and each of the 16 bit strings of length 4 is equally likely. What is the probability that a string contains at least two consecutive 0's, given that its first bit is a 0?

first find $p(F)$ ~ Probability of the first bit being 0.

Total is $2^4$ = 16. There is a 1/2 chance the first bit is 0, so $\frac{8}{16}$ will be $\frac{1}{2}$.

 $p(E\cap F)$ means probability they both occur. SO what is the combined probability that a string contains two consecutive 0s AND the first bit is 0.


{0000, 0100, 0011, 0001, 0010} = $\frac{5}{16}$

$$\frac{5/16}{1/2} = \frac{5}{8}$$


***Independent Probability*** 

This made up part of our conditional probability, but it exists on its own.

$$p(E \cap F) = p(E)p(F)$$

Example: Any event *with* replacement.

1. Choose a card from a 52 card deck. Put it back. What are the odds of choosing a jack and then an 8?$$\frac{4}{52} \cdot \frac{4}{52}$$ 
2. Events E and F are independent if an only if:
	1. $p(E \cap F) = p(E)p(F)$
	2. $p(E|F) = p(E)$
	3. $p(F|E) = p(F)$
	Note: '|' means given that


***Bernoulli Trials***

If an experiment can have only two possible outcomes, each 'run' is called a *Bernoulli trial*. One outcome is called a success and one is called a failure. If p is success probability and q is failure probability, p + q = 1.

If a coin has a 2/3 chance to be heads and 1/3 to be tails, then what is the probability exactly four heads occur when the coin is flipped seven times. 

$$(\frac{2}{3})^4(\frac{1}{3})^3 \cdot C(7,4)$$

This is because each flip is independent, multiplying the probabilities is the probability of us getting 4 heads in one pattern. C(7,4) 7choose4 shows that the head spots don't have to be back to back, and there are 7choose4 ways that this successful output can appear.

This directly ties with binomial distribution.


***Binomial Distribution***

The probability of exactly k successes in n mutually independent Bernoulli trials, withe probability of success p is given by the binomal distribution

$$b(k;n,p) = C(n,k)p^kq^{n-k}$$
This is exactly the form we discovered when applying Bernoulli trials.


Remaining Topics in Discrete Probability
- [[Bayes Theorem]]







**this note was imported from my other vault, ideas are not complete :(**




[[Discrete Math]]