<h2>Check if a number is Armstrong Number or not</h2>
<p>Problem Statement: Given a number, check if it is Armstrong Number or Not.</p>

<pre>
  Example 1:
Input:153 
Output: Yes, it is an Armstrong Number
Explanation: 1^3 + 5^3 + 3^3 = 153

Input:170 
Output: No, it is not an Armstrong Number
Explanation: 1^3 + 7^3 + 0^3 != 170
</pre>

<p>
  What are Armstrong Numbers?

Armstrong Numbers are the numbers having the sum of digits raised to power no. of digits is equal to a given number. <br>
Examples- 0, 1, 153, 370, 371, 407, and 1634 are some of the Armstrong Numbers.
</p>

![pasted image 0](https://github.com/samsorrahman/DSA-Python/assets/112087807/425a20b6-071d-42da-9284-d5ac19f91f3d)

![pasted image 0 (1)](https://github.com/samsorrahman/DSA-Python/assets/112087807/e8da3ec2-5db9-4032-aba0-5330c0aca53d)

<pre>
  Solution
Approach:

Let us check one 3-digit Armstrong Number

n=153

sum=0

No. of digits = 3 so we need to cube every digit.

In the First iteration, extract digit 3 from 153 and cube it which becomes 27, add it to sum= 0+27=27 which becomes 27 now

In Second iteration , extract digit 5 from 15 and cube it which becomes 125 , add it to sum = 27 +125 = 152 which becomes 152 now

In Third iteration , extract digit 1 from 1 and cube it which becomes 1 , add it to sum = 152 + 1 = 153 which becomes 153 now.

The original Number was 153 and the sum of cubes = 153. 

This means it is an Armstrong Number.
</pre>
![pasted image 0 (2)](https://github.com/samsorrahman/DSA-Python/assets/112087807/cf992aaf-a8d8-4756-9fe5-616881b711c8)

<pre>
  def ArmstrongNumber(n):
    originalno = n
    count = 0
    temp = n
    while temp != 0:
        count += 1
        temp //= 10
    sumofpower = 0
    while n != 0:
        digit = n % 10
        sumofpower += pow(digit, count)
        n //= 10
    return sumofpower == originalno




if __name__ == "__main__":
    n1 = 153
    if ArmstrongNumber(n1):
        print("Yes, it is an Armstrong Number")
    else:
        print("No, it is not an Armstrong Number")



  Output:

Yes, it is an Armstrong Number

Time Complexity: O(n) where n is the number of digits since we need to traverse every digit and add digits raised to power no.
of digits to sum.

Space Complexity: O(1) since no extra space is required
</pre>
