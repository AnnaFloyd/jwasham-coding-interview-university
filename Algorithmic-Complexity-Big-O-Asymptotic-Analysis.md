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

Big Oh Notation (and Omega and Theta) - Prof Bill Byrne
- f(n) is O(g(n)) if there's a constant C and n0 such that f(n) <= C*g(n) for all n > n0
- Example:
f(n) = 4n^2 + 16n + 2
Is f(n) -> O(n^4)?

| n | C | 4n^2 + 16n + 2 | C*n^4 |
| --- | --- | --- | --- |
| 0 | 1 | 2 | 0 |
| 1 | 1 | 22 | 1 |
| 2 | 1 | 50 | 16 |
| 3 | 1 | 86 | 81 |
| 4 | 1 | 130 | 256 |
- When C = 1, f(n) -> O(n^4) if n >= 4.
-  f(n) is Ω(g(n)) if there's a constant C and n0 such that f(n) >= C*g(n) for all n > n0
- Example:
f(n) = 4n^2 + 16n + 2
Is f(n) -> Ω(n^2)?

| n | C | 4n^2 + 16n + 2 | C*n^2 |
| --- | --- | --- | --- |
| 0 | 1 | 2 | 0 |
- When C = 1, f(n) -> Ω(n^4) if n >= 0.
- Is f(n) -> Ω(n^3)?
4n^2 + 16n + 2 > C*n^3
Note: C must be a positive number
- No, because 4n^2 will never overpower C*n^3
- f(n) is Θ(g(n)) iff f(n) is O(g(n)) and f(n) is Ω(g(n))
- Using f(n) from previously
- Is f(n) -> Θ(n^2)?
- We have shown previously that f(n) -> Ω(n^2) when C = 1 and n0 = 0
- Is f(n) -> O(n^2)?
4n^2 + 16n + 2 < C*n^2

| n | C | 4n^2 + 16n + 2 | C*n^2 |
| --- | --- | --- | --- |
| 0 | 5 | 2 | 0 |
| 1 | 5 | 22 | 5 |
| 2 | 5 | 50 | 20 |
| 3 | 5 | 86 | 45 |
| 4 | 5 | 130 | 80 |
| 5 | 5 | 182 | 125 |
| 6 | 5 | 242 | 180 |
| 7 | 5 | 310 | 245 |
| 8 | 5 | 386 | 320 |
| 9 | 5 | 470 | 405 |
| 10 | 5 | 562 | 500 |
| 11 | 5 | 662 | 605 |
| 12 | 5 | 754 | 720 |
| 13 | 5 | 886 | 845 |
| 14 | 5 | 1010 | 980 |
| 15 | 5 | 1142 | 1125 |
| 16 | 5 | 1282 | 1280 |
| 17 | 5 | 1430 | 1445 |
- When C = 5 and n0 = 17, then f(n) -> O(n^2).
- Therefore, f(n) -> Θ(n^2).
- n^2 is the smallest value for O(n^2) possible. This is basically what Θ is showing, but common practice is to use Big Oh to state the best upper bound you can have