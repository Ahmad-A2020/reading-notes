### Resources:
- [Linked Lists](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/singly_linked_list.html)
- [What’s a Linked List, Anyway pt1](https://medium.com/basecs/whats-a-linked-list-anyway-part-1-d8b7e6508b9d)
- [What’s a Linked List, Anyway pt2](https://medium.com/basecs/whats-a-linked-list-anyway-part-2-131d96f71996)

### Linked Lists:
- A Linked List is a sequence of Nodes that are connected/linked to each other.
- There are two types of Linked List - Singly and Doubly.  A Singly linked list means that there is only one reference, while  A Doubly linked list means that there is a reference to both the Next and Previous node.
-When traversing a linked list, you are not able to use a foreach or for loop; the best way to approach a traversal is through the use of a while() loop.A-
- in short to add item at the begining of the linked list, we doing the following steps:
     -Allocate memory for new node
     - Store data
     - Change next of new node to point to head
     - Change head to point to recently created no.
- to add it at the middle we doing the following:
     - Insert at the Middle
      - Allocate memory and store data for new node
     -  Traverse to node just before the required position of new node
     -  Change next pointers to include new node in between

### What’s a Linked List, Anyway pt1:
- a linked list is a linear collection of data elements whose order is not given by their physical placement in memory. Instead, each element points to the next.
-  arrays and linked lists as being similar in the way that we sequence data.
-The biggest differentiator between arrays and linked lists is the way that they use memory in our machines.When an array is created, it needs a certain amount of memory, and we’d need all of that memory in one contiguous block, but  for a linked list , it doesn’t need a memory all in one place
- in other word, The fundamental difference between arrays and linked lists is that arrays are static data structures, while linked lists are dynamic data structures.
- A static data structure needs all of its resources to be allocated when the structure is created;while a dynamic data structure can shrink and grow in memory
- A linked list is made up of a series of nodes, which are the elements of the list. The starting point of the list is a reference to the first node, which is referred to as the head.
- there are different  types of linked lists including:
     -Singly linked lists are the simplest type of linked list, based solely on the fact that they only go in one direction..
     - doubly linked list, because there are two references contained within each node: a reference to the next node, as well as the previous node.
     - A circular linked list is a little odd in that it doesn’t end with a node pointing to a null value. Instead, it has a node that acts as the tail of the list (rather than the conventional head node), and the node after the tail node is the beginning of the list.

### What’s a Linked List, Anyway pt2:
- Big O Notation is a way of evaluating the performance of an algorithm.
- There are two major points to consider when thinking about how an algorithm performs: how much time it requires at runtime given how much time and memory it needs.
- An O(1) function takes constant time,and an O(n) function is linear, which means that as our input grows
there are problem in openning this resource "can't reach"
- Inserting an element at the beginning of a linked list is particularly nice and efficient because it takes the same amount of time, no matter how long our list is.
-