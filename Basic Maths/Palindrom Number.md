Check if a number is Palindrome or Not<br>
Problem Statement:  Given a number check if it is a palindrome.
<pre>
  Example 1:
Input: N = 123
Output: Not Palindrome Number
Explanation: 123 read backwards is 321.Since these are two different numbers 123 is not a palindrome.

Example 2:
Input: N =  121 
Output: Palindrome Number
Explanation: 121 read backwards as 121.Since these are two same numbers 121 is a palindrome.
</pre>

<pre>
  Approach:  We can reverse the original number and compare the original with the reversed number. If both are the same, the number qualifies as a palindrome number.

Say the input number is X. Declare a variable Y to store the reverse and initialize it to 0. Make a copy of X, say dummy that will be used later for comparison.

 Let’s understand the procedure to reverse a number.

At every step extract the last digit using the % operator. Suppose X%10 = d.
We will append this last digit, d to Y using a formula 10*Y+d.
The last digit of X has been used. Discard it using X/10. 
Repeat these steps for the remaining digits. After every iteration, the size of X will shrink by one digit. Terminate the iteration when X = 0 meaning no new digits are left to be reversed.

The reversed number Y is compared with the dummy variable since X was destroyed while iteration. If Y equals dummy print “Palindrome Number” otherwise “Not Palindrome Number”.

Code:

  def reverse(X):
    Y = 0
    while X > 0:
        # Extract the last digit
        digit = X % 10
        # Appending last digit
        Y = Y * 10 + digit
        # Shrinking X by discarding the last digit
        X = X // 10
    return Y




if __name__ == "__main__":
    X = 121
    dummy = X
    Y = reverse(X)
    if dummy == Y:
        print("Palindrome Number")
    else:
        print("Not Palindrome Number")
  
Time Complexity: O(logN) for reversing N digits of input integer.

Space Complexity: O(1)
</pre>

<h3>Solution 2</h3>
<pre>
  To achieve O(1) time complexity for checking if a number is a palindrome, you can employ the following approach:

Convert the input number to a string.
Split the string into two halves.
Compare the characters of the two halves from the beginning and the end simultaneously.
If all corresponding characters match, the number is a palindrome; otherwise, it is not.
This approach has O(1) time complexity because it only compares a constant number of characters, regardless of the length of the input number.
Here's the code implementation:

def is_palindrome(num):
    num_str = str(num)
    mid = len(num_str) // 2

    for i in range(mid):
        if num_str[i] != num_str[len(num_str) - 1 - i]:
            return False

    return True
</pre>
