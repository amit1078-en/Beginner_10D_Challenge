# Odd Zeroes

```
Michael is bored in the office and as a fun activity he gives his friend 
Jim some numbers ranging from 1 to 10^5 and asks him to find out which of 
these numbers' factorial has odd number of trailing zeroes.

Jim has a lot of work to do but also can't avoid Michael therefore he wants
to get rid of this task as soon as possible and hence he wants your help.
Your task is to complete the function oddTrailingZeroes which takes integer 
N as input and returns true if the factorial of number contains odd no. of 
zeroes and false if it contains even no. of zeroes making the task easier.

```

**Test Cases:-**

Input: N=6
Output: true

Explanation:

> The factorial of number 6 = 6! = 720 has odd number of trailing
> zeroes( 1 zero ) hence the answer is true.

Input: N=13
Output: false

Explanation:

> The factorial of number 13 = 13! = 6227020800 has even number of
> trailing zeroes( 2 zeroes ) hence the answer is false.

Input: N=125
Output: true

Explanation:

> The factorial of number 125 has odd number of trailing zeroes( 31
> zeroes ) hence the answer is true.

**Constraints:**

> 1<= N <= 10^5

**Trailing Zeroes Examples:**

Number=>No.of trailing zeroes
100=>2 
20290=>1 
10001=>0 
70000=>4

