# Median-Sort-in-C
Understanding the Median Sort

-----------------------------------------------------------------------------------------------
Please enter the number of elements:
10
Please enter the maximum:
50
-----------------------------------------------------------------------------------------------

Random Array:
28	19	5	38	22	44	12	17	35	7	

Sorted Array:
5	7	12	17	19	22	28	35	38	44	
-----------------------------------------------------------------------------------------------

SEARCH:
Please enter the number to be searched:
22

Naive Search:
	Searched Index:	5
Chop Search:
	Searched Index:	5
-----------------------------------------------------------------------------------------------

Commented the benchmark code since it will take a long time...

-----------------------------------------------------------------------------------------------
Benchmark results from previously executed code:
Naive Search:	benchmark_naive:
-----------------------------------------------------------------------------------------------
Parameters: n=2000, max=10000, s=10, mult=1000000
		Elapsed time in milliseconds: 13960568.000000

Parameters: n=2000, max=10000, s=5000, mult=1000000
		Elapsed time in milliseconds: 14033882.000000

Parameters: n=2000, max=10000, s=9000, mult=1000000
		Elapsed time in milliseconds: 14153901.000000

-----------------------------------------------------------------------------------------------
Chop Search:	benchmark_chop:
-----------------------------------------------------------------------------------------------
Parameters: n=2000, max=10000, s=10, mult=1000000
		Elapsed time in milliseconds: 13872250.000000

Parameters: n=2000, max=10000, s=5000, mult=1000000
		Elapsed time in milliseconds: 13605529.000000

Parameters: n=2000, max=10000, s=9000, mult=1000000
		Elapsed time in milliseconds: 13956548.000000

-----------------------------------------------------------------------------------------------

Comments:
-----------------------------------------------------------------------------------------------
* Comments on Elapsed Time:
Overall, it is expected that chop search (O(log n)) would have better performance than the naive search (O(n)).
This is evident from the elapsed time results.

Naive search: As the search element increases from 10 to 5000 and to 9000, the time taken to execute also increases.
This is expected since for larger search elements, more number of statements have to be executed.

Chop search: Here, the 5000 case performed better compared to 10 and 9000.
This is because, the median was found(or not found) in fewer iterations.

* Time Complexity of sorting:

Since mediansort() is a recursive function, called recursively with decrementing n, the time complexity is linear. O(n).
But median sort calls median() every time which has quadratic time complexity O(n^2)(because of 2 nested for loops).
Therefore, the total time complexity is cubic. O(n * n^2) = O(n^3).
The time complexity is the same for best, worst and average cases, since we iterate though all n elements in all the cases.

* Time Complexity of Naive Search:

Best case: In the best case, the first element is the searched element so that the time complexity is O(1).
Worst case: In the worst case, the last element is the searched element so that the time complexity is O(n).
Average case: In the average case, the middle element is the searched element so that the time complexity is O(n/2).

* Time Complexity of Chop Search:

Best case: In the best case, the searched element is same as the random number x so that the time complexity is O(1).
Worst case: In the worst case, the time complexity is O(log n). This also relies on random number x.
Average case: In the average case, the time complexity is O(log n). This also relies on random number x.

-----------------------------------------------------------------------------------------------
