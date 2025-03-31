# Binary Search Tree
This project demonstrates a simple Binary Search Tree.
## Assignment Video
Here is my video explaining this assignment: https://youtu.be/_lZlDOqtJrk 
## Number 1
If we have an empty binary search tree and insert the following sequence of numbers in this order: [1, 5, 9, 2, 4, 10, 6, 3, 8], below is a diagram showing what the binary search tree would look like: 
![image](https://github.com/user-attachments/assets/9a10a1d2-928d-4f06-b64a-70fc23559574)

## Number 2
If a well-balanced binary search tree contains 1,000 values, then the maximum number of steps it could take to search for a value within it would be log(1000) = 3.
## Number 3 & 4
```c++
//  main.cpp
//  binary_search_tree

#include <iostream>
using namespace std;

// Define a node using structure
struct Node {
    int data; // member for the value
    Node* left; // a pointer member to a Node for the left side child
    Node* right; // a pointer member to the Node for the right side child
    
    Node(int value) { // Node constructor
        data = value; // set the value param equal to the data
        left = nullptr; // set both left and right Nodes equal to null pointers
        right = nullptr;
    }
};

// Function to find the greatest value (#3)
int findMax(Node* root) { // receives a pointer to the root Node
    if (root == nullptr) { // if it is a null pointer/empty
        cout << "The tree is empty." << endl; // display message and end
        return -1; // Return -1 if the tree is empty
    }
    Node* current = root; // define a 'current' Node and set it equal to the passed root
    while (current->right != nullptr) { // while the right member is not null (there is a larger value in the set)...
        current = current->right; // then set the current Node equal to the right member of the former current Node - traversing down the tree
    }
    return current->data; // return the data value when it is done
}

// Helper function to insert a new node (#4)
Node* insert(Node* root, int value) { // receives a pointer to the 'root' Node and a value ot insert
    if (root == nullptr) { // if the passed 'root' Node is null, create and return a new Node and pass the value - initial insert/creates new children when we fill the left/right members
        return new Node(value);
    }
    // otherwise, if it is not null, we will compare the value to the 'root' Node and fill either the right or left member with the value
    // we call this same function to do it and pass the applicable member as the 'root' and the value - this will create new children
    if (value < root->data) {
        root->left = insert(root->left, value);
    } else {
        root->right = insert(root->right, value);
    }
    return root;
}

int main() {
    // Create the Binary Search Tree using the array from #1
    int data[] = {1, 5, 9, 2, 4, 10, 6, 3, 8};
    Node* root = nullptr; // set the initial root Node to a null pointer
    // loop through the data set and reassign the root each time by calling the insert function and passing the values
    // this will create the applicable Nodes
    for (int value : data) {
        root = insert(root, value);
    }
    // Find and print the greatest value by calling findMax and passing the root
    int maxValue = findMax(root);
    cout << "The greatest value in the Binary Search Tree is: " << maxValue << endl;
}

```
