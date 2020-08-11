# Class Five

## Linked Lists

### Below are definitions that will be able to help you learn linked lists. 

1. linked List 
  - is a sequence of Nodes that are connected/linked to each other

1. singly 
  - Singly refers to the number of references the node has. A Singly linked list means that there is only one reference, and the reference points to the Next node in a linked list.

1. doubly 
  - Doubly refers to there being two (double) references within the node. A Doubly linked list means that there is a reference to both the Next and Previous node.

1. node 
  - Nodes are the individual items/links that live in a linked list. Each node contains the data for each link.

1. next 
  - Each node contains a property called Next. This property contains the reference to the next node.

1. head 
  - The Head is a reference type of type Node to the first node in a linked list.

1. current - The Current reference is a reference type of type Node that is currently being looked at. This node is traditionally used when traversing through a full linked list. When traversing, you typically reset the current to the head to guarantee you are starting from the beginning of the linked list.

1. linear data structures 
  - there is a sequence and an order to how they are constructed and traversed.

1. non-linear data structures 
  - items don’t have to be arranged in order, which means that we could traverse the data structure non-sequentially.

1. static data structures 
  - needs all of its resources to be allocated when the structure is created; this means that even if the structure was to grow or shrink in size and elements were to be added or removed, it still always needs a given size and amount of memory

1. dynamic data structures 
  - can shrink and grow in memory. It doesn’t need a set amount of memory to be allocated in order to exist, and its size and shape can change, and the amount of memory it needs can change as well.

1. null - the end of the list, an empty value

1. data - the information that the node contains

1. big O Notation - is a way of evaluating the performance of an algorithm.  There are two major points to consider when thinking about how an algorithm performs: how much time it requires at runtime given how much time and memory it needs.

1. O(1) function 
  - takes constant time, which is to say that it doesn’t matter how many elements we have, or how huge our input is: it’ll always take the same amount of time and memory to run our algorithm

1. An O(n) function 
  - is linear, which means that as our input grows the space and time that we need to run that algorithm grows linearly.

### Singly linked list visual 

- a - b - c - d - null

  - information passes from one node to the next node, by one link. Meaning the node only has a reference to the next node.  
  
  - ie a only references b, c only reference b, so forth and so on. 

### Doubly linked list visual

- a = b = c = d = null

  - information passes from one node to the next by two links.  This means the nodes have a reference to the node not only after them like the singly linked list, but also to the node before it. 

  - ie b reference both a and c.  c references both b and d.  so forth and so on. 
