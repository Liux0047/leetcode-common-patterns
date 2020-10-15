# leetcode-common-patterns
Common patterns and useful techniques for LeetCode questions

### Stack
For Java, use ArrayDeque instead of the Stack class, [find out more](https://stackoverflow.com/a/12524949/2408445). 
* Find the index of first unsorted element: https://leetcode.com/articles/shortest-unsorted-continous-subarray/ (see the Stack solution)
* To flatten nested data structure, can use stack of iterators: https://leetcode.com/problems/flatten-nested-list-iterator/solution/


### Arrays
* Finding duplicate / missing number from 1..n where n is the length of array, use element itself as index, and manipulate original array with by +/- n. In this way, the orignal element can be retrieved with x % n, and number of times visited is x / n. 
  * https://leetcode.com/problems/first-missing-positive/discuss/17080/Python-O(1)-space-O(n)-time-solution-with-explanation
  * https://leetcode.com/problems/find-all-numbers-disappeared-in-an-array/
  * https://leetcode.com/problems/find-all-duplicates-in-an-array/

* In Java, `Arrays.sort(Object[])` and `Collections.sort(List<T>)` are guaranteed to be stable. This can be useful to preserve original ordering if partial sorting is required: 
  * https://leetcode.com/problems/reorder-data-in-log-files/

### Heap
For Java, the data strcuture is PriorityQueue; for Python see functions in heapq
* K smallest / largest elements from whatever: 
  * https://leetcode.com/problems/merge-k-sorted-lists/
  * https://leetcode.com/problems/find-k-pairs-with-smallest-sums/
  * https://leetcode.com/problems/kth-smallest-element-in-a-sorted-matrix/
* K-way merge: maintain a heap of size K; poll from the heap and replace with its next item from its array:
  * https://leetcode.com/problems/merge-k-sorted-lists/
  * https://leetcode.com/problems/smallest-range-covering-elements-from-k-lists/discuss/104893/Java-Code-using-PriorityQueue.-similar-to-merge-k-array
* Find max number of overlapping intervals at any point of time: https://leetcode.com/problems/meeting-rooms-ii/solution/

### Two heaps
Usually for finding median in data stream. Use a max and min heap to keep left and right half. Always add new element to one heap and poll from it to avoid deciding which heap to add:
* https://leetcode.com/problems/find-median-from-data-stream/
* https://leetcode.com/problems/sliding-window-median/


### Fast & slow pointer
* Useful when you need to maintain certain distance between linked list nodes: https://leetcode.com/problems/remove-nth-node-from-end-of-list/
* Cycle detection with fast/slow pointer: https://leetcode.com/problems/linked-list-cycle/solution/
* Find the middle of linked list with fast/slower pointer, when fast runs to the end, slow is in the middle: https://leetcode.com/problems/middle-of-the-linked-list/solution/

### Two pointers
* odd / even pointer in linked list: https://leetcode.com/problems/odd-even-linked-list/
* Dutch national flag problem: https://leetcode.com/problems/sort-colors/ ; use 3 pointers for each boundary between 0,1, unclassified, 2

### Bucket sort
* Priority Queue solutions should be sufficient for top k frequent element questions in the interview, but bukcet sort can make it even more efficient:
  * https://leetcode.com/problems/top-k-frequent-elements/discuss/81602/Java-O(n)-Solution-Bucket-Sort
  * https://leetcode.com/problems/sort-characters-by-frequency/solution/
  
### Union find
* https://leetcode.com/problems/number-of-connected-components-in-an-undirected-graph/discuss/896208/Java-Classic-Union-Find
