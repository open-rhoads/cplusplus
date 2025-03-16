# Stacks and Queues
## Assignment Video
Here is my video explaining this assignment:
## 1) Begin with an Initially empty stack S of size 6:					
![image](https://github.com/user-attachments/assets/34401fab-3f33-419d-b14d-f9a21e28bf93)

### a. PUSH(S,4)									
![image](https://github.com/user-attachments/assets/778656bd-15c5-4dc9-9b54-36dd698ec9ae)

### b. PUSH(S,1)
![image](https://github.com/user-attachments/assets/51c572a8-2b5d-412d-b12d-dd7008e6dc69)

### c. PUSH(S,3)
![image](https://github.com/user-attachments/assets/c27be270-5eb9-4939-9089-9df68857cd44)

### d. POP(S)			
![image](https://github.com/user-attachments/assets/0e1bf87c-908d-47c4-a06f-b53c1d047f23)

### e. PUSH(S,8)			
![image](https://github.com/user-attachments/assets/714bcad1-3bb2-4ae1-9790-470569b796bb)

### f. POP(S)		
![image](https://github.com/user-attachments/assets/289dc0f4-79a2-459c-8d50-dce16862f670)

## 2) Begin with an Initially empty queue of size 6:
![image](https://github.com/user-attachments/assets/e11d9282-af45-4ad4-874f-9af9b576f952)

### a. ENQUEUE(Q,4)									
![image](https://github.com/user-attachments/assets/7c0e695f-6358-4d65-be30-bf594be999b3)

### b. ENQUEUE(Q,1)	
![image](https://github.com/user-attachments/assets/03aca9df-3acb-455e-89fd-b29c4ace62b1)

### c. ENQUEUE(Q,3)	
![image](https://github.com/user-attachments/assets/0be42f4e-01a3-4d38-8450-093f1186e527)

### d. DEQUEUE(Q)	
![image](https://github.com/user-attachments/assets/fd973513-d1bd-451d-998b-75eb51e3b25a)

### e. ENQUEUE(Q,8)
![image](https://github.com/user-attachments/assets/51b86f11-d790-47e8-ae10-1e1768be1584)

### f.DEQUEUE(Q)
![image](https://github.com/user-attachments/assets/33c1b390-4184-4c2d-9c3a-21b368dcd940)


## 3) Rewrite ENQUEUE and DEQUEUE to detect underflow and overflow of a queue
### Underflow
Underflow occurs when the queue is already empty (meaning that Q.head == Q.tail == 1). We can account for this by checking for this condition and throwing an error with a message if it occurs. Otherwise, we dequeue:
```pseudocode
if Q.head == Q.tail 
  error "underflow"
else
  x = Q[Q.head]
  if Q.head == Q.length
      Q.head = 1
  else Q.head = Q.head + 1
  return x
```
### Overflow
Overflow occurs when the queue is already full (meaning that Q.head == Q.tail + 1). We can account for this by checking for this condition and throwing an error with a message if it occurs. Otherwise, we enqueue:
```pesudocode
if Q.head == Q.tail + 1 
  error "overflow"
else
  Q[Q.tail] = x
  if Q.tail == Q.length
      Q.tail = 1
  else Q.tail = Q.tail + 1
```
## 4) 
Because a deque (double-ended queue) allows insertion and deletion at both ends. We can write four O(1)-time procedures to insert elements into and delete elements from both ends of a deque implemented by an array:
### Pseudocode of PUSH_BACK(DQ,x) (same as Enqueue for Queue)
```
Q[Q.tail] = x // set value at tail equal to passed number
if Q.tail == Q.length // if the tail is equal to the length, set tail equal to 1 (first element)
    Q.tail = 1
else Q.tail = Q.tail + 1 / otherwise, increment the tail/moves up one (element added to the back)
```
### Pseudocode of PUSH_FRONT(DQ,x)
```
Q[Q.head] = x // set value at head equal to passed number
if Q.head == Q.length // if the head is equal to the length, set head equal to 1 (first element)
    Q.head = 1
else Q.head = Q.head - 1 // decrement head/moves back one (element added to the front)
```
### Pseudocode of POP_BACK(DQ)
```
x = Q[Q.tail] // store the tail value in variable
if Q.tail == Q.length // if the tail is equal to the length, set tail equal to 1 (first element)
    Q.tail = 1
else Q.tail = Q.tail - 1 // decrement tail/moves back one (back element removed from DQ)
return x // return the previous tail number
```
### Pseudocode of POP_FRONT(DQ) (Same as Dequeue for Queue)
```
x = Q[Q.head] // store the head value in variable
if Q.head == Q.length // if the head is equal to the length, set head equal to 1 (first element)
    Q.head = 1
else Q.head = Q.head + 1 // increment head/moves up one (front element removed from DQ)
return x // return the previous head number
```

