# EX 5C Kadane's Algorithm
## DATE:
## AIM:
To Create a python Program to find the maximum contiguous sub array using Dynamic Programming.

## Algorithm
1. Initialize maxi with the first element and k (unused here).
2. Iterate through the array starting from the second element.
3. Update the current element a[i] to be the maximum of itself or itself plus the previous element a[i-1].
4. Update maxi with the maximum value found so far between maxi and the current a[i].
5. Return maxi after iterating through all elements.  

## Program:
### Developed by: NARASIMHAN S
### Register Number: 212223230133 

```python
def maxSubArraySum(a,size):
    maxi=a[0]
    k=0
    for i in range(1,size):
        a[i]=max(a[i],a[i]+a[i-1])
        maxi=max(maxi,a[i])
    return maxi
    
n=int(input())  
a =[] #[-2, -3, 4, -1, -2, 1, 5, -3]
for i in range(n):
    a.append(int(input()))
print("Maximum contiguous sum is", maxSubArraySum(a,n))
```
## Output:

![image](https://github.com/user-attachments/assets/ac99f623-554e-4fbb-8795-f40d09592e0f)

## Result:
Thus the program was executed successfully for finding the maximum contiguous sum of subarray using Dynamic Programming.
