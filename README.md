# ucb-cs61A
Q1: A Plus Abs B
Fill in the blanks in the following function for adding a to the absolute value of b, without calling abs.

from operator import add, sub

def a_plus_abs_b(a, b):
    """Return a+abs(b), but without calling abs.

    >>> a_plus_abs_b(2, 3)
    5
    >>> a_plus_abs_b(2, -3)
    5
    """
    if b < 0:
        f = sub
    else:
        f = add
    return f(a, b)
    
a_plus_abs_b(1,-2)

Q2: Two of Three
Write a function that takes three positive numbers and returns the sum of the squares of the two largest numbers. Use only a single line for the body of the function.

def two_of_three(a, b, c):
    """Return x*x + y*y, where x and y are the two largest members of the
    positive numbers a, b, and c.

    >>> two_of_three(1, 2, 3)
    13
    >>> two_of_three(5, 3, 1)
    34
    >>> two_of_three(10, 2, 8)
    164
    >>> two_of_three(5, 5, 5)
    50
    """
    return _____

from operator import add,mul
def two_of_three(a,b,c):
    f = add(mul(max(a,b,c),max(a,b,c)),mul(min(c,max(a,b)),min(c,max(a,b))))
    #两个数中间最大的数和第三个数做比较，小者为中间数（第二大的数字）
    return f
result = two_of_three(1,2,3)
print(result)


Q3: Largest Factor
Write a function that takes an integer n that is greater than 1 and returns the largest integer that is smaller than n and evenly divides n.

def largest_factor(n):
    """Return the largest factor of n that is smaller than n.

    >>> largest_factor(15) # factors are 1, 3, 5
    5
    >>> largest_factor(80) # factors are 1, 2, 4, 5, 8, 10, 16, 20, 40
    40
    >>> largest_factor(13) # factor is 1 since 13 is prime
    1
    """
    "*** YOUR CODE HERE ***"
from operator import add,sub,mul
def largest_factor(a):
    factors = []
    for i in range(1,a-1):
        if a % i == 0:
            factors.append(i)
        else:
            continue
    return max(factors)

result = largest_factor(80)
print(result)

05
def if_function(condition,True_result,False_result):
    if condition:
        return  True_result
    else:
        return  False_result

def with_if_statement():
    """
    >>> result = with_if_statement()
    2
    >>> print(result)
    None
    """
    if c():
        return t()
    else:
        return f()

def with_if_function():
    """
    >>> result = with_if_function()
    1
    2
    >>> print(result)
    None
    """
    return if_function(c(), t(), f())

def c():
    return False


def t():
    "*** YOUR CODE HERE ***"
    print(1)

def f():
    "*** YOUR CODE HERE ***"
    print(2)

print(if_function(False,1,2))
print(with_if_function())

06
def hailstone(x):
    while x != 1:
        print(x)
        if x % 2 == 0:
            x = x//2
        else:
            x = 3*x + 1



hailstone(999)
