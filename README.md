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

- looking up and element is O(1)
- dynamically creates a array with some fixed size 
- and if we need to add more data than the existing size, then it creates a new array in some memory localtion and copies over the entire array and adds the new element there.
- If you remove the item from list, then the list moves the remaining elements to fill up the space as the elements has to run sequential, and thus removing is O(n)
-  If you are removing the top element in a loop, then the operation is O(N square) **avoid it any cost**

### Linked List

![alt text](https://github.com/inianantony/c_sharp_collections/blob/master/linkedlist.png)



