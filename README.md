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

We should start with the definition of a good pivot. A good pivot creates two partitions of size at most 3n/4. That means inside of a sorted list a good pivots exists between n/4 and 3n/4. This means that half of the elements are good pivots in a random list. This means the possibility of picking a good pivot by selecting the first, last, or random elements is all the same at 50%. 

The Median-of-three method considers this when attempting to pick a good pivot. It takes the medium of the first, middle, and last elements. Each element has a 50% chance of being a good pivot. It also knows that inside a sorted list, good pivots exist between n/4 and 3n/4, so it takes the medium of the three elements. This means the Median-of-three method has an 87.5% chance of picking any good pivot.

I got that by taking the percentage chance of each of the elements not being a good pivot, which is 50%, and multiplying them together

.5 *.5*.5 =.125, Meaning there is a 12.5% chance of the Median-of-three method not finding a good pivot and then 1 - .125 to get the percent chance of at least one being a good pivot 87.5%. Selecting the median of the three elements is the best way to figure out which is a good pivot. So the Median-of-three percent chance of picking a good pivot is 87.5%.



For this assignment, I used the resources of lecture01-sorting.pdf.

"I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice."
