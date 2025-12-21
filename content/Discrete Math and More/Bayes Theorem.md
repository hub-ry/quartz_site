
Example (Using Bayes' without definition):

Two boxes: 

The first contains two green and seven red balls.
The second contains four green balls and three red balls.

Bob selects a ball by 

1.)  First choosing one of the two boxes at random.
2.) Selecting one of the balls in this box at random.

What is the probability that he selected a ball from the first box, given that the ball is red?

find p(box1 and red) and p(box 2 and red)

1.) $7/9 \cdot 1/2 = 7/18$
2.) $3/7 \cdot 1/2 = 3/14$

Therefore p(red) = $7/18 + 3/14 = 0.603$

$$p(box1 | red) = \frac{p(\text{box1 and red})}{p(red)}= 49/76$$


***Bayes' Theorem Formula***

$$p(F | E) = \frac{p(E|F)p(F)}{p(E|F)p(F)+p(E|\overline{F})p(\overline{F})}$$

Note: the line above f means complement of; 1-p(F)



***Example using this new idea:***

Suppose 1 out of every 1000 computer chips has a defect. The test to discover defects is successful with a probability of .99. 

If the chip does not have a defect, the test will inaccurately report that it does 0.02 probability.

Q: If the outcome of a test indicates that there is a defect, what is the likelihood that the chip is actually faulty.


p(actually faulty given the test says there is a defect)

so actually faulty is F, test says defect is E 

(probability there is defect given the test is faulty) * (probability actually faulty) 

/

probability (defect given faulty)(actually faulty + (Defect but not faulty)(not actually faulty))


ok break down these statements one more time:

(defect given faulty): '  
If the chip has a defect, the test will discover the defect with  
probability 0.99.'

(actually faulty): '0.001 because one out of every 1000 chips has a defect.'

(Defect but not actually faulty): 'If a chip does not have a defect, the test reports that  
it has a defect with probability 0.02.'

(not actually defect): .999 (1 out of 1000 are defect so 1-.001)

plugging these values into formula gives 0.047 ^^


Apparently this has applications in spam filters lol.






**this note was imported from my other vault, ideas are not complete :(**