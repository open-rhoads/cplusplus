# Graphs - Breadth-First & Depth-First Search (BFS & DFS)
The following is a simple Graph implementation with BFS & DFS algorithms in C++.

## Assignment Video
Here is my video explaining this assignment:

## Number 1 - Sample Graph


## Number 2 - Graph Implementation w/ BFS & DFS
```c++
#include <iostream>
#include <vector>
#include <queue>
#include <stack>

using namespace std;

// Graph class
class Graph {
public:
    // the adjacent_list data member is a vector of integer vectors
    vector<vector<int>> adjacent_list;
    // constructor accepts an integer of nodes, and calls the resize member function of the adjacent_list member vector, passing the # of nodes
    Graph(int nodes) {
        adjacent_list.resize(nodes);
    }
    // the connect member function accepts 2 int params and pushes back each number to the adjacent_list vector that corresponds to the other number (undirected graph)
    void connect(int u, int v) {
        adjacent_list[u].push_back(v);
        adjacent_list[v].push_back(u);
    }
    
    // the output_graph member function dual loops through the 2D vector and prints the list of adjacent nodes for each node in the graph
    void output_graph() {
        for (int i = 0; i < adjacent_list.size(); ++i) {
            cout << "Node " << i << ": ";
            for (int j : adjacent_list[i]) {
                cout << j << " ";
            }
            cout << endl;
        }
    }
};

// Breadth-First Search (BFS)
void BFS(Graph& graph, int start) { // accepts params of reference to graph and start int
    vector<bool> visited(graph.adjacent_list.size(), false); // creates a bool vector the same size as the primary level adjacent_list
    queue<int> q; // creates a queue of integers
    visited[start] = true; // sets the visited vector at the index corresponding to the start int to true
    q.push(start); // pushes the start number to the queue

    while (!q.empty()) { // while the queue is not empty - runs until there are no more adjacent numbers in the graph
        int node = q.front(); // grab the front number in the queue to examine it as a node and store in variable
        q.pop(); // pop the front value off
        cout << node << " "; // print the start value of the node being examined/just popped
        for (int neighbor : graph.adjacent_list[node]) { // loop through each number in the adjacent_list of the passed graph corresponding to the examined node
            if (!visited[neighbor]) { // if the neighbor number has not yet been visited/no value in the visited vector corresponding to the neighbor number
                visited[neighbor] = true; // set the bool corresponding to the neighbor number in the visited vector to true
                q.push(neighbor); // push neighbor number to the queue
            }
        }
    }
    cout << endl;
}

// Depth-First Search (DFS)
void DFS(Graph& graph, int start) { // accepts params of reference to graph and start int
    vector<bool> visited(graph.adjacent_list.size(), false); // creates a bool vector the same size as the primary level adjacent_list
    stack<int> s; // creates a stack of integers
    s.push(start); // pushes the start number to the stack

    while (!s.empty()) { // while the stack is not empty
        int node = s.top(); // grab the top number from the stack and store in variable
        s.pop(); // pop the top number from the stack

        if (!visited[node]) { // if the node has not yet been visited/no value in the visited vector corresponding to the node number
            visited[node] = true; // set the bool corresponding to the node number in the visited vector to true
            cout << node << " "; // print the node value
        }

        for (int neighbor : graph.adjacent_list[node]) { // loop through the adjacent_list values of the node number
            if (!visited[neighbor]) { // if the neighbor number has not been visited/no value in the visited vector corresponding to neighbor number
                s.push(neighbor); // push the neighbor number to the stack... now it will repeat with all the neighbors bc stack is not empty
            }
        }
    }
    cout << endl;
}

int main() {
    Graph graph(5); // create the empty graph
    // use the connect method add all the connections & build the graph
    graph.connect(0, 1);
    graph.connect(0, 2);
    graph.connect(1, 3);
    graph.connect(2, 3);
    graph.connect(2, 4);
    
    // output the graph
    cout << "Graph representation:" << endl;
    graph.output_graph();
    
    // display BFS
    cout << "BFS starting from node 0:" << endl;
    BFS(graph, 0);
    
    // display DFS
    cout << "DFS starting from node 0:" << endl;
    DFS(graph, 0);
}
```
## Number 3 - Big O Efficiency Comparison of BFS & DFS
Both algorithms process each Vertex(V) and Edge(E) once. Therefore, their time complexity is O(V+E). Both algorithms must store each Vertex(V) in a queue or stack. Therefore, their space requirement is O(V).
