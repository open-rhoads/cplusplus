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
This error makes it so that the base case will never occur; because when we start with 10 for the value of n and the recursive function is calling itself and subtracting 2 from n each time, it will skip over 1 and go to 0. Therefore, the line ```python return 1 if n == 1``` never occurs and it will be an infinite loop.
## Number 3
The following function accepts two numbers called low and high and returns the sum of all the numbers from low to high. However, our code is missing the base case, and will run indefinitely! Fix the code by adding the correct base case:
```python
def sum(low, high)
    return high + sum(low, high - 1)
end
```
This code needs to end on the iteration before the high number equaling the low numbe; because we don't want to add the low number twice. Therefore, you could solve this infinite loop by adding a conditional of wrapping the return statement in a while loop:
```c++ 
while (low != high) {
    return high + sum(low, high - 1);
}
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
```c++
#include <iostream>
#include <vector>

// Define a custom type to hold either an integer or a vector of itself
struct MultiDimArray {
    bool isInt; // Flag to indicate if the element is an integer
    int intValue; // Holds the integer value if isInt is true
    std::vector<MultiDimArray> vecValue; // Holds the vector if isInt is false

    // Constructor for integer type
    MultiDimArray(int value) : isInt(true), intValue(value) {}

    // Constructor for vector type
    MultiDimArray(std::vector<MultiDimArray> value) : isInt(false), vecValue(value) {}
};

void processArray(const MultiDimArray& array, int depth = 0) {
    // Print the current depth
    std::cout << "Depth: " << depth << std::endl;

    if (array.isInt) {
        // If it's an integer, process it (e.g., print it)
        std::cout << array.intValue << " ";
    } else {
        // If it's a vector, recursively process each element
        for (const auto& element : array.vecValue) {
            processArray(element, depth + 1);
        }
    }
    std::cout << std::endl;
}

int main() {
    // Example multi-dimensional array
    MultiDimArray array = MultiDimArray({
        MultiDimArray(1),
        MultiDimArray(2),
        MultiDimArray(3),
        MultiDimArray(std::vector<MultiDimArray>{MultiDimArray(4), MultiDimArray(5), MultiDimArray(6)}),
        MultiDimArray(7),
        MultiDimArray(std::vector<MultiDimArray>{
            MultiDimArray(8),
            MultiDimArray(std::vector<MultiDimArray>{
                MultiDimArray(9), MultiDimArray(10), MultiDimArray(11),
                MultiDimArray(std::vector<MultiDimArray>{MultiDimArray(12), MultiDimArray(13), MultiDimArray(14)})
            })
        }),
        MultiDimArray(std::vector<MultiDimArray>{
            MultiDimArray(15), MultiDimArray(16), MultiDimArray(17), MultiDimArray(18), MultiDimArray(19),
            MultiDimArray(std::vector<MultiDimArray>{
                MultiDimArray(20), MultiDimArray(21), MultiDimArray(22),
                MultiDimArray(std::vector<MultiDimArray>{
                    MultiDimArray(23), MultiDimArray(24), MultiDimArray(25),
                    MultiDimArray(std::vector<MultiDimArray>{MultiDimArray(26), MultiDimArray(27), MultiDimArray(29)})
                }), MultiDimArray(30), MultiDimArray(31)
            }), MultiDimArray(32)
        }), MultiDimArray(33)
    });

    // Process the array
    processArray(array);
}

```
