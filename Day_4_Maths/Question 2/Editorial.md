# Odd Zeroes Solution

**Problem Statement 2:** 

**Difficulty:** Easy

**Pre-Requisites:** Basic Mathematics

## Brief Explanation: 

Find the count of 5 in the prime factors of N! which will give us total number of trailing zeroes and then return true if count is odd and false if even.

> Total count of 5 = floor(N/5)+floor(N/25)+floor(N/125)+....

**Explanation:**

Instead of finding factorial, find the count of numbers which contribute to trailing zero.
A pair of 2 & 5 contributes to one trailing zero (2×5=10)

So, we need to find total number of pairs of 2&5 included in prime factorization of the N!

As count of 2's will always be greater than count of 5's
Only calculate total number of 5's to get total count of trailing zeroes.

Lets, consider example of 125! = 1×2×3×4×5×6×7×8×9×10×...×25×...125

Here 5,10,15,20,... all have one 5 in their prime factors
However, some numbers have two 5's such as 25,50,75,...
And some have three 5's such as 125

Count of no. having at least one 5 in their prime factors = N/5

Count of no. having at least two 5 in their prime factors = N/25
and so on …

From this we can formulate the given expression:
Total count of 5 = floor(N/5)+floor(N/25)+floor(N/125)+....

## Code:
```
bool oddTrailingZeroes(int N)
{
	int count=0;
	for(int i=5;i<=N;i=i*5)
	{
		count+=N/i;
	}

	if(count%2!=0)
	{
		return true;
	}

	return false;
}
```
**Time Complexity:**

>  O(log5(N))
