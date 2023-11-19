<h1>Print all Divisors of a given Number</h1>
Problem Statement: Given a number, print all the divisors of the number.<br>
A divisor is a number that gives the remainder as zero when divided.

<pre>
  Example 1:
Input: n = 36
Output: 1 2 3 4 6 9 12 18 36
Explanation: All the divisors of 36 are printed.

Example 2:
Input: n = 97
Output: 1 97
Explanation: Since 97 is a prime number, only 1 and 97 are printed.
</pre>

<h1>Brute Force Approach</h1>
<pre>
  Algorithm / Intuition
Solution 1:
Intuition:

As we know the divisors of a number will definitely be lesser or equal to the number, all the numbers between 1 and the number, are the possible candidates for the divisors.

Approach:

This is the basic approach. As we know the possible candidates, we iterate upon all the candidates and check whether they divide the actual number.
If it divides, then it is one of the divisors. Therfore, we print it.
If it does not divide, then it is not a divisor. We do this for all the candidates.
</pre>

<h1>
  Code
</h1>
<pre>
  def printDivisorsBruteForce(n):
    print("The Divisors of ",n," are:")
    for i in range(1,n+1):
        if n % i == 0:
            print(i,end=" ")
    print()
if __name__ == "__main__":
    printDivisorsBruteForce(36)

    

Complexity Analysis
Time Complexity: O(n), because the loop has to run from 1 to n always.

Space Complexity: O(1), we are not using any extra space.
</pre>





<h1>Optimal Approach</h1>
<pre>
  Algorithm / Intuition
Solution 2:
Intuition:
The above method takes O(n) time complexity. We can also think of another approach. If we take a closer look, we can notice that the quotient of a division by one of the divisors is actually another divisor. Like, 4 divides 36. The quotient is 9, and 9 also divides 36.
Another intuition is that the root of a number acts as a splitting part of all the divisors of a number.
Also, the quotient of a division by any divisor gives an equivalent divisor on the other side. Like, 4 gives 9 while dividing 36. See the image below.
</pre>

![Divisors](https://github.com/samsorrahman/DSA-Python/assets/112087807/f58fff27-a79d-41ec-bbaf-2737fd33df99)


<pre>
  Approach:
From the intuition, we can come to the conclusion that we don’t need to traverse all the candidates and if we found a single divisor, we can also find another divisor(Here, we need to be careful, if the given number is a perfect square, like 36, 6 also give 6 as quotient. This is a corner case.)
By keeping these in mind, it is enough if we traverse up to the root of a number. Whenever we find a divisor, we print it and also print the quotient. If the quotient is the same, we ignore it. Because the root of a perfect square will give the same quotient as itself.
The quotients are the numbers that are on the other side of the root. So, it’s okay if we stop traversing at the root.
This approach is more time efficient than the previous one. But the output sequences are not the same. In the previous approach, we get an ordered output unlike here.
</pre>


<h1>Code and Complexity Analysis</h1>
<pre>
  def printDivisorsOptimal(n):
    print("The Divisors of",n,"are:")
    for i in range(1, int(n**0.5)+1):
        if n % i == 0:
            print(i, end=" ")
            if i != n/i:
                print(int(n/i), end=" ")
    print()
if __name__ == "__main__":
    printDivisorsOptimal(36)


  Complexity Analysis
Time Complexity: O(sqrt(n)), because every time the loop runs only sqrt(n) times.

Space Complexity: O(1), we are not using any extra space.
</pre>
