# Class Ten

## Stacks and Queues

Stack - 
  - A stack is a data structure that consists of Nodes. Each Node references the next Node in the stack, but does not reference its previous.

Common Terminology for a stack is;
1. Push 
  - Nodes or items that are put into the stack are pushed
1. Pop 
  - Nodes or items that are removed from the stack are popped. When you attempt to pop an empty stack an exception will be raised.
1. Top 
  - This is the top of the stack.
1. Peek 
  - When you peek you will view the value of the top Node in the stack. When you attempt to peek an empty stack an exception will be raised.
1. IsEmpty 
  - returns true when stack is empty otherwise returns false.

Stacks follow these concepts:

- FILO
  - First In Last Out

  - This means that the first item added in the stack will be the last item popped out of the stack.

- LIFO
  - Last In First Out

  - This means that the last item added to the stack will be the first item popped out of the stack.

- Push O(1)
  - Pushing a Node onto a stack will always be an O(1) operation. This is because it takes the same amount of time no matter how many Nodes (n) you have in the stack.

- Pop O(1)
  - Popping a Node off a stack is the action of removing a Node from the top. When conducting a pop, the top Node will be re-assigned to the Node that lives below and the top Node is returned to the user.

- Peek O(1)
  - When conducting a peek, you will only be inspecting the top Node of the stack.

  - Typically, you would check isEmpty before conducting a peek. This will ensure that an exception is not raised. Alternately, you can wrap the call in a try/catch block.


- Common terminology for a queue is

1. Enqueue 
  -  Nodes or items that are added to the queue.
1. Dequeue 
  - Nodes or items that are removed from the queue. If called when the queue is empty an exception will be raised.
1. Front 
  - This is the front/first Node of the queue.
1. Rear 
  - This is the rear/last Node of the queue.
1. Peek   
  - When you peek you will view the value of the front Node in the queue. If called when the queue is empty an exception will be raised.
1. IsEmpty 
  - returns true when queue is empty otherwise returns false.

- Queues follow these concepts:

- FIFO
  - First In First Out

  - This means that the first item in the queue will be the first item out of the queue.

- LILO
  - Last In Last Out

  - This means that the last item in the queue will be the last item out of the queue.

- Enqueue O(1)
  - When you add an item to a queue, you use the enqueue action. This is done with an O(1) operation in time because it does not matter how many other items live in the queue (n); it takes the same amount of time to perform the operation.

- Dequeue O(1)
  - When you remove an item from a queue, you use the dequeue action. This is done with an O(1) operation in time because it doesn’t matter how many other items are in the queue, you are always just removing the front Node of the queue.

- Peek O(1)
  - When conducting a peek, you will only be inspecting the front Node of the queue.

  - Typically, you want to check isEmpty before conducting a peek. This will ensure that an exception is not raised. Alternately, you can wrap the call in a try/catch block.








