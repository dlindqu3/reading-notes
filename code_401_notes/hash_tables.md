# Code 401 Reading Notes 
### Hash Tables

####  source: "Hashtables" [link](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-30/resources/Hashtables.html)
- hash: a value computed from an input string 
- bucket: what is contained in each index of a hash table; each index is a bucket
- collisions: multiple keys get hashed to the same location of a hash table 
- each node/bucket of a hash table has a key and a value 
- a hash code turns a key into an integer 
- a hashtable is typically made from an array

####  source: "What is a HashTable Data Structure - Introduction to Hash Tables , Part 0" [link](https://www.youtube.com/watch?v=MfhjkfocRR0)
- a hash function will tell which location in an array stores a given key 
- hash (paul)  returns index of paul in the array 
- if a value already exists at a given index, create a chain/link to new value
