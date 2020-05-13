# VIDEO SCRIPT
## Slide 1 
The doubly linked-list is a well node data structure where the data are stored in a list of nodes **(click)** each one pointing, not only to the next one, **(click)** but also to the previous one. **(click)** On both ends, we have what we call anchors which are fixed to the left, an the right.

## Slide 3

When we want to add a node to the list, we make it point to its neighbors and then, change the pointers accordingly.

## Slide 8

But now, if multiple threads want to make modify the list, we need to make it thread safe.

## Slide 9
Most of the algorithms, lock-free or not, use the same ACQUIRE, APPLY and RELEASE phases. If during the acquire phase, a process needs a lock owned by another process, it waits for it to release it and it thus creates an hold-and-wait chain

## Slide 10 
In the Built-in Coloring for Highly Concurrent Doubly-Linked Lists paper, the authors came up with an innovative algorithm allowing us to reduce the size of the hold-and-wait chain.

## Slide 11 
This algorithm is called CAS-Chromo and is completely lock-free. As its name says, it uses Compare and Swap operations to make changes atomically.

## Slide 12
The idea is that each node of the list will have a color different to the one of its neighbors in addition to a reference to the operation that is using it.

## Slide 13
Talking about operations, those have a state, a subject node which is the one it has to add or remove and a source node which is adjacent to it.

The Memento contains a copy of the nodes before 
