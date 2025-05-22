# EX 5A Minimum Cost Path
## DATE:
## AIM:
To Write a python program to Implement Minimum cost path using Dynamic Programming.

## Algorithm
1. Initialize a 2D array tc with the same dimensions as cost and set tc[0][0] to cost[0][0].
2. Fill the first column of tc by adding the current cost to the value above it.
3. Fill the first row of tc by adding the current cost to the value to its left.
4. For the remaining cells, tc[i][j] is the minimum of tc[i-1][j-1], tc[i-1][j], and tc[i][j-1], plus cost[i][j].
5. Return the value at tc[m][n]. 

## Program:
### Developed by: NARASIMHAN S 
### Register Number: 212223230133 

```python
R = int(input())
C = int(input())
def minCost(cost, m, n):
    tc = [[0 for x in range(C)] for x in range(R)]
    tc[0][0] = cost[0][0]
    for i in range(1, m+1):
        tc[i][0] = tc[i-1][0] + cost[i][0]
    for j in range(1, n+1):
        tc[0][j] = tc[0][j-1] + cost[0][j]
    for i in range(1, m+1):
        for j in range(1, n+1):
            tc[i][j] = min(tc[i-1][j-1], tc[i-1][j], tc[i][j-1]) + cost[i][j]
    return tc[m][n]
 
cost = [[1, 2, 3],
        [4, 8, 2],
        [1, 5, 3]]
print(minCost(cost, 2, 2))

```
## Output:

![image](https://github.com/user-attachments/assets/14938fb3-16f8-44ab-b3b2-544e49471ab8)

## Result:
Thus the above program was executed successfully for finding Minimum cost path using Dynamic Programming.
