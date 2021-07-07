## Stacks and Queues

### What is a Stack?

stack is a **data structure** that **consists of Nodes**. Each Node references the next Node in the stack, but does not reference its previous.

### The common terminology for a stack is:

1- Push - push Nodes into the stack 
2- Pop - removed Node from the stack are popped.
3- Top - This is the top of the stack.
4- Peek - view the value of the top Node in the stack.
5- IsEmpty - returns true when stack is empty otherwise returns false.

### Stacks follow concepts:

- **FILO:** (First In Last Out) the first added node popped the last node out of stack
- **LIFO:** (last in first out) the last added nod popped the first thing out of the stack


### Pushing O(1): 

When adding a Node, you push it into the stack by assigning it as the new top, with its next property equal to the original top.


1- add the the Node.
2- assign the next property of added Node to reference the same Node that was in the top is referencing
3- re-assign our reference top to the newly added Node


### Pop O(1):

the top Node will be re-assigned to the Node that lives below and the top Node is returned to the user. you would check isEmpty before conducting a pop

1- to remove Node from the stack first we have to create a reference named temp that points to the same Node that top points to.

2- Once you have created the new reference type, you now need to re-assign top to the value that the next property is referencing. In our visual, we can see that the next property is pointing to Node 4. We will re-assign top to be Node 4.

3- We can now remove Node 5 safely without it affecting the rest of the stack. Before we do that though you may want to make sure that you clear out the next property in your current temp reference. This will ensure that no further references to Node 4 are floating around the heap. This will allow our garbage collector to cleanly and safely dispose of the Nodes correctly.

4- Finally, we return the value of the temp Node that was just popped off.


### Peek O(1):

When conducting a peek, you will only be inspecting the top Node of the stack. you would check isEmpty before conducting a peek.

## What is a Queue?



Enqueue - Nodes or items that are added to the queue.
Dequeue - Nodes or items that are removed from the queue. If called when the queue is empty an exception will be raised.
Front - This is the front/first Node of the queue.
Rear - This is the rear/last Node of the queue.
Peek - When you peek you will view the value of the front Node in the queue. If called when the queue is empty an exception will be raised.
IsEmpty - returns true when queue is empty otherwise returns false.

###  Queue concepts:
- **FIFO** (First In First Out) This means that the first item in the queue will be the first item out of the queue.

- **LILO** (Last In Last Out) This means that the last item in the queue will be the last item out of the queue.


### Enqueue O(1)

1- change the next value to be the value of the adding node 
2- change the rear to point on the added node

### Dequeue O(1)

1- add a temp pointer to point on the front
2- re-assign front to the next value that the Node front is referencing
3- re-assign the next property on the temp Node to null

