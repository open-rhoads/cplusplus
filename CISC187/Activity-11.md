# Recursion
The following are exercises demonstrating how recursion works.
## Assignment Video
Here is my video explaining this assignment: 
## Number 1
The following function prints every other number from a low number to a high number. **Identify the base case in the function**:
```python
def print_every_other(low, high) 
    return if low > high
    puts low
    print_every_other(low + 2, high)
end
```
**The base case occurs when the low number is greater than the high number**; as this is when the function will return/end: 
```python
return if low > high
```
## Number 2
My kid was playing with my computer and changed my factorial function so that it computes factorial based on (n - 2) instead of (n - 1). Predict what will happen when we run factorial(10) using this function:
```python
def factorial(n)
    return 1 if n == 1
    return n * factorial(n - 2)
end
```
This error makes it so that the base case will never occur; because when we start with 10 for the value of n and the recursive function is calling itself and subtracting 2 from n each time, it will skip over 1 and go to 0. Therefore, the line ```return 1 if n == 1``` never occurs and it will be an infinite loop.
## Number 3
The following function accepts two numbers called low and high and returns the sum of all the numbers from low to high. However, our code is missing the base case, and will run indefinitely! Fix the code by adding the correct base case:
```python
def sum(low, high)
    return high + sum(low, high - 1)
end
```
## Number 4
Below is an array containing both numbers as well as other arrays, which in turn contain numbers and arrays. Write a recursive function that prints all the numbers (and just numbers).
```c++
array=[ 1, 
        2, 
        3,
        [4, 5, 6],
        7,
        [8,
          [9, 10, 11,
            [12, 13, 14]
          ] 
        ],
        [15, 16, 17, 18, 19,
          [20, 21, 22,
            [23, 24, 25,
              [26, 27, 29]
            ], 30, 31 
          ], 32
        ], 33 
      ]
```
