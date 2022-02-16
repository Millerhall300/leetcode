<!--|This file generated by command(leetcode description); DO NOT EDIT.    |-->
<!--+----------------------------------------------------------------------+-->
<!--|@author    awesee <openset.wang@gmail.com>                           |-->
<!--|@link      https://github.com/awesee                                 |-->
<!--|@home      https://github.com/awesee/leetcode                        |-->
<!--+----------------------------------------------------------------------+-->

[< Previous](../check-if-a-parentheses-string-can-be-valid "Check if a Parentheses String Can Be Valid")
　　　　　　　　　　　　　　　　
[Next >](../build-the-equation "Build the Equation")

## [2117. Abbreviating the Product of a Range (Hard)](https://leetcode.com/problems/abbreviating-the-product-of-a-range "一个区间内所有数乘积的缩写")

<p>You are given two positive integers <code>left</code> and <code>right</code> with <code>left &lt;= right</code>. Calculate the <strong>product</strong> of all integers in the <strong>inclusive</strong> range <code>[left, right]</code>.</p>

<p>Since the product may be very large, you will <strong>abbreviate</strong> it following these steps:</p>

<ol>
	<li>Count all <strong>trailing</strong> zeros in the product and <strong>remove</strong> them. Let us denote this count as <code>C</code>.
	<ul>
		<li>For example, there are <code>3</code> trailing zeros in <code>1000</code>, and there are <code>0</code> trailing zeros in <code>546</code>.</li>
	</ul>
	</li>
	<li>Denote the remaining number of digits in the product as <code>d</code>. If <code>d &gt; 10</code>, then express the product as <code>&lt;pre&gt;...&lt;suf&gt;</code> where <code>&lt;pre&gt;</code> denotes the <strong>first</strong> <code>5</code> digits of the product, and <code>&lt;suf&gt;</code> denotes the <strong>last</strong> <code>5</code> digits of the product <strong>after</strong> removing all trailing zeros. If <code>d &lt;= 10</code>, we keep it unchanged.
	<ul>
		<li>For example, we express <code>1234567654321</code> as <code>12345...54321</code>, but <code>1234567</code> is represented as <code>1234567</code>.</li>
	</ul>
	</li>
	<li>Finally, represent the product as a <strong>string</strong> <code>&quot;&lt;pre&gt;...&lt;suf&gt;eC&quot;</code>.
	<ul>
		<li>For example, <code>12345678987600000</code> will be represented as <code>&quot;12345...89876e5&quot;</code>.</li>
	</ul>
	</li>
</ol>

<p>Return <em>a string denoting the <strong>abbreviated product</strong> of all integers in the <strong>inclusive</strong> range</em> <code>[left, right]</code>.</p>

<p>&nbsp;</p>
<p><strong>Example 1:</strong></p>

<pre>
<strong>Input:</strong> left = 1, right = 4
<strong>Output:</strong> &quot;24e0&quot;
<strong>Explanation:</strong> The product is 1 &times; 2 &times; 3 &times; 4 = 24.
There are no trailing zeros, so 24 remains the same. The abbreviation will end with &quot;e0&quot;.
Since the number of digits is 2, which is less than 10, we do not have to abbreviate it further.
Thus, the final representation is &quot;24e0&quot;.
</pre>

<p><strong>Example 2:</strong></p>

<pre>
<strong>Input:</strong> left = 2, right = 11
<strong>Output:</strong> &quot;399168e2&quot;
<strong>Explanation:</strong> The product is 39916800.
There are 2 trailing zeros, which we remove to get 399168. The abbreviation will end with &quot;e2&quot;.
The number of digits after removing the trailing zeros is 6, so we do not abbreviate it further.
Hence, the abbreviated product is &quot;399168e2&quot;.
</pre>

<p><strong>Example 3:</strong></p>

<pre>
<strong>Input:</strong> left = 371, right = 375
<strong>Output:</strong> &quot;7219856259e3&quot;
<strong>Explanation:</strong> The product is 7219856259000.
</pre>

<p>&nbsp;</p>
<p><strong>Constraints:</strong></p>

<ul>
	<li><code>1 &lt;= left &lt;= right &lt;= 10<sup>4</sup></code></li>
</ul>

### Related Topics
  [[Math](../../tag/math/README.md)]

### Hints
<details>
<summary>Hint 1</summary>
Calculating the number of trailing zeros, the last five digits, and the first five digits can all be done separately.
</details>

<details>
<summary>Hint 2</summary>
Use a prime factorization property to find the number of trailing zeros. Use modulo to find the last 5 digits. Use a logarithm property to find the first 5 digits.
</details>

<details>
<summary>Hint 3</summary>
The number of trailing zeros C is nothing but the number of times the product is completely divisible by 10. Since 2 and 5 are the only prime factors of 10,  C will be equal to the minimum number of times 2 or 5 appear in the prime factorization of the product.
</details>

<details>
<summary>Hint 4</summary>
Iterate through the integers from left to right. For every integer, keep dividing it by 2 as long as it is divisible by 2 and C occurrences of 2 haven't been removed in total. Repeat this process for 5. Finally, multiply the integer under modulo of 10^5 with the product obtained till now to obtain the last five digits.
</details>

<details>
<summary>Hint 5</summary>
The product P can be represented as P=10^(x+y) where x is the integral part and y is the fractional part of x+y. Using the property "if S = A * B, then log(S) = log(A) + log(B)", we can write x+y = log_10(P) = sum(log_10(i)) for each integer i in [left, right]. Once we obtain the sum, the first five digits can be represented as floor(10^(y+4)).
</details>