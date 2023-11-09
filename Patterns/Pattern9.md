<pre>
  def erect_pyramid(N):
    for i in range(N):
        for j in range(N - i - 1):
            print(" ", end="")
        for j in range(2 * i + 1):
            print("*", end="")
        for j in range(N - i - 1):
            print(" ", end="")
        print()

def inverted_pyramid(N):
    for i in range(N):
        for j in range(i):
            print(" ", end="")
        for j in range(2 * N - (2 * i + 1)):
            print("*", end="")
        for j in range(i):
            print(" ", end="")
        print()

if __name__ == "__main__":
    N = 5
    erect_pyramid(N)
    inverted_pyramid(N)
</pre>

-------------------------------------------------------
<pre>
Output
    *    
   ***   
  *****  
 ******* 
*********
*********
 ******* 
  *****  
   ***   
    *  

</pre>
