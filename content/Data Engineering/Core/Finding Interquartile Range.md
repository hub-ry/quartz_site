
IQR is a vital concept, particularly for visualizing data spread and detecting unusual values.

IQR measures the statistical dispersion that describes the middle 50% of your data.

Q1 - Value below 25% of data.

Q2 - Midpoint - 50% of scores are below this value

Q3 - Value below which 75% of the data falls 

Maximum Score

IQR = Q3-Q1

***Example walkthrough:***

`[0,13,14,19,21,23,40]`

7 values: Q2 = 7+1 / 2 = 4th positon

Now 3 on each side. 

3+1 /2 = 2, 2nd value, so now you can say 

Q1 = 13
Q2 = 19
Q3 = 23

IQR = 23-13 = 10

Lower Bound = 13 - (1.5 * 10) = -2
Upper Bound = 23- (1.5 * 10) = 38


**NOTE - the 1.5 is specific to the boxplot method.



lost? ~ [[Index - Data Engineering]]