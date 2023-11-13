Find GCD of two numbers<br>
Problem Statement: Find the gcd of two numbers.

<pre>
  Example 1:
Input: num1 = 4, num2 = 8
Output: 4
Explanation: Since 4 is the greatest number which divides both num1 and num2.

Example 2:
Input: num1 = 3, num2 = 6
Output: 3
Explanation: Since 3 is the greatest number which divides both num1 and num2.
</pre>

<h3>Brute Force Approach</h3>
<pre>
  Solution 1: Brute force

Intuition: Simply traverse from 1 to min(a,b) and check for every number.

Approach: 

Traverse from 1 to min(a,b).
And check if i is divisible by both a and b.If yes store it in the answer.
Find the maximum value of i which divides both a and b.

if __name__ == '__main__':
    num1 = 4
    num2 = 8
    ans = 1
    for i in range(1, min(num1, num2) + 1):
        if num1 % i == 0 and num2 % i == 0:
            ans = i
    print("The GCD of the two numbers is", ans)


  Output: The GCD of the two numbers is 4

Complexity Analysis
Time Complexity: O(N).

Space Complexity: O(1).
</pre>


<h3>Optimal Approach</h3>

<pre>
  Algorithm / Intuition
Solution 2: Using Euclidean’s theorem.

Intuition: Gcd is the greatest number which is divided by both a and b.If a number is divided by both a and b,
it is should be divided by (a-b) and b as well. 
</pre>

![download](https://github.com/samsorrahman/DSA-Python/assets/112087807/591b33be-6dd2-4644-ad55-a14df7dff058)

<pre>
  Approach:

Recursively call gcd(b,a%b) function till the base condition is hit.
b==0 is the base condition.When base condition is hit return a,as gcd(a,0) is equal to a.

def gcd(a, b):
    if b == 0:
        return a
    return gcd(b, a % b)


if __name__ == "__main__":
    a = 4
    b = 8
    print("The GCD of the two numbers is", gcd(a, b))

  Complexity:
  Time Complexity: O(logɸmin(a,b)), where ɸ is 1.61.

  Space Complexity: O(1).
</pre>
