def pattern8(N): <br>
    for i in range(N):<br>
        //printing spaces<br>
        for j in range(i):<br>
            print(" ", end="")<br>
        // Printing stars<br>
        for j in range(2 * N - (2 * i + 1)):<br>
            print("*", end="")<br>
        // Printing spaces <br>
        for j in range(i):<br>
            print(" ", end="")<br>
        print()<br>

if __name__ == "__main__":<br>
    N = 5<br>
    pattern8(N)<br>


    -----------------------------------------------------
    Output:
    *********
     ******* 
      *****  
       ***
        *   
