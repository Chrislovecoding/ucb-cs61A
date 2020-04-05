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
