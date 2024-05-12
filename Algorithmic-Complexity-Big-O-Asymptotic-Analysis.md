## Algorithmic Complexity/Big-O/Asymptotic Analysis ##

Asymptotic Notation - CS50
- Formal Definition: f(x) runs on the order of g(x) if there exists an x0 and constant C where f(x) <= C*g(x) where x > x0
- Analyzes how a program's runtime grows as the size of the input grows
- For example, counting the number of characters in a given string runs in O(n) or linear time
- However, if we know and store the length before even getting the string, we can access the variable in O(1) or constant time. This takes more storage to keep the variable
- log(n) < n < n^2
- Best case: Omega
- Worst case: Big-O
- When best and worst case are the same: Theta

Big O Notations - Derek Banas
- Measuring how well a computer algorithm scales as the amount of data increases
- When dealing with large numbers, the largest scaling variable in the equation is the one that affects the efficiency the most (5n^3 + 6n^2 would be more affected on O(n^3))
- Constant time executes in the same amount of time no matter the size of the data
- Example of O(n): linear search through a list
- Example of O(n^2): bubble sort algorithm
- Example of O(log(n)): binary search algorithm on already sorted data
- Example of O(n log(n)): quick sort algorithm (less than n^2 but more than n)