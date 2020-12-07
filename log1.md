# Johongir

## 100 Days of Code

### Day 1: Dec 4, 2020

#### Introduction
So actually I've started 600 days of code challenge for about 2 weeks and I'm also starting to keep journal of my progress each day. I'm going to write about what new I've learned today and what were the challenges that i could solve. So hopefully this challenge keeps me accounted for the upcoming NOWS. So let's rock it

#### What I've learned so far
So i've learned algorithms, memory, and nowdays I'm learning data structures and today i've learned about singly linked lists


### Day 2: Dec 5, 2020

#### Things I've learned
Today I've learned about Doubly Linked List Which data structure that consists of Nodes And Each node in the list connected with each other via pointers(links, references) unlike Singly Linked List, nodes in DLL has knows address of both node next to it and node before it.

#### Advantages of DLL over SLL
While removing last node is O(n) in DLL it is constant because of nodes in DLL has previous and next pointers but in SLL has only next pointer which points node after it, so you can just make second to last node tail which is constant time O(1)

You can loop through both forward and backwards in DLL but in only left to right 

#### Disadvantages of DLL over SLL
As nodes in DLL use two pointers and data while in SLL only uses data and a single pointer, that's why DLL require more memory than SLL

#### Resource
I've been learning Algorithms and Data Structures Which is the course of Colt Steele. And I'm very satisfied with his course for it contains not only theortical explanations of topics but also practical exercies


#### Day 3: Dec 6, 2020

#### Things I've Learned
 * Stacks and Queues
 * Trees/Binary Trees/Binary Search Trees
 
 
#### Stacks
Stack is FILO(first-in-last-out) and LIFO(last-in-first-out) data structure. It stores called functions and it has finite storage when functions keep being called error is thrown "Maximum Call stack size exceeded"

##### How functions are stored and removed
When functions is called, we say it is pushed into stack it is stored in call-stack and when program executed all codes till curly brace of function or it encounters return keyword it is removed or popped from the call-stack

##### Stacks Analogy
Imagine you keep stacking up plates on top of another and when you need to clean them, you start by removing the plate at the very top which was put last so the plate first put in the stack will be removed last

##### Real World use cases
For storing invoked functions
undo/redo in photoshop 

##### How to implement it with code
You have two options to do it 
1. By using array you can simulate stack but it is very inefficient with unshift and shift as all items has to be reindexed when one of these methods used, use push and pop instead
2. SLL or DLL SLL is very efficient enough to implement stack.

##### Big O of stacks with SLL/DLL 
Adding and Removing O(1)
Searching and Accessing O(n)


#### Queues
Queues are FIFO(first-in-first-out) and LILO(last-in-last-out) data structure

##### How to implement it with code
You can implement it with array or SLL/DLL
1. Implementing queues with array is very inefficient with arrays as you have to use combination of push and shift or unshift and pop both of which cause all items being reindexed. Imagine working with millions of sets of data.
2. Use SLL/DLL

##### Big O of Queues with SLL/DLL
Adding and Removing O(1)
Accessing and Searching O(n)


### Day 4: Dec 7, 2020

#### Things I've learned today
   * Tree Traversal
   * Breadth First Search
   * Depth First Search (Pre-Order; Post-Order; In-Order)
   
   
##### Tree Traversal
Traversing Tree is process of visiting (checking and or updating) each node exactly once in the tree data structures

##### Breadth First Search
Breadth First Search  searches nodes on the same level and it uses queue(array/sll/dll) to enqueue them and after it visited them, itdequeue them

##### Depth First Search
Depth First Search searches nodes vertically and it has 3 algorithms on its own to visit nodes on the specific order

##### Pre-Order and for What it is used for
In Pre-Order algorithm first root(parent) node visited, then all left child nodes and all right child nodes: ROOT -> LEFT CHILD -> RIGHT CHILD
It is used to copy tree

##### Post-Order and for What it is used for
In Post-Order first left child node then right child node and then finally parent node visited: LEFT CHILD -> RIGHT CHILD -> ROOT 
It's used to delete tree as it first visits child nodes then parent node

##### In-Order
In In-Order first left child node and then its parent node then right child node visited: LEFT CHILD -> ROOT -> RIGHT CHILD
If we use In-Order in BSTS we will get sorted data





