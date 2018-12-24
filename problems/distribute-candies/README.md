<!--|This file generated by command(leetcode description); DO NOT EDIT.    |-->
<!--+----------------------------------------------------------------------+-->
<!--|@author    Openset <openset.wang@gmail.com>                           |-->
<!--|@link      https://github.com/openset                                 |-->
<!--|@home      https://github.com/openset/leetcode                        |-->
<!--+----------------------------------------------------------------------+-->

## 575. Distribute Candies (Easy)

Given an integer array with <b>even</b> length, where different numbers in this array represent different <b>kinds</b> of candies. Each number means one candy of the corresponding kind. You need to distribute these candies <b>equally</b> in number to brother and sister. Return the maximum number of <b>kinds</b> of candies the sister could gain. 

<p><b>Example 1:</b><br />
<pre>
<b>Input:</b> candies = [1,1,2,2,3,3]
<b>Output:</b> 3
<b>Explanation:</b>
There are three different kinds of candies (1, 2 and 3), and two candies for each kind.
Optimal distribution: The sister has candies [1,2,3] and the brother has candies [1,2,3], too. 
The sister has three different kinds of candies. 
</pre>
</p>

<p><b>Example 2:</b><br />
<pre>
<b>Input:</b> candies = [1,1,2,3]
<b>Output:</b> 2
<b>Explanation:</b> For example, the sister has candies [2,3] and the brother has candies [1,1]. 
The sister has two different kinds of candies, the brother has only one kind of candies. 
</pre>
</p>

<p><b>Note:</b>
<ol>
<li>The length of the given array is in range [2, 10,000], and will be even.</li>
<li>The number in given array is in range [-100,000, 100,000].</li>
<ol>
</p>

### Related Topics
[[Hash Table](https://github.com/openset/leetcode/tree/master/tag/hash-table/README.md)] 
### Hints
  1. To maximize the number of kinds of candies, we should try to distribute candies such that sister will gain all kinds.
  1. What is the upper limit of the number of kinds of candies sister will gain? Remember candies are to distributed equally.
  1. Which data structure is the most suitable for finding the number of kinds of candies?
  1. Will hashset solves the problem? Inserting all candies kind in the hashset and then checking its size with upper limit.