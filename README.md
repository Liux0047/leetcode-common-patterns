# leetcode-common-patterns
Common patterns and useful techniques for LeetCode questions

### Stack
For Java, use ArrayDeque instead of the Stack class, [find out more](https://stackoverflow.com/a/12524949/2408445). 

#### Find boundary
* Find the index of first unsorted element: https://leetcode.com/articles/shortest-unsorted-continous-subarray/ (see the Stack solution)


### Arrays
* Finding duplicate / missing number from 1..n where n is the length of array, use element itself as index, and manipulate original array with by +/- n. In this way, the orignal element can be retrieved with x % n, and number of times visited is x / n. 
  * https://leetcode.com/problems/first-missing-positive/discuss/17080/Python-O(1)-space-O(n)-time-solution-with-explanation
  * https://leetcode.com/problems/find-all-numbers-disappeared-in-an-array/
  * https://leetcode.com/problems/find-all-duplicates-in-an-array/

* In Java, `Arrays.sort(Object[])` and `Collections.sort(List<T>)` are guaranteed to be stable. This can be useful to preserve original ordering if partial sorting is required: 
  * https://leetcode.com/problems/reorder-data-in-log-files/

### Two heaps
Usually for finding median in data stream. Use a max and min heap to keep left and right half. Always adding new element to one half and poll from it to avoid deciding which half to add:
* https://leetcode.com/problems/find-median-from-data-stream/
* https://leetcode.com/problems/sliding-window-median/


### Fast & slow pointer
* Useful when you need to maintain certain distance between linked list nodes: https://leetcode.com/problems/remove-nth-node-from-end-of-list/
* Cycle detection with fast/slow pointer: https://leetcode.com/problems/linked-list-cycle/solution/
* Find the middle of linked list with fast/slower pointer, when fast runs to the end, slow is in the middle: https://leetcode.com/problems/middle-of-the-linked-list/solution/
