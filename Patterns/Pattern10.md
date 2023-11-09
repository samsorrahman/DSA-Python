<pre>
def pattern10(N):
  for i in range(1, 2 * N):
    stars = min(i, 2 * N - i)
    for j in range(stars):
      print("*", end="")
    print()

if __name__ == "__main__":
  N = 5
  pattern10(N)
</pre>

----------------------------------------------------------------
<pre>
  Output

    *    
    **   
    ***  
    **** 
    *****
    **** 
    ***  
    **   
    *  
</pre>
