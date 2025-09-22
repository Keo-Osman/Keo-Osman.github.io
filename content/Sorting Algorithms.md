#Computer-Science, #Maths/Algorithms 
# Bubble Sort - $O(n^{2})$
1. Iterate over the array and swap elements that are out of order. 
2. Repeat until you iterate with no swaps.

# Shuttle Sort - $O(n^{2})$
*Slightly more efficient than bubble sort*
1. 1st pass - compare the 1st and 2nd numbers and swap if necessary
2. 2nd pass - compare the 2nd and 3rd. If a swap has occurred compare the 1st and new 2nd.
3. Repeat. If a swap occurs check previous elements.
# Quick Sort - $O(n\log n)$
1. Pick a pivot in the middle
2. Put all numbers bigger than the pivot in one sub list and all numbers less in another sub list.
3. Repeat for each sub list recursively
4. When a sub list has one element it's sorted.
# Interchange Sort - $O(n^{2})$
1. Iterate over the list to find the smallest number and put it 1st in a new list and remove it from the original list.
2. Iterate again adding the smallest element to the new list and repeat.