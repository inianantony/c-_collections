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
1. So to remove an item, say example Barbados, then change the 1st node's next to 3rd and change the 3rd nodes prev to 1st and remove all the linkages of the 2nd node, thus it will be garbage collected.
2. Apply the vice versa principle to add
3. So we can conclude that Add and Remove in linked list is O(1) operation.
4. However to look up an element in linked list it needs to iterate the whole list and this its a O(n) operation

### Takeaway
1. List and Array is optimized for reading data on the exact index O(1)
2. Linked list is optimized for adding and removing O(1)
3. Enumating LinkedList, List, Array are O(n) operations

### Sets

1. Another datastructure offered from microsoft
2. HashSet, SortedSet
3. Its an unordered bag of objects
4. Incontract with dictionary which lookup data by key , HashSet enumerate by value
5. When adding diplicate key in dictionary throws error, but in HashSet it silently ignores the duplicated data
6. Sets offer set operations like UnionWith, IntersectWith, ExceptWith


### ReadOnly vs Immutable

1. ReadlyOnly is just a wrapper on top of the underlying collection and comes from System.Collections.ObjectModel 
```C#
var list = new List<int>();
var readOnlyList = new ReadOnlyCollection<int>(list);
list.Add(1); // This line still chages the readonly collections data
```
2. Immutable holds the data inside and its completely immutable and its comes from System.Collections.Immutable



