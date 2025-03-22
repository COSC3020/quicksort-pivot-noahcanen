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


We should start with having an idea of what the theoretical perfect pivot for quicksort would be. The theoretical perfect pivot for quicksort is the median of the array. This is because it would create two partitions of n/2. So, a good pivot would be a number that would be at least close to these partitions of n/ 2. This means that although there is only one perfect pivot in a random array, there could be several good pivots in that same array. 
I will analyze this from the perspective of which algorithm is more likely to select the perfect pivot inside a random array. I will justify this by stating that if this method is more likely to catch, the perfect pivot is also more likely to catch a good pivot. Let's start with the baseline of picking the first number in the array as the pivot. This number has a 1/n chance of being the perfect pivot inside a random array. 
The Median-of-three method of picking a pivot inspects the first, middle, and last elements of the part of the array under consideration and chooses the median value. This number has a 3/n chance of being the perfect pivot because it inspects three values. 
This means that The Median-of-three method is 3 times more likely to Pick a good pivot than the first number method.

For this assignment, I used the resources of lecture01-sorting.pdf.

"I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice."
