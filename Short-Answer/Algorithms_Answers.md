# Analysis of Algorithms

## Exercise I

Give an analysis of the running time of each snippet of
pseudocode with respect to the input size n of each of the following:

```
a)  a = 0     ---> O(1)
    while (a < n * n * n):  ---> O(n)
      a = a + n * n   ---> O(1)
```
This algorithm is O(n). Line one sets a variable and only runs once so it is O(1). Line two is a while loop and the number of times it runs is dependent on n so it is O(n). Line 3 is similar to line one in that it sets a value to a variable making it O(1). When we add this together the total run time would be O(n).
```
b)  sum = 0   ---> O(1)
    for i in range(n):  ---> O(n)
      i += 1    ---> O(1)
      for j in range(i + 1, n): ---> O(n)
        j += 1  ---> O(1)
        for k in range(j + 1, n): ---> O(n)
          k += 1  ---> O(1)
          for l in range(k + 1, 10 + k): ---> O(1)
            l += 1  ---> O(1)
            sum += 1 ---> 0(1)
```
This algorithm would be O(n^3). It as a total of 3 loops that are dependant on n. The last is a range and will never vary on the number of times that it runs. SO if you multiple O(n) three times we get O(n^3).

```
c)  def bunnyEars(bunnies):
      if bunnies == 0:  ---> O(1)
        return 0  ---> O(1)

      return 2 + bunnyEars(bunnies-1)  ---> O(n)
```
This algorithm is 0(n). The first 3 lines are dropped or ignored because they are all O(1). The last line turns the function into a recursive loop that is dependant on 'n'. To determine the number of times that it runs. 

## Exercise II

Suppose that you have an _n_-story building and plenty of eggs. Suppose also that an egg gets broken if it is thrown off floor _f_ or higher, and doesn't get broken if dropped off a floor less than floor _f_. Devise a strategy to determine the value of _f_ such that the number of dropped eggs is minimized.

Write out your proposed algorithm in plain English or pseudocode and give the runtime complexity of your solution.re.