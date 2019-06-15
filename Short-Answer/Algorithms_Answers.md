# Analysis of Algorithms

## Exercise I

Give an analysis of the running time of each snippet of
pseudocode with respect to the input size n of each of the following:

```
a)  a = 0     ---> 0(1)
    while (a < n * n * n):  ---> o(n)
      a = a + n * n   ---> 0(1)
```
This algorithm is 0(n). Line one sets a variable and only runs once so it is 0(1). Line two is a while loop and the number of times it runs is dependent on n so it is 0(n). Line 3 is similar to line one in that it sets a value to a variable making it 0(1). When we add this together the total run time would be 0(n).
```
b)  sum = 0   ---> 0(1)
    for i in range(n):  ---> 0(n)
      i += 1
      for j in range(i + 1, n):
        j += 1
        for k in range(j + 1, n):
          k += 1
          for l in range(k + 1, 10 + k):
            l += 1
            sum += 1
```

```
c)  def bunnyEars(bunnies):
      if bunnies == 0:
        return 0

      return 2 + bunnyEars(bunnies-1)
```

## Exercise II

Suppose that you have an _n_-story building and plenty of eggs. Suppose also that an egg gets broken if it is thrown off floor _f_ or higher, and doesn't get broken if dropped off a floor less than floor _f_. Devise a strategy to determine the value of _f_ such that the number of dropped eggs is minimized.

Write out your proposed algorithm in plain English or pseudocode and give the runtime complexity of your solution.re.