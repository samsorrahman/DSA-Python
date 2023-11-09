def pattern8(N):
    for i in range(N):
        //printing spaces
        for j in range(i):
            print(" ", end="")
        // Printing stars
        for j in range(2 * N - (2 * i + 1)):
            print("*", end="")
        // Printing spaces 
        for j in range(i):
            print(" ", end="")
        print()

if __name__ == "__main__":
    N = 5
    pattern8(N)


    -----------------------------------------------------
    Output:
    *********
     ******* 
      *****  
       ***
        *   
