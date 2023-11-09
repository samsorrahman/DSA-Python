def pattern7(N):
    for i in range(N):
        for j in range(N - i - 1):
            print(" ", end="")
        for j in range(2 * i + 1):
            print("*", end="")
        for j in range(N - i - 1):
            print(" ", end="")
        print()

if __name__ == "__main__":
    N = 5
    pattern7(N)


-------------------------------------------------------------------------
    *    
   ***   
  *****  
 ******* 
*********
