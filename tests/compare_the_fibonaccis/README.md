**Note-1** - This is a test related to your understanding of Fundamentals of Computer Science.

**Note-2** The example codes in this problem uses Python 3 and hence there are type hinting


You are given two simple functions to generate the sum of [Fibonacci numbers](https://en.wikipedia.org/wiki/Fibonacci_number) until a given times (Like, first 10 or 20 or 50 Fibonacci numbers)

### Function-1 (fib1)

```
def fib1(n: int) -> int:
    if n < 2:
        return n
    return fib1(n-2) + fib1(n-1)
```

**AND**

### Function-2 (fib2)

```
def fib2(n: int) -> int:
    if n == 0:
        return n
    last: int = 0
    next: int = 1
    for _ in range(1, n):
        last, next = next, last + next
    return next
```

Here are the two questions we had been wondering

1. If you run both of them to generate the sum of first 50 Fibonacci numbers, like so `fib1(50)` and `fib2(50)` what do you observe? Can you explain your observations?

2. Can you propose a better version of fib1? 

--------

3. (This is a bonus question, only applicable if you have solved 2. and **not** mandatory, however, nice to be answered :)) What are the additional observations that you made with the better version you proposed? Also what are your ideas about the time complexity of these two functions?