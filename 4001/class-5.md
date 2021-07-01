## Linked List 
A **data structure** that contains **nodes** each node(the individual links inside a linked list and it contains the data for the link) references the next Node in the list (by the proparity next). there are 2 typs: Singly and Doubly,
- for the **single** type it mean that the node refers for references one only.
- for the **Doubly**  the node refers for 2 references (Next and Previous).


we have also:
- Head: reference of type Node to the first node in a linked list.
- Current: a reference of type Node to the node that is currently.

### Traversal
When traversing a linked list, We depend on the Next value in each node to know where the next reference is pointing and allow us to extract the data. while loop check that the next is not refers to null if it dose
we will get a NullReferenceException the program will end.

## Adding a Node
the Pseudo code for an Add method on a Linked list:

```
ALGORITHM Add(newValue)
// INPUT <-- Value to add
// OUTPUT <-- No output

  newNode <-- NEW Node
  newNode.Value <-- newValue
  newNode.Next <-- Head
  Head <-- newNode

```

### Print Out Nodes

pseudo code for a method to print out all the nodes in a linked list:

```
ALGORITHM Print()
// INPUT <-- None
// OUTPUT <-- string to console

  Current <-- Head

  WHILE Current is not equal to NULL
    OUTPUT <-- "{Current.Value} --> "
    Current <-- Current.Next

  OUTPUT <-- "NULL"

```

## data structures

 which are the different ways that we can organize our data; variables, arrays, hashes, and objects are all types of data structures.
 

 
One characteristic of linked lists is that they are **linear data structures**, which means that there is a sequence and an order to how they are constructed and traversed. threr is also data **non-linear data structures**, items don’t have to be arranged in order, which means that we could traverse the data structure non-sequentially.


### Memory management

differentiator between **arrays** and linked lists is the way that they use memory when array is created, it needs a certain amount of memory and it need to be in order one byte next to the another, all together, in one place.on the other hands **linked list** One byte could live somewhere, while the next byte could be stored in another place in memory altogether.


