# Linked List
The following is a simple Linked List implementation in C++.

## Assignment Video
Here is my video explaining this assignment: https://youtu.be/06NjkH7F0Pg 

```c++
//  main.cpp
//  linked_list

#include <iostream>
using namespace std;

// Define a node structure
struct Node {
    double data; // this member stores the data value
    Node* next; // this member is a pointer to another node
};

// Function to print the linked list
void printList(Node* n) { // accepts pointer to a Node
    while (n != nullptr) { // while the pointer is not a nullptr (empty list)
        cout << n->data << " "; // output the 'data' member
        n = n->next; // traverse to the next Node member
    }
    cout << endl;
}

// Function to add a node at the start
void push(Node** head, double newData) { // accepts double pointer to head and the new data
    Node* newNode = new Node(); // create a new Noder pointer
    newNode->data = newData; // assign the passed data to the data property
    newNode->next = *head; // assign the next property as a pointer to the current head
    *head = newNode; // make the head equal to the new Node
}

// Function to delete a node at the start
void deleteNode(Node** head) {
    if (*head == nullptr) return; // return/end if head is nullptr - no Nodes left
    Node* temp = *head; // assign the current head pointer in a temp variable
    *head = (*head)->next; // make the new head pointer equal to the current head pointer's next property (the second item in list)
    delete temp; // delete the old head/temporary variable to avoid memory issues
}

int main() {
    Node* head = nullptr; // set the head equal to nullptr originally

    // Add nodes at the start by calling the push function and passing the address of the head and the new value to add
    push(&head, 1.1);
    push(&head, 1.2);
    push(&head, 1.3);
    push(&head, 1.4);
    push(&head, 1.5);

    cout << "My initial Linked List: ";
    printList(head);

    // Delete nodes at the start by calling the deleteNode function and passing the address of the head
    deleteNode(&head);
    cout << "My Linked list after deleting 1 node: ";
    printList(head);

    deleteNode(&head);
    cout << "My Linked list after deleting another node: ";
    printList(head);
}
```
