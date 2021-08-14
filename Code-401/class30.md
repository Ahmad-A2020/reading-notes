### Implementation: Hash Tables

####  Recourses:
- [Read Intro to Hash Tables](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-30/resources/Hashtables.html)
- [Watch what is a hash table?](https://www.youtube.com/watch?v=MfhjkfocRR0)
- [Read basics of hash tables](https://www.hackerearth.com/practice/data-structures/hash-tables/basics-of-hash-tables/tutorial/)
- [Skim hash table wiki](https://en.wikipedia.org/wiki/Hash_table)

### Definitions:
- **hash table:** a hash table (hash map) is a data structure that implements an associative array abstract data type, a structure that can map keys to values.
- **Hash :**  A hash is the result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose.
- **Buckets:** A bucket is what is contained in each index of the array of the hashtable.
- **Collisions:** A collision is what happens when more than one key gets hashed to the same location of the hashtable.


### Explaination
hash is the ability to encode the key that will eventually map to a specific location in the data structure that we can look at directly to retrieve the value. Since we are able to hash our key and determine the exact location where our value is stored, we can do a lookup in an O(1) time complexity.
### Structure
- Creating a Hash:  A hashtable traditionally is created from an array. the key is converted to index using some sort of logic to turn that “key” into a numeric number value. Here is a possible suggestion:

         -  Add or multiply all the ASCII values together.
         -  Multiply it by a prime number such as 599.
         - Use modulo to get the remainder of the result, when divided by the total size of the array.
         -  Insert into the array at that index.

- Collisions: A collision occurs when more than one key hashes to the same index in an array. Collisions are solved by changing the initial state of the buckets. Instead of starting them all as null we can initialize a LinkedList in each one! Now if two keys resolve to the same index in the array then their key/value pairs can be stored as a node in a linked list. Each index in the array is called a “bucket” because it can store multiple key/value pairs.
