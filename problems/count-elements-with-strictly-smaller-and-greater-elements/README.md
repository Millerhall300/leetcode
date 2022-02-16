<!--|This file generated by command(leetcode description); DO NOT EDIT.    |-->
<!--+----------------------------------------------------------------------+-->
<!--|@author    awesee <openset.wang@gmail.com>                           |-->
<!--|@link      https://github.com/awesee                                 |-->
<!--|@home      https://github.com/awesee/leetcode                        |-->
<!--+----------------------------------------------------------------------+-->

[< Previous](../number-of-ways-to-divide-a-long-corridor "Number of Ways to Divide a Long Corridor")
　　　　　　　　　　　　　　　　
[Next >](../rearrange-array-elements-by-sign "Rearrange Array Elements by Sign")

## [2148. Count Elements With Strictly Smaller and Greater Elements  (Easy)](https://leetcode.com/problems/count-elements-with-strictly-smaller-and-greater-elements "元素计数")

<p>Given an integer array <code>nums</code>, return <em>the number of elements that have <strong>both</strong> a strictly smaller and a strictly greater element appear in </em><code>nums</code>.</p>

<p>&nbsp;</p>
<p><strong>Example 1:</strong></p>

<pre>
<strong>Input:</strong> nums = [11,7,2,15]
<strong>Output:</strong> 2
<strong>Explanation:</strong> The element 7 has the element 2 strictly smaller than it and the element 11 strictly greater than it.
Element 11 has element 7 strictly smaller than it and element 15 strictly greater than it.
In total there are 2 elements having both a strictly smaller and a strictly greater element appear in <code>nums</code>.
</pre>

<p><strong>Example 2:</strong></p>

<pre>
<strong>Input:</strong> nums = [-3,3,3,90]
<strong>Output:</strong> 2
<strong>Explanation:</strong> The element 3 has the element -3 strictly smaller than it and the element 90 strictly greater than it.
Since there are two elements with the value 3, in total there are 2 elements having both a strictly smaller and a strictly greater element appear in <code>nums</code>.
</pre>

<p>&nbsp;</p>
<p><strong>Constraints:</strong></p>

<ul>
	<li><code>1 &lt;= nums.length &lt;= 100</code></li>
	<li><code>-10<sup>5</sup> &lt;= nums[i] &lt;= 10<sup>5</sup></code></li>
</ul>

### Related Topics
  [[Array](../../tag/array/README.md)]
  [[Sorting](../../tag/sorting/README.md)]

### Hints
<details>
<summary>Hint 1</summary>
All the elements in the array should be counted except for the minimum and maximum elements.
</details>

<details>
<summary>Hint 2</summary>
If the array has n elements, the answer will be n - count(min(nums)) - count(max(nums))
</details>

<details>
<summary>Hint 3</summary>
This formula will not work in case the array has all the elements equal, why?
</details>