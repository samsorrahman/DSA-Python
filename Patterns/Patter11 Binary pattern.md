<pre>
  def pattern11(N):
    start = 1
    for i in range(N):
        if i % 2 == 0:
            start = 1
        else:
            start = 0
        for j in range(i + 1):
            print(start, end="")
            start = 1 - start
        print()

if __name__ == "__main__":
    N = 5
    pattern11(N)
</pre>

------------------------------------------------------------------------
<pre>
  Output
  1
  01
  101
  0101
  10101

</pre>
