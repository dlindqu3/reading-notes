# Code 401 Reading Notes 
### 05. Read: 05 -  Linked Lists  

####  source: "Big O: Analysis of Algorithm Efficiency" [link](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/big_oh.html)
  - describes the worst case for algorithm efficiency 
  - O(1)
  - O(logN) -- example: binary search 
  - O(N)
  - O(N^2) -- often caused by nested loops 
  - O(N^3) -- deeply nested loops 
  - O(2^N) -- example: compare one subset to all other possible subsets; common for factorial problems  

#### source: "Linked Lists" [link](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/singly_linked_list.html) 
  - a ll is a sequence of nodes, and each node references the next 
  - singly ll: each node only points to the next node 
  - doubly ll: reference to next and previous nodes 
  - node: the item that lives on a ll
  - head: reference to the first node 
  - current: node being looked at 
  - best way to approach traversal is with a while loop 
  - common ll problem: see if ll includes a given value 
