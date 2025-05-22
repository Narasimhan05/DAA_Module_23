# EX 5D Minimum Jump to Reach End Array
## DATE:
## AIM:
To Create a python program to find Minimum number of jumps to reach end  of the array using naive method(recursion)

## Algorithm
1. Base Cases: Return 0 if already at the end, or infinity if stuck (current element is 0).
2. Initialize min jumps to infinity.
3. Iterate through all reachable indices from the current position.
4. Recursively find the minimum jumps from each reachable index and add 1 for the current jump.
5. Return the overall minimum jumps found.   

## Program:
### Developed by: 
### Register Number:  
```python
def minJumps(arr, l, h):
    if (h == l):
        return 0
    if (arr[l] == 0):
        return float('inf')
    min = float('inf')
    for i in range(l + 1, h + 1):
        if (i < l + arr[l] + 1):
            jumps = minJumps(arr, i, h)
            if (jumps != float('inf') and
                       jumps + 1 < min):
                min = jumps + 1
    return min
        
arr = []
n = int(input()) 
for i in range(n):
    arr.append(int(input()))
print('Minimum number of jumps to reach','end is', minJumps(arr, 0, n-1))
 
```
## Output:

![image](https://github.com/user-attachments/assets/ce041851-6707-4d03-97e9-b8ae64d914c4)

## Result:
Thus the program was executed successfully for finding the minimum number of jumps to reach end  of the array using naive method(recursion).
