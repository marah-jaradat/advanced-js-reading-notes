# 14-March-2022- Ninth class reading notes:

## Stacks and Queues:

**What is a Stack**
A stack is a data structure that consists of Nodes. Each Node references the next Node in the stack, but does not reference its previous.

Push O(1)
Pushing a Node onto a stack will always be an O(1) operation. This is because it takes the same amount of time no matter how many Nodes (n) you have in the stack.

Pop O(1)
Popping a Node off a stack is the action of removing a Node from the top. When conducting a pop, the top Node will be re-assigned to the Node that lives below and the top Node is returned to the user.

Peek O(1)
When conducting a peek, you will only be inspecting the top Node of the stack.

IsEmpty O(1)

**What is a Queue**
Common terminology for a queue is

Enqueue - Nodes or items that are added to the queue.
Dequeue - Nodes or items that are removed from the queue. If called when the queue is empty an exception will be raised.
Front - This is the front/first Node of the queue.
Rear - This is the rear/last Node of the queue.
Peek - When you peek you will view the value of the front Node in the queue. If called when the queue is empty an exception will be raised.
IsEmpty - returns true when queue is empty otherwise returns false.

Enqueue O(1)
When you add an item to a queue, you use the enqueue action. This is done with an O(1) operation in time because it does not matter how many other items live in the queue (n); it takes the same amount of time to perform the operation.

**Difference between Stack and Queue Data Structures**
Stack A stack is a linear data structure in which elements can be inserted and deleted only from one side of the list, called the top. A stack follows the LIFO (Last In First Out) principle, i.e., the element inserted at the last is the first element to come out. The insertion of an element into stack is called push operation, and deletion of an element from the stack is called pop operation. In stack we always keep track of the last element present in the list with a pointer called top.

A queue is a linear data structure in which elements can be inserted only from one side of the list called rear, and the elements can be deleted only from the other side called the front. The queue data structure follows the FIFO (First In First Out) principle, i.e. the element inserted at first in the list, is the first element to be removed from the list. 

Stacks: Stack is collection of elements, that follows the LIFO order. LIFO stands for Last In First Out, which means element which is inserted most recently will be removed first. Imagine a stack of tray on the table. When you put a tray there you put it at top, and when you remove it, you also remove it from top.

**Similarities between stack and queue.**
There are two similarities between the stack and queue:

Linear data structure
Both the stack and queue are the linear data structure, which means that the elements are stored sequentially and accessed in a single run.
Flexible in size
Both the stack and queue are flexible in size, which means they can grow and shrink according to the requirements at the run-time.

**Types of Queues**
There are three common types of queues you can expect to encounter. So far, we learned about the Linear Queue. The other two queues are:

Circular Queue: In a circular queue, the last element is connected to the first element to form a circle. Initially, the front and rear parts of the queue point to the same location, but they move apart as more elements are inserted into the queue. A real-life example of a circular queue is an automated traffic signal system.

Priority Queue: In priority queues, elements are sorted based on priority. The most important element appears first, and the least important appears last. Priority queues are used in operating systems for load balancing to determine which programs should be given more priority.

**FIFO & LILO and LIFO & FILO Principles
**Queue: First In First Out (FIFO): The first object into a queue is the first object to leave the queue, used by a queue.

Stack: Last In First Out (LIFO): The last object into a stack is the first object to leave the stack, used by a stack

OR

Stack: Last In First Out (FILO): The First object or item in a stack is the last object or item to leave the stack.

Queue: Last In First Out (LILO): The last object or item in a queue is the last object or item to leave the queue.