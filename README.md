SUMMARY

Insights
 
•	Efficient algorithm takes time twice as much as the basic algorithm.
•	Efficient algorithm takes n times lesser memory than basic algorithm.
•	Therefore, it is a trade-off between time & memory. 
•	Basic algorithm uses a lot of memory compared to the efficient algorithm’s time consumption.
•	In reality, memory is very expensive while computing time can be reduced using efficient machines.
•	In sequence alignment, the amount of memory required is in billions. Thus, basic algorithm requires a huge amount of memory.
Graph1 – Memory vs Problem Size (M+N)
 

Nature of the Graph (Logarithmic/ Linear/ Polynomial/ Exponential)

Basic: The memory increases in polynomial time.
Efficient: The memory is almost constant up to a point and then there is a slight increase and overall runs in polynomial time.


Explanation: 
In the Basic algorithm, m represents the size of word X and n represents the size of word Y. The memory required to compute in this algorithm grows quadratically with respect to the problem size, which is O(nm). We use divide and conquer in the Efficient algorithm to make the solution memory efficient. We divide the string Y in two equal halves. We compute the optimal point for string X by first running the DP recurrence method on X and Y's first half. Then we reverse X and Y's last half and use the DP's recurrence method to find the point for X. Thus, memory usage is greatly reduced in this manner.

Graph2 – Time vs Problem Size (M+N)
 
Nature of the Graph (Logarithmic/ Linear/ Polynomial/ Exponential)

Basic: As problem size increases, there’s a polynomial increase in the runtime which is proportional to O(m*n).
Efficient: As the problem size increases, there’s a polynomial increase in the runtime which is proportional to O(2*m*n).

Explanation: 
In the basic algorithm, we create a 2D table for the Dynamic approach with m rows and n columns using Dynamic programming. First, both X and Y strings are computed from the input, and then we simply execute the DP recurrence formula recursively on the two strings. In the recurrence formula, we take the minimum of the gap in front of X and Y-1, the gap in front of Y and X-1 and Y-1, and X-1 while taking alpha values into account. After that, perform a top-down pass to find the optimal solution. If there is a match with the diagonal element, we have paired the two values; if we move diagonally, there is a gap in front of both strings. There is a gap in front of Y-1 if we move vertically; otherwise, we move horizontally. As a result, there is a space in front of X-1. To get the actual alignment, reverse both alignment values because we came from the top down. 

Time complexity: O(m*n) 
In the Efficient approach, we divide the string Y into two halves using Divide and Conquer methods and perform more comparisons in a 2D table for instance of Y to instance of X. As a result, it takes longer than the basic approach but is still limited to the size of X and Y time complexity: O(2*m*n).
