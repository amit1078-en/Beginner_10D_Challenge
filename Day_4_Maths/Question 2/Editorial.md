
# Fib-Reset Editorial

Type : Easy
Topics : Fibonacci, Modulo

## Hints :

-  The pattern is repeating and we can use MOD (%).

## Example

Let's take an example of N = 9, M = 15.
then we will have series like this

> (0,1,1,2,3,5,8,13,21,0,1,1,2,3,5)


- We know pattern repeats after event 9 steps 

    0  1  1  2  3  5  8  13  21
    
    0  1  1  2  3  5  8  13  21
    
    0  1  1  2  3  5  8  13  21

and we need to find the 15th occurrence 

then a simple formula,
 number = (M%N)
 number = (15%9) = 6

so we need to output 6th number of the Fibonacci series.

## Code

For generating nth Fibonacci you can use this reference.
https://www.geeksforgeeks.org/program-for-nth-fibonacci-number/
