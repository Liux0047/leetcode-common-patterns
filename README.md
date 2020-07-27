# leetcode-common-patterns
Common patterns and useful techniques for LeetCode questions

### Stack
For Java, use ArrayDeque instead of the Stack class, [find out more](https://stackoverflow.com/a/12524949/2408445). 

##### Find boundary
* Find the index of first unsorted element: https://leetcode.com/articles/shortest-unsorted-continous-subarray/ (see the Stack solution)


### Arrays
* finding duplicate / missing number from 1..n where n is the length of array, use element itself as index, and manipulate original array with by +/- n. In this way, the orignal element can be retrieved with x % n, and number of times visited is x / n. 
  * https://leetcode.com/problems/first-missing-positive/discuss/17080/Python-O(1)-space-O(n)-time-solution-with-explanation
  * https://leetcode.com/problems/find-all-numbers-disappeared-in-an-array/
  * https://leetcode.com/problems/find-all-duplicates-in-an-array/
