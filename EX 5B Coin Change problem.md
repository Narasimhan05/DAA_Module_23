# EX 5B Coin Change Problem
## DATE:
## AIM:
To Create a Python Function to find the total number of distinct ways to get a change of 'target'  from an unlimited supply of coins in set 'S'.

## Algorithm
1. Base Cases: If target is 0, return 1 way; if target is negative or no coins left, return 0 ways.
2. Include current coin: Recursively find ways by subtracting the current coin from the target.
3. Exclude current coin: Recursively find ways by moving to the next coin without using the current one.
4. Sum results: Add the ways found by including and excluding the current coin.
5. Repeat until all possibilities are explored and summed.  

## Program:
### Developed by: NARASIMHAN S 
### Register Number: 212223230133 
```python
def count(S, n, target):
    if target == 0:
        return 1
    if target < 0 or n < 0:
        return 0
    incl = count(S, n, target - S[n])
    excl = count(S, n - 1, target)
    return incl + excl
    
if __name__ == '__main__':
    S = []
    n=int(input())
    target = int(input())
    for i in range(n):
        S.append(int(input()))
    print('The total number of ways to get the desired change is',
        count(S, len(S) - 1, target))
```
## Output:

![image](https://github.com/user-attachments/assets/36b8eebb-8156-4bbc-901e-9f5d138a4cd7)

## Result:
Thus the program was executed successfully for finding the total number of distinct ways to get a change of 'target' from an unlimited supply of coins in set 'S'.
