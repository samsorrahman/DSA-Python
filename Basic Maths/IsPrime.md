<pre>
  Check if a number is prime or not
Problem Statement: Given a number, check whether it is prime or not. A prime number is a natural number that is only divisible by 1 and by itself.

Examples 1 2 3 5 7 11 13 17 19 …


  Example 1:
Input: N = 3
Output: Prime
Explanation: 3 is a prime number

Example 2:
Input: N = 26
Output: Non-Prime
Explanation: 26 is not prime



  Brute Force Approach
Algorithm / Intuition
Solution 1: Using Iterative solution

Approach: 

A prime number is a natural number that is only divisible by 1 and by itself. Examples 1 2 3 5 7 11 13 17 19 …

Running a for loop for checking if the number is divisible by a number from 2 to a number less than a given number.

And then checking if the number is divisible by the numbers from 2 to the number less than a given number

Then, If the remainder is zero, that means it is divisible and hence not a prime number.

If the loop runs till square root and none of the numbers divided it completely. So it is the Prime number.


<h1>Code</h1>
  def isPrime(n):
    for i in range(2, n):
        if n % i == 0:
            return False
    return True




if __name__ == "__main__":
    n = 11
    ans = isPrime(n)
    if n != 1 and ans == True:
        print("Prime Number")
    else:
        print("Non Prime Number")

  <h1>Time Complexity</h1>
  Time Complexity: O(n)

  Space Complexity: O(1)
</pre>


<hr>

<h1>Optimal Approach </h1>

<pre>
  Algorithm / Intuition
Solution 2: Optimized Approach

Approach: Running the for loop till the square root of the number

A prime number is a natural number that is only divisible by 1 and by itself. Examples 1 2 3 5 7 11 13 17 19 …

Using a for loop for checking if the number is divisible by a number from 2 to its square root.

Running the for loop from 2 to the square root of the number.

And then checking if the number is divisible by the numbers from 2 to its square root.

Then, If the remainder is zero, that means it is divisible and hence not a prime number.

If the loop runs till square root and none of the numbers divided it completely. So it is the Prime number.

<h1>Code</h1>
  from math import sqrt

def isPrime(N):
    for i in range(2, int(sqrt(N))):
        if N % i == 0:
            return False
    return True


if __name__ == "__main__":
    n = 11
    ans = isPrime(n)
    if n != 1 and ans == True:
        print("Prime Number")
    else:
        print("Non Prime Number")


  Complexity Analysis
Time Complexity: O(√n)

Space Complexity: O(1)
</pre>





