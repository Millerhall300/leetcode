## 719. Find K-th Smallest Pair Distance (Hard)

<p>Given an integer array, return the k-th smallest <b>distance</b> among all the pairs. The distance of a pair (A, B) is defined as the absolute difference between A and B. </p>

<p><b>Example 1:</b><br />
<pre>
<b>Input:</b>
nums = [1,3,1]
k = 1
<b>Output: 0</b> 
<b>Explanation:</b>
Here are all the pairs:
(1,3) -> 2
(1,1) -> 0
(3,1) -> 2
Then the 1st smallest distance pair is (1,1), and its distance is 0.
</pre>
</p>

<p><b>Note:</b><br>
<ol>
<li><code>2 <= len(nums) <= 10000</code>.</li>
<li><code>0 <= nums[i] < 1000000</code>.</li>
<li><code>1 <= k <= len(nums) * (len(nums) - 1) / 2</code>.</li>
</ol>
</p>

### Similar Questions
  1. [Find K Pairs with Smallest Sums](https://github.com/openset/leetcode/tree/master/solution/find-k-pairs-with-smallest-sums) (Medium)
  1. [Kth Smallest Element in a Sorted Matrix](https://github.com/openset/leetcode/tree/master/solution/kth-smallest-element-in-a-sorted-matrix) (Medium)
  1. [Find K Closest Elements](https://github.com/openset/leetcode/tree/master/solution/find-k-closest-elements) (Medium)
  1. [Kth Smallest Number in Multiplication Table](https://github.com/openset/leetcode/tree/master/solution/kth-smallest-number-in-multiplication-table) (Hard)
  1. [K-th Smallest Prime Fraction](https://github.com/openset/leetcode/tree/master/solution/k-th-smallest-prime-fraction) (Hard)