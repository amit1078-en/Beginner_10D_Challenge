# Fib-Reset

Fib-Reset is a type of Fibonacci series that resets its value after generating every N numbers. 

If given N is 5 then we will have our series something like this

    0 1 1 2 3 (reset) 0 1 1 2 3 (reset) 0 1 1 ... till infinity

Given the value of N your task is to find out the Mth number of the sequence.

## Input Output format

**Input :**

First Line of Input take two values N,M.

**Output :**

Return the value of Mth number in new line.

**Constraints :**

    1 <= N <= 30
    1 <= M <= 10^9

**Testcase 1:**

    Input  : N = 9, M = 15
    Output : 5
    
**Explanation:**

If we create a series according to the question then we have 
(0,1,1,2,3,5,8,13,21,0,1,1,2,3,5) and if we follow one base indexing we have number 5
at 15th index.
