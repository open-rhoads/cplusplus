# Dijkstra's Algorithm 
## Assignment Video
Here is my video explaining this assignment: https://youtu.be/sjsqefN__uU 

## Number 1 - Negative Weights
Explain with the help of an example "Why Dijkstra's algorithm fails on negative weights".
![image](https://github.com/user-attachments/assets/c03a13f3-878e-40a6-837b-ceaaa91fef10)

Dijkstra's Algorithm fails if there are negative weights essentially because it could choose to go one direction earlier on, but then if there was a negative weight further down along a different path that it didn't see, it's actually not efficient. In the above example, if we're looking for the shortest path from A to D, it would choose the 3 weight initially, not seeing the -9 later on.
