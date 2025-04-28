# Dijkstra's Algorithm 
## Assignment Video
Here is my video explaining this assignment:

## Number 1 - Negative Weights
Explain with the help of an example "Why Dijkstra's algorithm fails on negative weights".
![image](https://github.com/user-attachments/assets/d8cdf88a-9459-4ed2-ba5e-5348e4fe8be5)

Dijkstra's Algorithm fails if there are negative weights essentially because it could choose to go one direction earlier on, but then if there was a negative weight further down along a different path that it didn't see, it's actually not efficient.
