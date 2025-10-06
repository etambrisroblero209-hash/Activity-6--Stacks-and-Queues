# Activity-6--Stacks-and-Queues

Task 1: 
Step 1 
PUSH(S,4)
S.top becomes 1.
S[1] = 4

Stack: [4]
S.top = 1

Step 2 
PUSH(S,1)
S.top becomes 2.
S[2] = 1

Stack: [4, 1]
S.top = 2

Step 3 
PUSH(S,3)
S.top becomes 3.
S[3] = 3

Stack: [4, 1, 3]
S.top = 3

Step 4
POP(S)
Pop returns 3.
S.top becomes 2.

Stack: [4, 1]
S.top = 2

Step 5 
PUSH(S,8)
S.top becomes 3.
S[3] = 8

Stack: [4, 1, 8]
S.top = 3

Step 6
POP(S)
Pop returns 8.
S.top becomes 2.

Stack: [4, 1]
S.top = 2

Final State:
Index	1	2	3	4	5	6
Value	4	1				
S.top = 2

Task 2:
Step 1
Q: [4, -, -, -, -, -]  
head = 1  
tail = 1
Step 2
Q: [4, 1, -, -, -, -]  
head = 1  
tail = 2
Step 3
Q: [4, 1, 3, -, -, -]  
head = 1  
tail = 3
Step 4
Q: [-, 1, 3, -, -, -]  
head = 2  
tail = 3
Step 5
Q: [-, 1, 3, 8, -, -]  
head = 2  
tail = 4
Step 6
Q: [-, -, 3, 8, -, -]  
head = 3  
tail = 4
Final
Q = [ -, -, 3, 8, -, - ]  
head = 3  
tail = 4

Task 3: To prevent underflow in DEQUEUE, you must check if the queue is empty: Q.head==Q.tail. If true, signal an error. To prevent overflow in ENQUEUE, you must check if the queue is full: calculate the next tail position, and if it equals Q.head, signal an error, as the circular buffer is full.

Task 4: All four O(1)-time deque operations rely on two pointers, D.head (front) and D.tail (back insertion point), managed with circular array logic to prevent element shifting. INSERT_FRONT checks for overflow, moves D.head backward circularly, and inserts the element. DELETE_FRONT checks for underflow, retrieves the element at D[D.head], and moves D.head forward circularly. INSERT_BACK checks for overflow, inserts the element at D[D.tail], and moves D.tail forward circularly. DELETE_BACK checks for underflow, moves D.tail backward circularly to the last element's index, retrieves that element, and returns it.

Video: https://youtu.be/SoBj1Z5_EcI
