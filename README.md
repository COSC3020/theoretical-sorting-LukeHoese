# Theoretical Sorting

A Computer Science researcher claims to have come up with a sorting algorithm
that can sort arbitrary elements in $O(n)$ time based on comparisons of two
elements at a time. This would be asymptotically faster than any known general
sorting algorithm. The algorithm itself is proprietary and will be sold by a
company.

How would you verify this claim? You may assume that you have access to a
black-box implementation of the sorting algorithm, i.e. you cannot examine the
source code, but you can use it to sort any list you like. Explain in detail
your method for investigating whether X is correct, including any expected
results you would get.

Also give a theoretical argument for why X could or could not be correct, based
on the complexity of the general sorting problem we covered in class.

I would start out a practical test of the algorithms runtime by trying it on edge case lists, and common worst case scenario lists: reverse sorted, nearly sorted but with last element in first index, completely random, increasingly large data sets, lists with repeat elements, lists of different data types (floats, doubles, etc.), etc. I would also do intensive testing over a large set of lists, all random, to see if the run time continues to hold. I would also see how it compares to other common or fast algorithms in similar circumstances to see what data it excels on and what it struggles on to further be able to test it. Given my skepticism below I would expect to see that when testing with a large random data set, which includes edge case tests, the average runtime would level out to a more reasonable nlogn or worse. Comparing to other algorithms I would likely see that it levels out with them and there would be algorithms that test similarly on the same edge cases, and be able to determine at a base level how the sorting algorithm works. You would see how the measured runtime on whatever worst case scenario you find changed as you use larger data sets, as well as how the average changes with larger data sets, and how best case scenario changes with larger data sets. Which should show growth rates that can be corresponded to particular complexities. If the after exhaustively testing the algorithm on large, random, and edge case data sets we saw a runtime that was linear by some factor to the elements of the data sets, it could then be considered that the time complexity of this algorithm is O(n).

Theoretically I would immediately be incredibly skeptical, if not straight up in disbelief of such an algorithm. As we discussed in class it is impossible for a comparison based sorting algorithm to run in a time of O(n) because O(n) is only enough time for one comparison per element, which given we're only comparing two elements at a time simply cannot give enough information to consistently sort in linear time. A given list of n elements has n! permutations, which means a huge growth rate, making it impossible for an algorithm to consistently find the "sorted" permutation of a list in time linear to the amount of elements. With 2 comparisons and n! comparisons this would give a best possible algorithm of O(log2(n!)), or asymptotically simplified to O(nlog2(n)).

Add your answers to this markdown file.
