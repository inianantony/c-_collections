# c#_collections
repo to explain the concepts of C# collections

### Array's

- Fixed Size
- and Continuous block in memory
- thats why we cant dynamically add data
- Thats why looking up in array by index is O(1) operation
  - So from the 1st element, get the ints size
  - 4 * size of int, and then it knows exactly where to go and fetch in memory
  

### List

- dynamically creates a array with some fixed size 
- and if we need to add more data than the existing size, then it creates a new array in some memory localtion and copies over the entire array and adds the new element there.

