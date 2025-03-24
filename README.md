# Quicksort Pivots

in the lectures I only briefly mentioned strategies for determining a good pivot
for quicksort. The implementation on the slides simply picks the leftmost
element in the part of the array that we consider as a pivot. I also mentioned a
few other ways of picking a good pivot, e.g. randomly.

Median-of-three is also a good way of picking a pivot -- inspect the first,
middle, and last elements of the part of the array under consideration and
choose the median value. Using the probabilities for picking a pivot in a
particular part of the array (in the same way as we did on slide 34), argue
whether this method is more or less (or equally) likely to pick a good pivot
compared to simply choosing the first element. Assume that all permutations are
equally likely, i.e. the input array is ordered randomly.

Your answer must derive probabilities for choosing a good pivot and
quantitatively reason with them.

Add your answer to this markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

We should start with the definition of a good pivot. A good pivot creates two partitions of size at most 3n/4. That means good pivots exist between n/4 and 3n/4 inside a sorted list. Half of the elements are good pivots in a random list. This means the possibility of picking a good pivot by selecting the first, last, or random elements is all the same at 50%. 


The Median-of-three method selects 3 elements: the first, the middle, and the last, and then selects the medium of those three elements as the pivot.


This means that this method has four outcomes 
1.	all three elements selected are good pivots
2.	two elements selected are good pivots
3.	one element selected is a good pivot
4.	none of the elements selected are good pivots


Scenario one has a 12.5% chance of happening. I got this by multiplying the percent chance that each element is a good pivot. No matter which element is packed, it will be a good pivot in this scenario. So, the percentage chance of this scenario happening and picking a good pivot is 12.5%


Scenario 2 has a 12.5% chance of happening. I got this by multiplying the percentage chance of two elements being good and one being bad. There are three different possibilities in scenario 3: the first element is bad, the middle element is bad, and the last element is bad. Because we take the medium of these three elements 100% of the time, we will select a good pivot out of the three scenarios. This means we must multiply .125 * 3 * 1  = .375%.   There is no possibility of choosing the bad pivot since we are taking the median of the three. So, the percentage chance of this scenario happening and picking a good pivot is 37.5%


Scenario 3 has a 12.5% chance of happening. I got this by multiplying the percentage chance of one element being good and two being bad. There are three different possibilities in scenario 3: the first element is good, the middle element is good, and the last element is good. Because we take the medium of these three elements 50% of the time, we will select a good pivot out of the three scenarios. This means we must multiply .125 * 3 * .5  = .1875%. So, the percentage chance of this scenario happening and picking a good pivot is 18.75%


Scenario 4 has a 12.5% chance of happening. I got this by multiplying the percent chance that each element is a bad pivot. There is no possibility of selecting a good pivot since all chosen elements are bad in this scenario. So, the percentage chance of this scenario happening and picking a good pivot is 0%

 So, adding up the percent chance of each scenario, we get that The Median-of-three method  has a 68.75% chance of selecting a good pivot

Means that this method is 18.75 % more likely to select a good pivot than the first element method.



For this assignment, I used the resources of lecture01-sorting.pdf.

"I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice."
